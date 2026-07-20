# Software Engineering – Lab 05: Maven Session

Name: H.DS Dinuki  
Student Registration Number:245024G  


## Task Summary

### Maven Hello World
This task covers the fundamentals of Apache Maven as a build automation tool. It includes:
- Creating a new Maven project using `mvn archetype:generate` with the `maven-archetype-quickstart` archetype
- Understanding the standard Maven project structure (`src/main`, `src/test`, `pom.xml`)
- Exploring the `pom.xml` file: project coordinates, properties, dependencies, and build plugins
- Running core Maven lifecycle commands: `mvn compile`, `mvn test`, `mvn package`
- Reading custom properties from `pom.xml` at runtime using Java system properties (`-D` flags)
- Configuring the `maven-jar-plugin` to embed a main class in the JAR manifest, enabling execution via `java -jar`

## How to Build and Run

Clone the repository and navigate into the project folder:

```bash
git clone https://github.com/shehana-dinuki/maven-hello-world.git
cd maven-hello-world
```

Build the project:

```bash
mvn clean package
```

Run the application:

```bash
java -jar target/hello-world-1.0-SNAPSHOT.jar
```

To run with custom properties from `pom.xml`:

```bash
java -Dapp.name=HelloWorldApp -Dapp.version=1.0.0 -jar target/hello-world-1.0-SNAPSHOT.jar
```

Expected output:
```
App Name: HelloWorldApp
App Version: 1.0.0
```