# Introducción Práctica a Kubernetes (Nivel Básico)

## Preparar el entorno

Esto se hizon en windows utilizando Docker Desktop

- Abrimos Docker Desktop.
- vamos a settings > Kubernetes.
- Activamos "Enable Kubernetes".
- Esperamos que aparezca "Kubernetes is running".
- Luego verificamos en una consola el clúster.

![Prepaparar el Entorno](./imgs/PrepararEntorno.PNG)
![Prepaparar el Entorno](./imgs/PrepararEntorno2.PNG)

## Desplegando nuestra primera aplicación

- Creamos un deployment con nginx
![Crear el deployment](./imgs/Creardeployment.PNG)

- Verificamos que el pod se esté ejecutando:
![Verificar el pod](./imgs/VerificarPod.PNG)

- exponemos el servicio
![Exponer el servicio](./imgs/ExponerServicio.PNG)

- Revisamos el servicio:
![Revizar el servicio](./imgs/RevizamosService.PNG)

### Accedemos desde el navegador

![Acceder desde el navegador](./imgs/AccederNavegador.PNG)

### Escalamos la aplicación

- Aumentamos el número de replicas a 3:
![Aumentar el número de replicas](./imgs/EscalarAplicación.PNG)

### Ahora eliminamos todo

- Limpiamos los recursos creados
![Limpiar los recursos creados](./imgs/EliminarTodo.PNG)
