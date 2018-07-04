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

The example in this project has different test data set sources for the data-driven approach:
- xlsx (Excel)
- csv (CSV files with common delimeters)
- datasource (MySQL)
- internal datasource (2-dimension flat file)

In Katalon Studio, data-driven approach happens at TestSuite level so the example contains different test suites for each data set sources.

### Object Repository

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
