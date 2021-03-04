# DataDrivenTestAutomation
Production ready data driven test automation based on TestNG and Selenium Java
### I would love to show you the framework in detail. Please contact me for a demo.

# Test automation framework that contains UI and API tests
This framework is a hybrid test automation framework that contains both UI and API test cases. It puts emphasis on easy test development 
by abstracting all of the low-level Selenium codes into a single class called UIActions. This allows novice testers to be able to start automating test
cases without in-depth knowledge of Selenium.

### Dependencies 
This automation framework depends on following 
external libraries. 
* **rest-assured**: for sending API requests and processing API response.
* **selenium-java**: for browser automation through Java code.
* **webdrivermanager**:  for managing webdriver executable files through Java code.
* **testng**: for representing, organizing and managing test cases through Java code.
* **extentreports**: for generating HTML reports.
* **json-path**: for extracting data from the JSON format.
* **javafaker**: for generating randomized test data on the fly.

### Framework Project Structure Diagram
```
|-data                           #  all test data is stored here
|-images                         #  all images are stored here
|-reports                        #  all the generated test execution reports are here 
|-src
   |---test
         |----java               #  all the java source files needs to stored in this folder 
                |-[+]base        #  java class package, all the base classes will be stored here
                |-[+]pages       #  all the page object classes will be stored here
                |-[+]testcase    #  java class package, all test classes will be stored here 
                |-[+]utility     #  java class package, all the utility classes will be stored here  
|-.gitignore                     #  git ignore config file 
|-pom.xml                        #  project object model file for the maven software
|-READMD.md                      #  you are currently viewing this file 
|-testNG.xml                     #  TestNG configuration files for the test structures and groupings 
```

![screenshot](/images/datadrivenscreenshot.png)

## Pre-requisites
* Download and install Chrome or Firefox browser  ( viewing report )
* Download and install JDK v1.8 + 
* Download and install Apache Maven v3.0+
* Download and install Git v2.0+ 

## Inner Works of the Framework 
This is a diagram that details the internal structure of the framework.  Multiple parts of the
code work together to bring successful automated test executions.
![screenshot](/images/frameworkinternalstructure.png)

## Set-up Instructions 
This framework contains multiple test contexts such as smoke, regression, e2e etc. in CI pipeline. 
Please refer to the following diagram for recommended test triggering points.
![screenshot](/images/utilization.png)


## How to run Tests 
All the test triggering is done through maven commands, this framework supports multiple different types of 
test executions such as smoke, regression, and end-to-end on different possible environment such as QA, Staging, and 
UAT. 
Please download the project, and using command line or terminal to navigate to the root directory of
this project. Once you are in the root directory, please execute one of the following commands.

#### Executing specific tests 
If you would like to execute a specific test which is stated on testNG.xml file
Choose from the following command: 

For invoking UI Smoke Test
```shell script
mvn test -Dtestof="UISmokeTest"
```
For invoking API Smoke Test
```shell script
mvn test -Dtestof="APISmokeTest"
```


## How to view the report
All the test execution reports are available as an HTML report on following folder after test execution.
Please navigate to this report file and open the report with your preferred browser.
```
 report
   |--[HTML] reports
```
![screenshot](/images/reportscreencapture.png)


