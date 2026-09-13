# CodeAlpha Java + Gradle Application

## Project Overview

This project was completed as part of the CodeAlpha DevOps Internship.

The project demonstrates how a simple Java application can be managed using **Gradle**, including building, testing, packaging, and running the application.

## Technologies Used

* Java JDK 25
* Gradle 9.7.1
* JUnit 5
* Git
* GitHub
* Windows 11

## Project Structure

```text
CodeAlpha-Java-Gradle/
│
├── .gitignore
├── build.gradle
├── settings.gradle
│
└── src/
    ├── main/
    │   └── java/
    │       └── App.java
    │
    └── test/
        └── java/
            └── AppTest.java
```

## Application

The application is a simple Java program that displays:

```text
Hello from CodeAlpha Java + Gradle!
```

The main application is located in:

```text
src/main/java/App.java
```

## Gradle Configuration

The `build.gradle` file configures the project to use the Gradle Application plugin and JUnit for automated testing.

Gradle is used to automate the application's build and testing process.

## Build the Project

To build the application:

```powershell
gradle build
```

A successful build produces:

```text
BUILD SUCCESSFUL
```

## Run the Application

The application can be run through Gradle using:

```powershell
gradle run
```

Expected output:

```text
Hello from CodeAlpha Java + Gradle!
```

## Run Automated Tests

The project uses JUnit for testing.

Run the tests with:

```powershell
gradle test
```

A successful test execution produces:

```text
BUILD SUCCESSFUL
```

Gradle also generates a test report under:

```text
build/reports/tests/test
```

## Create the JAR Package

To create a Java JAR package:

```powershell
gradle clean jar
```

The generated JAR is stored in:

```text
build/libs/
```

## Run the JAR

The packaged application can be executed with:

```powershell
java -jar .\build\libs\CodeAlpha-Java-Gradle.jar
```

Expected output:

```text
Hello from CodeAlpha Java + Gradle!
```

## DevOps Workflow

The project demonstrates the following workflow:

```text
Java Source Code
       ↓
     Gradle
       ↓
    Compile
       ↓
    Testing
       ↓
    Build
       ↓
   JAR Package
       ↓
 Run Application
```

## Troubleshooting

### JAR does not run

If Java reports:

```text
no main manifest attribute
```

the JAR does not contain the application's main class information.

The `build.gradle` file includes the following configuration to specify the main class:

```groovy
jar {
    manifest {
        attributes(
            'Main-Class': 'App'
        )
    }
}
```

After changing the configuration, rebuild the JAR:

```powershell
gradle clean jar
```

Then run it again.

## Git and GitHub

Git is used to track changes to the project, while GitHub is used to store and share the source code remotely.

Generated Gradle files are excluded using `.gitignore`:

```text
.gradle/
build/
```

## Learning Outcomes

Through this project, I learned how to:

* Install and configure Java.
* Install and configure Gradle.
* Create a Java application.
* Configure a Gradle project.
* Build a Java application using Gradle.
* Run automated tests with JUnit.
* Package an application as a JAR.
* Run a packaged Java application.
* Troubleshoot a JAR manifest configuration problem.
* Use Git for version control.
* Upload source code to GitHub.

## Project Status

**Completed:** Java application successfully built, tested, packaged, and executed using Gradle.
