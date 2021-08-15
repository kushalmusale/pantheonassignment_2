# Assignment 2: 

### API Under Test: https://api.darksky.net/forecast/{api_key}/latitude,longitude
ex. for Bengaluru https://api.darksky.net/forecast/6508dfe23c140cf146a5ad4c2b233282/12.9716,77.5946

###### Automation framework:

###### Developed hybrid framework (combination of Data driven approach, TestNG framework and POM design pattern) using Selenium automation tool, Java as programming language, RestAssured api and Maven build tool 

### Components of automation framework: 
###### 1. com.pantheon.api.base -> package contains “TestBase.java” class to contains constructor to load properties file
###### 2. com.pantheon.api.config -> package contains properties file (config.properties)
###### 3.com.pantheon.api.util -> package contains “ApiUtil.java” class to check field from JSON object and data size of JSON array
###### 4. com.pantheon.api.client -> package contains “ApiClinet.java” class contains method to send request 
###### 5. com.pantheon.api.test -> package contains “GetAPITest.java” to assert field from JSON object and data size of JSON array


***
### Run Selenium tests scripts from command line: 
1.	Install maven on your machine and set the maven home and path in environment variables
2.	Go to folder where maven is installed in command prompt 
3.	Use “mvn clean install” to generate, compile, and execute the jars files and “mvn test” command to run the test scripts 

***
### Run Selenium tests using Jenkins
1. Download and install jenkins on your system 
2. Open Command prompt and navigate to project home directory and Start Jenkins server
Cmd > Project_home_Directory> java -jar Jenkins.war
Jenkins runs on 8080 port
3. Open any browser and type the URL  http://localhost:8080
4. Configure Jenkins so that Jenkins can identify other tools as well like Java, Maven etc.
5. Click on > Manage Jenkins -> Click on Configure System and add Javan and Maven 

We can execute test cases in Jenkins using 4 ways
1. Execute Windows batch command 
2. Execute shell 
3. Invoke Ant
4. Invoke top level maven targets 

Execute as "Execute Windows batch command" way:
1. Create a batch file add the same batch file to Jenkins
2. Create a job in Jenkins which will execute our build -> Open Jenkins on browser (type http://localhost:8080) -> Click on the new item -> Give the Job-Name, select Build a free-style software project and Click on OK button -> Navigate to Advanced Project Options > Check the use custom workspace > in directory we will specify the project home directory -> Important part now specify the Add Build step >Click on Execute Windows batch command -> In this section please specify the batch file which we created and click on Apply and save
3. you can finally run the Build > Click on Build now  option
4. Check Build history and Console output and verify the output
5. Also Schedule your build in Jenkins for periodic execution
