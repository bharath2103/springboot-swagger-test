# springboot-swagger-test

Springfox is an implementation of swagger-2 Specification
Swagger removes the guess work in calling a service
Using swagger we can automate the documentation of the web service that we have published

Dependencies
<dependency>
<groupId>io.springfox</groupId>
<artifactId>springfox-swagger2</artifactId>
<version>2.4.0</version>
</dependency>

<dependency>
<groupId>io.springfox</groupId>
<artifactId>springfox-swagger-ui</artifactId>
<version>2.4.0</version>
</dependency>

Required:
Controller(REST Endpoint) + SwaggerConfig file

SwaggerConfig File
The Swagger Config file is annotated with @Configuration annotation, so this class will be executed during the application start up itself.

is annotated with @EnableSwagger2

This contains three method

- public Docket postsApi()

          Using the Select method , we will get the APISelectorBuilder instance, in the parameter of the
          APISelectorBuilder Instance we will inject postPaths() method value, which has exposed  API's

- private Predicate<String> postPaths()

          Here we wil define the exposed API's, this method makes the Swagger attach itself to the Rest
          endpoints

- private ApiInfo apiInfo()

          contains the information which will be defines in the swagger UI

Swagger UI
     http://localhost:8080/swagger-ui.html
