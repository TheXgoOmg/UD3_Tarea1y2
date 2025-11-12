# UD3_Tarea1

Este proyecto trata sobre un programa para mantener una base de datos MySQL, en mi caso llamada 'BMW_Clasicos'.
Teniendo diferentes tipos de relaciones entre las entidades, tanto 1:1, 1:M y N:M.
El objetivo es gestionar las relaciones entre estas entidades y aplicarles correctamente las operaciones CRUD.

## Tecnologías
- *Lenguaje de programación:* Java (JDK 24)
- *ORM:* Hibernate
- *Gestión de persistencia*: JPA (Jakarta Persistence API)
- *Gestor de BD*: MySQL

### Dependencias
| Dependencia | Versión | Descripción |
|-------------|---------|-------------|
| `mysql-connector-j` | 9.4.0 | Conector JDBC apra MySQL |
| `hibernate-core` | 7.1.2 | Implementación de ORM para JPA |
| `jakarta.persistence-api` | 3.2.0 | API estándar de persistencia para Java |
| `logback-classic` | 1.5.19 | Sistema de logging flexible y potente |
| `lombok` | 1.18.42 | Genera código repetitivo (getters, setters, builders, etc.) automáticamente |

## Estructura
El proyecto tiene las siguientes clases relacionadas con la BD:
- `Motor`
- `Chasis`
- `Mecánico`
- `MecanicoMotor`: Se usa como tabla intermedia para la relación N:M entre `Mecánico` y `Motor`
- `idMecanicoMotor`

## Relaciones
Las relaciones entre las entidades son las siguientes:
- `Motor` y `Chasis`: Relación 1:1
- `Chasis` y `Mecanico`: Relación 1:M
- `Motor` y `Mecanico`: Relación N:M

## Funcionalidad

### 1. Operaciones CRUD
Puedes realizar libremente las operaciones CRUD con las siguientes funciones:
- `muestra Mecanico`: Muestra los datos de Mecanico según su ID
- `insertar`: Inserta un nuevo Mecanico a la BD, pide los datos por la consola
- `actualizar`: Actualiza los datos de un Mecanico según su ID, pide los datos por la consola
- `eliminar`: Elimina un Mecanico de la BD según su ID

### 2. Operaciones especiales
Estas son operaciones que solo se realizan con Chasis, para probar el correcto funcionamiento de las relaciones entre entidades:
- `muestra Chasis`: Muestra la información de todos los Chasis de la BD
- `muestra -r Chasis`: Muestra la información de todos los Chasis de la BD de forma recursiva, por lo que muestra los datos de todos los Motores asociados por la relación 1:1 con cada Chasis

## Comienza
1. Clona este repositorio
2. Crea el servicio MySQL y vuelca el archivo 'dumpSQL'
3. Ejecuta el programa y utiliza el comando 'help' para recordar los comandos
