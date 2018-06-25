# katalon-studio-samples
## DATA DRIVEN TESTS
The **data-driven-tests** is a testing project with examples of performing functional automation test on JIRA Web Application using Katalon Studio with Data driven approaches. The examples in this project are various from simple to advance tests:

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

- [Katalon Studio](https://www.katalon.com/)
- Permission access to [Jira System](https://katalon.atlassian.net) (provided in the sample code)
- [MySQL](https://dev.mysql.com/)


### Installing
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

A step by step series of examples that tell you have to get a development env running

```
Step 1:
	- Check out the code from this .git

Step 2:
	- Open Katalon Studio
	- Open the project from Katalon Studio

Step 3:
	- Update configuration for integration: Jira, Katalon Analytics
```

## Running the tests

Explain how to run the automated tests for this system
The example in this project has different test data set sources for the data-driven approach:
- xlsx (Excel)
- csv (CSV files with common delimeters)
- datasource (MySQL)
- internal datasource (2-dimension flat file)
In Katalon Studio, data-driven approach happens at TestSuite level so the example contains different test suites for each data set sources.

Test cases at this section help users understanding:
- How to create RESTful Web services object at Object Repository with parameters so that it can be tested with different data set using data-driven approach
- How to create test cases that can be reused in different test scenario
- How to create test cases with BDD mindset
- How to use built-in keywords together with extended scripts such as assertj to verify the response information.
- How to group API end-points

### Object Repository
Webservice Object at the Object Repository can be executed with its hard coding test data. Those object having test data as parameters cannot be executed correctly.

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

## Contributing

## Versioning

## Authors

## License

## Acknowledgments
