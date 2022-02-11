# Steps to migrate Quarkus project to Red Hat build of Quarkus
1. update ```pom.xml``` file:
   ```
   <quarkus.platform.group-id>io.quarkus.platform</quarkus.platform.group-id>
   <quarkus.platform.version>2.7.0.Final</quarkus.platform.version>
    ```
    
    to
    
    ```
    <quarkus.platform.group-id>com.redhat.quarkus.platform</quarkus.platform.group-id>
    <quarkus.platform.version>2.2.3.SP2-redhat-00001</quarkus.platform.version>
    ```
1. update maven's ```settings.xml``` file with:
   ```

   ```
# Links
1. https://access.redhat.com/documentation/en-us/red_hat_build_of_quarkus/2.2/guide/e75e6f99-0d92-4236-bfb8-2de30a6a605d#proc-online-maven_quarkus-getting-started