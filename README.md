# Spring Boot v3 Keycloak Integration

Oauth2 keycloak with spring boot client-credentials

Run docker in container: 
```
docker pull quay.io/keycloak/keycloak:latest
```
```
docker run --name minkeycloak -d -p 8081:8080 -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=admin quay.io/keycloak/keycloak:latest start-dev
```


### Endpoints
Anonymous:
```
[GET] http://localhost:8080/api/anonymous
```
Admin:
```
[GET] http://localhost:8080/api/admin
Authorization - Bearer Token with admin privileges
```
User:
```
[GET] http://localhost:8080/api/user
Authorization - Bearer Token with admin or user privileges
```

Based off: https://medium.com/geekculture/using-keycloak-with-spring-boot-3-0-376fa9f60e0b
