# Spring Boot - error with Spring Security argument resolvers

This is a minimal project to demonstrate error that occurs when using Spring Security together
with Spring Data.

The cause of this issue is [DATACMNS-776](https://jira.spring.io/browse/DATACMNS-776). This project
demonstrates the problem with Spring Security's `@AuthenticationPrincipal` annotated `UserDetails`
argument and `CsrfToken` argument.

To demonstrate the issue, build and start the application, and log in using username `user` and
password `password`. Once logged in, navigate to `/principal` and `/csrf` endpoints.

If the project is build with `org.springframework.boot:spring-boot-starter-data-jpa` dependency
commented out from the build script, the endpoints work as expected.
