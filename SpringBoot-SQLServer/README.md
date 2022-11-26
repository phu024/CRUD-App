# Overview of Spring Boot + SQL Server example
We will build a Spring Boot CRUD Rest Apis using Spring Data JPA with SQL Server (MSSQL) Database for a Tutorial application in that:
- Each Tutotial has id, title, description, published status.
- Apis help to create, retrieve, update, delete Tutorials.
- Apis also support custom finder methods such as find by published status or by title.

These are APIs that we need to provide:
`URL : http://localhost:8080`
| Methods | Urls | Actions |
| ------- | ---- | ------- |
POST | /api/tutorials | create new Tutorial
GET | /api/tutorials | retrieve all Tutorials
GET | /api/tutorials/:id | retrieve a Tutorial by :id
PUT | /api/tutorials/:id |update a Tutorial by :id
DELETE | /api/tutorials/:id | delete a Tutorial by :id
DELETE | /api/tutorials | delete all Tutorials
GET | /api/tutorials/published | find all published Tutorials
GET | /api/tutorials?title=[keyword] | find all Tutorials which title contains keyword

– We make CRUD operations & finder methods with Spring Data JPA’s JpaRepository.
– The database will be SQL Server (MSSQL) by configuring project dependency & datasource.

## Two ways we can start the standalone Spring boot application.
> 1. From the root directory of the application and type the following command to run it -
`$ mvn spring-boot:run`
> 2. From your IDE, run the SpringBootSqlServerApplication.main() method as a standalone Java class that will start the embedded Tomcat server on port 8080 and point the browser to http://localhost:8080/.
