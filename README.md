<h1 align="center">CashCard Spring Boot Practice<h1>

<div align="center">
  <img src="https://img.shields.io/badge/spring boot-0D1129.svg?style=for-the-badge&logo=springboot&logoColor=%6DB33F" alt="Spring Boot">
  <img src="https://img.shields.io/badge/junit-BE3939.svg?style=for-the-badge&logo=junit5&logoColor=white" alt="Java">
</div>

# Table of Contents

- [Table of Contents](#table-of-contents)
- [Overview](#overview)
- [Course Outcomes](#course-outcomes)
- [Knowledge Explored](#knowledge-explored)

# Overview

The repo is following the course [Building a REST API with Spring Boot](https://spring.academy/courses/building-a-rest-api-with-spring-boot) to get hands-on practice.

# Course Outcomes

- Build a fully functional `REST API` with Spring Boot.
- Utilize `Spring Security` to authenticate and authorize your application.
- Implement `test-driven development`.
- Convert database and Java objects automatically using `Spring Data JDBC`.

# Knowledge Explored

*As of February 5th, see [Spring.pdf](Spring.pdf) for more details.*

## Concepts

### Main idea

- Context & Dependency Injection
- Database Access
- Spring MVC

### IoC (Inversion of Control)

- Inversion of Control Container
- Providing Dependencies
- Initializer

### API Contracts & JSON

- API Contracts
  - Patterns for API Behavior
  - Consumer & Provider Driven Contracts
- JSON
  - JavaScript Object Notation

### Testing

- Red-Green-Refactor

### REST in Spring Boot

- Spring Beans
- Spring Annotations
- Spring Web Controllers
- Implementing GET
- Implementing POST
  - Idempotence and HTTP
  - Request and Response

### Repositories & Spring Data

- Controller-Repository Architecture
- H2 In-Memory Database
- Spring Data’s CrudRepository

### Security

- Authentication
- Spring Security
  - Filter Chain
- Authorization
  - Role-Based Access Control (RBAC)
- Same Origin Policy
- Cross-Origin Resource Sharing
- Common Web Exploits
  - CSRF & XSS

## Code Analysis

- [Overview](#overview)
- [Course Outcomes](#course-outcomes)
- [Knowledge Explored](#knowledge-explored)
  - [Concepts](#concepts)
  - [Code Analysis](#code-analysis)
    - [Components](#components)
    - [Annotations](#annotations)
  - [File Analysis](#file-analysis)

### Components

#### APP

- `SpringApplication.run(CashCardApplication.class, args);`

#### CRUD

- CrudRepository
- ResponseEntity
- TestRestTemplate
- HttpStatus

#### DATA

- Pageable
- Page<CashCard>
- PageRequest
- Sort

#### TEST

- assertThat

#### UTIL

- URI and UriComponentsBuilder
- Optional
- DocumentContext (JsonPath)
- JacksonTester

### Annotations

#### Class Level

- @SpringBootApplication
- @SpringBootTest(webEnvironment = SpringBootTest.WebEnvironment.RANDOM_PORT)
- @DirtiesContext(classMode = ClassMode.AFTER_EACH_TEST_METHOD)
- @JsonTest
- @RestController
- @RequestMapping("/cashcards")

#### Class Variable

- @Autowired

#### Class Method

- @BeforeEach
- @Test
- @GetMapping("/{requestedId}")
- @PostMapping
- @DirtiesContext

#### Parameter Level

- @PathVariable
- @RequestBody
- @Id

## File Analysis

- [Overview](#overview)
- [Course Outcomes](#course-outcomes)
- [Knowledge Explored](#knowledge-explored)
  - [Concepts](#concepts)
  - [Code Analysis](#code-analysis)
  - [File Analysis](#file-analysis)
    - [build.gradle](#buildgradle)
    - [schema.sql](#schemasql)
    - [data.sql](#datasql)

### build.gradle

- Dependencies for Spring Boot and H2 Database
- Test configurations for more verbose output
- Resource directories for main and test

### schema.sql

- SQL script defining a table `cash_card`

### data.sql

- SQL script inserting data into `cash_card` table
