# Crear el ClienteRestController

# 1. Crear el paquete controllers

![image](https://user-images.githubusercontent.com/31961588/194681534-09a9a297-ec63-4e8a-b965-8c0015f28054.png)

## 2. Crer el ClienteRestController


![image](https://user-images.githubusercontent.com/31961588/194681563-2c1ed83f-605f-4858-8c22-370dbe528ac1.png)

**ClienteRestController.java**

```Java
package com.mintic.controllers;

import java.util.HashMap;
import java.util.List;
import java.util.Map;
import java.util.stream.Collectors;

import javax.validation.Valid;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.dao.DataAccessException;
import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.PutMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

import com.mintic.models.entities.Cliente;
import com.mintic.models.services.IClienteService;

@RestController
@RequestMapping("/api")
public class ClienteRestController {
	
	@Autowired
	private IClienteService clienteService;
	
	@GetMapping("/clientes")
	public List<Cliente> index(){
		return clienteService.findAll();
		
	}
	
	@GetMapping("/cliente/{id}")
	public Cliente show(@PathVariable Long id) {
		return clienteService.findById(id);
		
	}
	
	@PostMapping("/clientes")
	public ResponseEntity<?> create(@Valid @RequestBody Cliente cliente, BindingResult result) {
		
		Cliente clienteNew=null;
		
		Map<String,Object> response=new HashMap<>();
		
		if(result.hasErrors()){			
			List<String> errors=result.getFieldErrors()
					            .stream()
					            .map(err->"El campo "+err.getField()+ " "+err.getDefaultMessage())
					            .collect(Collectors.toList());
			
			response.put("errors", errors);
			 return new ResponseEntity<Map<String,Object>>(response,HttpStatus.BAD_REQUEST);			
 		}
		try {
			clienteNew=this.clienteService.save(cliente);
			
		}catch(DataAccessException e) {
			response.put("mesaje", "Error al realiar el insert en la base de datos");
			response.put("error",e.getMessage().concat(":").concat(e.getMostSpecificCause().getMessage()));
			 return new ResponseEntity<Map<String,Object>>(response,HttpStatus.INTERNAL_SERVER_ERROR);
		}
		
		response.put("mensaje", "El cliente ha sido creado con éxito");
		response.put("cliente", clienteNew);
		return new ResponseEntity<Map<String,Object>>(response,HttpStatus.CREATED);	
		
		
	}
	
	@PutMapping("/cliente/{id}")
	public ResponseEntity<?> update(@Valid @RequestBody Cliente cliente, BindingResult result,@PathVariable Long id) {
		
		Cliente currentCliente=this.clienteService.findById(id);
		
		Cliente updateClient =null;		
		
		
		Map<String,Object> response=new HashMap<>();
		
		if(result.hasErrors()){			
			List<String> errors=result.getFieldErrors()
					            .stream()
					            .map(err->"El campo "+err.getField()+ " "+err.getDefaultMessage())
					            .collect(Collectors.toList());
			
			response.put("errors", errors);
			 return new ResponseEntity<Map<String,Object>>(response,HttpStatus.BAD_REQUEST);			
 		}
		if(currentCliente==null) {
			response.put("mensaje", "Error: no se puede editar, el client ID: ".concat(id.toString())
					 .concat("no existe en la base de datos"));
			 return new ResponseEntity<Map<String,Object>>(response,HttpStatus.NOT_FOUND);
			
		} 
		try {
			
			currentCliente.setNombres(cliente.getNombres());
			currentCliente.setApellidos(cliente.getApellidos());
			currentCliente.setEmail(cliente.getEmail());
			currentCliente.setTelefono(cliente.getTelefono());
			currentCliente.setSaldo(cliente.getSaldo());			
			updateClient=this.clienteService.save(currentCliente);
			
		}catch(DataAccessException e) {
			response.put("mesaje", "Error al realiar el insert en la base de datos");
			response.put("error",e.getMessage().concat(":").concat(e.getMostSpecificCause().getMessage()));
			 return new ResponseEntity<Map<String,Object>>(response,HttpStatus.INTERNAL_SERVER_ERROR);
		}
		
		response.put("mensaje", "El cliente ha sido actulizado con éxito");
		response.put("cliente", updateClient);
		return new ResponseEntity<Map<String,Object>>(response,HttpStatus.CREATED);	
		
		
	}


}

```
