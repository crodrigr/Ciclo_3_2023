# Crear los servicios de la clase cliente para el crud

## 1. Crear el paquete model.services 

![image](https://user-images.githubusercontent.com/31961588/194678637-222dda59-605f-45bb-9d9e-f7e86d27079d.png)

## 2. Crear la interfaz IClienteService

![image](https://user-images.githubusercontent.com/31961588/194678707-8406be5e-9ff5-42fa-a4f6-c27a51128b93.png)

## 2.1 

![image](https://user-images.githubusercontent.com/31961588/194678883-10a178bf-19c0-4e66-941d-4d06b2488b8b.png)

## 3. Crear la clase ClienteServiceImpl 


![image](https://user-images.githubusercontent.com/31961588/194678955-b05e7f34-16ea-48c9-ac74-d3b31efa1ed5.png)

## 3.1 

![image](https://user-images.githubusercontent.com/31961588/194679309-27a3965d-4700-44e3-ba85-2ffa02a5d49f.png)


```Java
package com.mintic.models.services;

import java.util.List;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import com.mintic.models.dao.IClienteDao;
import com.mintic.models.entities.Cliente;

@Service
public class ClienteServiceImpl implements IClienteService {
	
	@Autowired
	private IClienteDao clienteDao;

	@Override
	public List<Cliente> findAll() {	
		return (List<Cliente>) clienteDao.findAll();
	}

	@Override
	public Cliente findById(Long id) {
		
		return clienteDao.findById(id).orElse(null);
	}

	@Override
	public Cliente save(Cliente cliente) {		
		return clienteDao.save(cliente);
	}

	@Override
	public void delete(Cliente cliente) {
		
		clienteDao.delete(cliente);
		
	}

}

```
