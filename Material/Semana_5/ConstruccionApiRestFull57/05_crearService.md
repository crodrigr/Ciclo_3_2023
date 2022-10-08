# Crear la IClienteService y ClienteServiceImpl que son los servicios que va consumir el restController. 


## 1. Crear el paquete models.service

![image](https://user-images.githubusercontent.com/31961588/194681058-6a491c38-b3d2-4311-a339-81c45f828389.png)

## 2. Crear la interfaz IClienteService


![image](https://user-images.githubusercontent.com/31961588/194681083-ec4a1e59-ba4f-4369-81d7-e248eea580c2.png)

## 2.1 IClienteService

![image](https://user-images.githubusercontent.com/31961588/194681179-61bfecd4-3a44-4b10-a9d2-01cea023efad.png)


## 3. Crear la clase ClienteServiceImpl

![image](https://user-images.githubusercontent.com/31961588/194681209-bf720d89-3587-45be-9915-364ddbeaaa22.png)

## 3.1 ClienteServiceImpl

![image](https://user-images.githubusercontent.com/31961588/194681470-c7e85f28-9534-41ee-b7d1-b711f341364f.png)

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
