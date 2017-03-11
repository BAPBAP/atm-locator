ATM Locator - HTTP REST API for searching ING bank ATM
=========================================

ATM Locator is an internet portal that acts as an interface to actual locations of ATM belonging to ING bank.
The ATM Loactor exposes: 
* REST API interface for accessing locations of ATM
* Simplified interface for searching and observing ATM near specified location


## How to build and deploy application

The easiest way to build and run the **server** is to use the maven:

    $ mvn install 
    
The command should build war **atm-locator.war**    

### Deployment 

In Tomcat env. it enough if you copy and paste **war** to **webapps** folder in Tomcat. 
When you start Tomcat, the **war** will be automatically deploy with context root   

### Technology stack

Spring 4.3.8
Spring Security 4.3.2
Servlet 3.0
JQuery 1.12.4
Maven 3.0




#### Command Line Using Gradle

The easiest way to run the **server** is to use the [Gradle Jetty Plugin](http://www.gradle.org/docs/current/userguide/jetty_plugin.html).
 Simply execute:

    $ gradlew :http:jettyRun

This command starts a Jetty servlet container running on port 8080 serving the application. 
Alternatively you can also package the war-file and deploy it manually to a servlet container of your choosing. For that to happen execute:

    $ gradlew :http:build

The resulting war-file will be located in the **target** folder.

#### Using an IDE such as SpringSource Tool Suite™ (STS)

If you are using [STS](http://www.springsource.com/developer/sts) and the project is imported as an Eclipse project into your workspace, you can just execute **Run on Server**. This will start the **server** application. 

### Client

#### Command Line Using Gradle

In order to run the **client** using Gradle, execute:

    $ gradlew :http:run

This will package the application and run it using the [Gradle Application Plugin](http://www.gradle.org/docs/current/userguide/application_plugin.html)

#### Using an IDE such as SpringSource Tool Suite™ (STS)

In STS (Eclipse), go to package **org.springframework.integration.samples.http**, right-click **HttpClientDemo** and select **Run as** --> **Java Application**. This will run the **client** application.

### Output
  
The gateway (**client**) initiates a simple request posting "Hello" to the **server** and the **server** responds by appending **from the other side** to the message payload and returns. You should see the following output from the server:
   
    ++++++++++++ Replied with: Hello from the other side ++++++++++++

