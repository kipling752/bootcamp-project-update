# Étape 1 : image de base légère Java 17
FROM amazoncorretto:17-alpine

# Étape 2 : répertoire de travail
WORKDIR /app

# Étape 3 : copier le jar compilé depuis Maven
COPY target/paymybuddy.jar app.jar

# Étape 4 : exposer le port de l'application
EXPOSE 8080

# Étape 5 : variables de connexion (écrasées par docker-compose)
ENV SPRING_DATASOURCE_URL=""
ENV SPRING_DATASOURCE_USERNAME=""
ENV SPRING_DATASOURCE_PASSWORD=""

# Étape 6 : commande de démarrage
ENTRYPOINT ["java", "-jar", "app.jar"]
