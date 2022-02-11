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

```xml
<?xml version="1.0" encoding="UTF-8"?>
<profiles>
 <profile>
   <id>red-hat-enterprise-maven-repository</id>
   <repositories>
     <repository>
       <id>red-hat-enterprise-maven-repository</id>
       <url>https://maven.repository.redhat.com/ga/</url>
       <releases>
         <enabled>true</enabled>
       </releases>
       <snapshots>
         <enabled>false</enabled>
       </snapshots>
     </repository>
   </repositories>
   <pluginRepositories>
     <pluginRepository>
       <id>red-hat-enterprise-maven-repository</id>
       <url>https://maven.repository.redhat.com/ga/</url>
       <releases>
         <enabled>true</enabled>
       </releases>
       <snapshots>
         <enabled>false</enabled>
       </snapshots>
     </pluginRepository>
   </pluginRepositories>
 </profile>
</profiles>
<activeProfiles>
 <activeProfile>red-hat-enterprise-maven-repository</activeProfile>
</activeProfiles>
```
   
# Links
1. https://access.redhat.com/documentation/en-us/red_hat_build_of_quarkus/2.2/guide/e75e6f99-0d92-4236-bfb8-2de30a6a605d#proc-online-maven_quarkus-getting-started
