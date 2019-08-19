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

In the Servers view right-click -> New -> Server
Select IBM -> WebSphere Application Server Liberty
Choose Install from an archive or a repository
Enter a destination path (/Users/username/liberty)
Choose WAS Liberty with Java EE 7 Web Profile
Continue the wizard with default options to Finish
Run your application locally on Liberty:
Right click on the JavaHelloWorldApp sample and select Run As -> Run on Server option
Find and select the localhost Liberty server and press Finish
In a few seconds, your application should be running at http://localhost:9080/JavaHelloWorldApp/
Create a Bluemix server definition:
In the Servers view, right-click -> New -> Server
Select IBM -> IBM Bluemix and follow the steps in the wizard.\
Enter your credentials and click Next
Select your org and space and click Finish
Run your application on Bluemix:
Right click on the JavaHelloWorldApp sample and select Run As -> Run on Server option
Find and select the IBM Bluemix and press Finish
A wizard will guide you with the deployment options. Be sure to choose a unique Name for your application
In a few minutes, your application should be running at the URL you chose.
Next Step
Ready to learn how to interact with a database? Check out this Sample and tutorial to help you get started with a Java EE app, REST API and a database.

Liberty App Accelerator
For help generating other Liberty samples checkout the Liberty App Accelerator at wasdev.net/accelerate
