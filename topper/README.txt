README 
--------

Topper is a webapp to demonstrate a simple spring webmvc application.


Environment
-------------
  * jdk 1.6.0
  * tomcat 6.0 / jetty 6.1 
  * mysql 5.1    
  * eclipse 3.5 (galileo)
  * maven 2.0
  * firefox 3.5  

  
Build
--------
NOTE - The dependencies are pulled from the m2 central repository - http://repo1.maven.org/maven2/. 
Make sure you are connected to the network, when doing the first build.
 
To build the app, use 
$ mvn    

To run the webapp, copy topper.war to webapps folder in tomcat / jetty. 
Else run it using the maven plugin ('mvn tomcat:run' OR 'mvn jetty:run') and 
then point the browser @ http://localhost:8080/topper/
 

Database
----------
The employee data is persisted in mysql database. Setup topper database using 
the script here - src/main/resources/topper.sql . 

For running tests, an H2 embedded DB is used. See the configuration here -
src/test/resources/test-topper-datasource.xml .  


Tomcat
--------
Copy mysql connector (mysql-connector-java-5.1.10.jar) to $TOMCAT_HOME/lib .

Jetty
-------
Copy the below 3 jars to $JETTY_HOME/lib
 * mysql-connector-java-5.1.10-bin.jar
 * commons-dbcp-1.2.2.jar
 * commons-pool-1.5.4.jar
Start Jetty with plusConfig enabled. 

TODO
-----------  
  * Mandatory fields need to be validated in add/edit screen
  * Show search box (by employeeId) in search screen

  
