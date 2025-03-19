FROM openjdk:8-jdk-alpine

# Crear un grupo y un usuario
RUN addgroup -S paymentchain && adduser -S admin -G paymentchain

# Cambiar al usuario creado
USER admin:paymentchain

# Crear un volumen para /tmp
VOLUME /tmp

# Especifica el archivo JAR correcto
ADD target/eurekaserver-0.0.1-SNAPSHOT.jar app.jar

# Establecer las opciones de Java
ENV JAVA_OPTS=""

# Define el comando de inicio
ENTRYPOINT ["sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar"]
