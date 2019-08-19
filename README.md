Java Hello World Sample
This project contains a simple servlet application.

Deploy to Bluemix

Running the application using the command-line
This project can be built with Apache Maven. The project uses Liberty Maven Plug-in to automatically download and install Liberty from the Liberty repository. Liberty Maven Plug-in is also used to create, configure, and run the application on the Liberty server.

Use the following steps to run the application locally:

Execute full Maven build to create the target/JavaHelloWorldApp.war file:

$ mvn clean install
Download and install Liberty, then use it to run the built application from step 1:

$ mvn liberty:run-server
Once the server is running, the application will be available under http://localhost:9080/JavaHelloWorldApp.

Use the following command to run the built application in Bluemix: bash $ cf push <appname> -p target/JavaHelloWorldApp.war

Developing and Deploying using Eclipse
IBM® Eclipse Tools for Bluemix® provides plug-ins that can be installed into an existing Eclipse environment to assist in integrating the developer's integrated development environment (IDE) with Bluemix.

Download and install IBM Eclipse Tools for Bluemix.

Import this sample into Eclipse using File -> Import -> Maven -> Existing Maven Projects option.

Create a Liberty server definition:

