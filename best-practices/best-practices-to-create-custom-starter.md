# Best practices to create custom starter
This best practice guid list some of the best practices to create custome SpringBoot starter.

## Naming
- do not start your module names with **spring-boot**
- name a combined module after the starter, if your are writing for `auth-token`
  - name `auto-configure` module as `auth-token-spring-boot-autoconfigure`
  - name `starter` module as `auth-token-spring-boot-starter`
  - if you only have one module that combines the two, name it `auth-token-spring-boot-starter`


## References
- [Spring Doc Reference](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-features-custom-starter)
