= A sample To Do web application

This project is a simple, MVC-based task management web application written in Java powered by Spring Boot. Its main purpose is to demonstrate implementation approaches for typical project automation requirements with the help of Gradle.

== Applied Gradle features

* Usage of the Gradle Wrapper.
* Support for a multi-project build.
* Implements various testing strategies:
** Unit testing with Spock.
** Integration testing Spring test utilities.
* Static code analysis with publishing of result to SonarCloud.
* Deployment of the WAR file to Heroku.

== Build pipeline

The project includes a Jenkins pipeline definition file named `Jenkinsfile`. The pipeline consists of the following steps:

1. **Compile source code:** Executes the Java compiler to turn production and test source code into byte code.
2. **Execute unit tests:** Runs the unit test suite for fast feedback.
3. **Execute integration tests:** Performs long-running integration tests.
4. **Perform static code analysis:** Analyzes the source code and identifies quality hotspots. For convenience reasons, the project uses the cloud-based service of Sonarqube.
6. **Assemble the WAR file:** Builds the final deliverable, a WAR file containing all resources needed in the runtime environment.
7. **Deploy the deliverable to production:** Pushes the WAR file to the Paas, Heroku, upon request.

== Running the application

You can directly run your application your local machine. There's no need to install a Servlet container. In a terminal window execute the following command from the root level of the project:

*Mac OS X/*nix*

[source]
----
./gradlew bootRun
----

*Windows*

[source]
----
gradlew.bat bootRun
----

Open your browser of choice and navigate to the URL `http://localhost:8080/`.
