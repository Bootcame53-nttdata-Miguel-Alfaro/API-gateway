# API Gateway

Este proyecto configura un API Gateway utilizando Spring Cloud Gateway para enrutar las solicitudes a varios microservicios. El API Gateway actúa como un punto de entrada único para todos los microservicios y facilita la gestión de rutas y balanceo de carga.

## Configuración del Proyecto

### Propiedades de Configuración

- **Nombre de la aplicación**: `api-gateway`
- **Eureka Instance Hostname**: `10.0.246.185`
- **Eureka Service URL**: `http://10.0.247.18:8761/eureka/`

### Configuración de Rutas

#### Customer Microservice
- **ID**: `CUSTOMER-MICROSERVICE`
- **URI**: `lb://customer-microservice`
- **Predicado de Ruta**: `/customers/**`

#### Loan Microservice
- **ID**: `LOAN-MICROSERVICE`
- **URI**: `lb://loan-microservice`
- **Predicado de Ruta**: `/credits/**`

#### Account Microservice
- **ID**: `ACCOUNT-MICROSERVICE`
- **URI**: `lb://account-microservice`
- **Predicado de Ruta**: `/accounts/**`

#### Product Microservice
- **ID**: `PRODUCT-MICROSERVICE`
- **URI**: `lb://product-microservice`
- **Predicado de Ruta**: `/products/**`

#### Debit Card Microservice
- **ID**: `DEBIT-CARD-MICROSERVICE`
- **URI**: `lb://debit-card-microservice`
- **Predicado de Ruta**: `/debit-cards/**`

## Acceso al API Gateway

El API Gateway está accesible a través de la siguiente dirección:

[4.152.240.150:8080/](http://4.152.240.150:8080/)

## Integración con Eureka

El API Gateway está configurado para integrarse con el servidor Eureka para el descubrimiento de servicios. Cada microservicio registrado en Eureka puede ser accedido a través del API Gateway utilizando las rutas configuradas.

## Información Adicional

Para más detalles sobre la configuración y uso del API Gateway, revisar el archivo de configuración del proyecto.
