# Katalon Studio Samples: Data Driven Tests
Katalon Studio is a free and easy-to-use automated functional and regression testing platform. It provides users the ability to implement full automated testing solutions for their application projects with minimal engineering and programming skill requirements.
______
The **data-driven-tests** demonstrates how to apply data-driven in automation testing with Katalon Studio.

## Getting Started
These instructions will get you a copy of the project up and running on your local machine.
### Prerequisites
- [Katalon Studio](https://www.katalon.com/) - [Installation and Setup](https://docs.katalon.com/x/HwAM)
- Internet access
- Application Under Test (AUT):
     + Jira cloud: https://katalon.atlassian.net/
     + Account: demo@katalon.com/8eml3nBz19rJ6kP8oCYK
- [MySQL](https://dev.mysql.com/)    

#### MySQL
- User: demouser/demouser@2018
- Database: jira_test
	- Table: accounts
```
	CREATE TABLE `jira_test`.`accounts` (
	  `id` INT NOT NULL AUTO_INCREMENT,
	  `username` VARCHAR(45) NULL,
	  `password` VARCHAR(45) NULL,
	  `status` VARCHAR(45) NULL,
	  PRIMARY KEY (`id`),
	  UNIQUE INDEX `id_UNIQUE` (`id` ASC));
	  
	INSERT INTO `jira_test`.`accounts` (`username`, `password`, `status`) VALUES ('demo@katalon.com', '8eml3nBz19rJ6kP8oCYK', 'active');
	INSERT INTO `jira_test`.`accounts` (`username`, `password`, `status`) VALUES ('tom@katalon.com', '1QpnA1G2cOTSJQLE4U3A', 'active');
	INSERT INTO `jira_test`.`accounts` (`username`, `password`, `status`) VALUES ('jerry@katalon.com', 'K@tAl0n@#1304', 'inactive');
	INSERT INTO `jira_test`.`accounts` (`username`, `password`, `status`) VALUES ('bella@katalon.com', 'jira@2018', 'invalid');

```
#### Excel
- Sheet: valid_accounts
```
	Username	        Password
	demo@katalon.com	8eml3nBz19rJ6kP8oCYK
	tom@katalon.com	        1QpnA1G2cOTSJQLE4U3A
```
- Sheet: invalid_accounts
```
	Username	        Password
	jerry@katalon.com	K@tAl0n@#1304
	bella@katalon.com	jira@2018
```
#### CSV
- Comma delimeter
```
	Username,Password
	demo@katalon.com,8eml3nBz19rJ6kP8oCYK
	tom@katalon.com,1QpnA1G2cOTSJQLE4U3A
```
### Setting Up
- [Check out](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository) the code from this repository
- [Open the project](https://docs.katalon.com//display/KD/Manage+Test+Project) from Katalon Studio

### Executing a Test Case
![Execute a simple test case](https://github.com/katalon-studio-samples/data-driven-tests/blob/master/Tutorials/Figures/Execute%20a%20test%20suite%20with%20data%20driven.png?raw=true)
1. The test case that is parameterized to support data-driven test
2. The test suite contains the test case under test
3. Data files created with different data souces
4. The test case selected in the test suite
5. Data file selected for the test case
6. Data binding between the data file and the test case parameters

At the end of this README, you will find additional ways to execute automation test cases. 

## Test Scenarios
Below is the list of all the available test cases in this project relating to the test scenarios as described. Simply select the test case you want to run in Katalon Studio and execute accordingly. You can also make additional changes in these test cases to get familiar with automation testing and specifically Katalon Studio. 
### Story: Login feature
```Gherkin     
     User story
         As a Jira user, I would like to be able to login the Jira system, so that I could manage Jira tickets.
 
         Scenario Outline: Login successfully
           Given The Login page is loaded successfully
           When I login the system with valid <username> and <password>
           Then The Dashboard Page is loaded successfully
         
         Examples:
          | username     | password  |
          |	tom      | jira@2018 |
          |	jerry    | jira@2019 |
 ```         
The example in this project has different test data set sources for the data-driven approach:
- xlsx (Excel)
- csv (CSV files with common delimeters)
- datasource (MySQL)
- internal datasource (2-dimension flat file)

In Katalon Studio, data-driven approach happens at TestSuite level so the example contains different test suites for each data set sources
