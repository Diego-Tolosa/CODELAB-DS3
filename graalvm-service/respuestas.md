# Codelab Generar un servicio Spring Boot nativo con GraalVM

## Tecnologías Utilizadas
- Java 21+
- Spring Boot
- Lombok

## Levantar el contenedor
```sh
docker compose up -d
```

## Entrar al contenedor
```sh
docker exec -it graalvm-builder /bin/bash
```

## Instalar dependencias
```sh
apt-get update && apt-get install -y apt-utils zip unzip curl wget build-essential zlib1g-dev
```

## Instalar SDKMAN (gestor de Java):
```sh
curl -s "https://get.sdkman.io" | bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
```

## Instalar GraalVM CE:
```sh
sdk list java
sdk install java 23.0.2-graalce
java -version
```

## Compilar el binario nativo
```sh
cd project
./mvnw clean package -Pnative -DskipTests
```

## Construir la imagen:
```sh
docker build -t juanlopezaranzazu388/graalvm-service:latest .
```

## Ejecutar la imagen:
```sh
docker run --rm -p 8080:8080 juanlopezaranzazu388/graalvm-service
```

## Detener los servicios
```sh
docker compose down
```

## Resultados

### Levantar el contenedor
![Leventar Contenedor](/graalvm-service/images/LevantarContenedor.PNG)

### Entrar contenedor
![Entrar Contenedor](/graalvm-service/images/EntrarContenedor.PNG)

### Instalar dependencias
![Instalar Dependencias](/graalvm-service/images/InstalarDependencias.PNG)

### Instalar sdkman
![Instalar sdkman](/graalvm-service/images/InstalarSDKMAN.PNG)

### Instalar graalvm
![Instalar graalvm](/graalvm-service/images/InstalarGraalvm.PNG)

### Instalar Java 23
![Instalar Java 23](/graalvm-service/images/InstalarJava23.PNG)

### Compilar Binario
![Compilar Binario](/graalvm-service/images/CompilarBinario.PNG)

### Construir Imagen
![Construir Imagen](/graalvm-service/images/ContruirImagen.PNG)

### Ejecutar Imagen
![Ejecutar Imagen](/graalvm-service/images/EjecutarImagen.PNG)

### Detener Servicios
![Ejecutar Imagen](/graalvm-service/images/DetenerServicios.PNG)