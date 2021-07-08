# Demo of Spring Cloud Fabric8 Health

### Steps to reproduce

- Startup application
- Go to http://localhost:8080/actualtor/health
- Check presence of "kubernetes" component despite the application.yml configuration: 
  ```
  management:
    health:
      kubernetes:
        enabled: false
  ```

### Dependencies:

```
extra["springCloudVersion"] = "2020.0.3"

dependencies {
  implementation("org.springframework.cloud:spring-cloud-kubernetes-fabric8-config")
}
```    
