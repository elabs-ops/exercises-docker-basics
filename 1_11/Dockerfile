FROM ibmjava:8-sdk
WORKDIR /usr/src/app
COPY --chmod=755 . .
RUN ./mvnw package
EXPOSE 8080
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
