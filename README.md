# MetaweatherAPI

This project contains cucumber-based automation framework for testing Metaweather API built on Java.

# Getting Started

## Prerequisites

•	IDE : Eclipse

•	Java 12 (make sure Java class path is set)

•	Maven Setup (make sure maven class path is set)

## Installing

The maven project can be cloned using Url : https://github.com/tejalnaik10/MetaweatherAPI.git

## Running the tests

There are 2 ways to run the test-
1.	Right click on ‘TestRunner.java’ in ‘src\test\java\runners\’ and run as Junit Test
2.	Right click on ‘MetaweatherApi.feature’ and run as Cucumber Feature

## Dependencies
1. Cucumber
2. Junit/testing
3. Rest-assured
4. Extent report

## Built With
•	Eclipse Photon - IDE

•	Maven - Dependency Management

•	Cucumber – BDD technique

•	Junit/Testng – Unit test Framework

# Assumptions and Project details
1.	MetaweatherAPI is a Maven project based on Java. The automation framework utilises BDD technique – Cucumber and Rest-assured to test Metaweather API. 

2.	‘MetaweatherApi.feature’ has test scenarios for the weather in London using methods -  ‘Location’, ‘Location Search’ and ‘Location Day’.

3.	The expected values for the weather forecast are as per the requirements which might fail the assertion step as the actual may not match with expected values:

•	Today: Heavy Cloud 

•	Tomorrow: Showers

•	Tomorrow +1: Clear

•	Tomrrow+2 : Light Cloud

4.	I have created the code in a manner that each API call response could be utilised entirely and each aspect of the response was tested per scenario which includes –

•	Response code

•	Response status

•	Response body – Weather state

•	Response body – 5 day forecast

•	Response time (Assuming response time is less than 3 seconds for the test)
 
5.	The test produces a report after running the feature file with all the scenarios with ‘@automation ’ tag and is stored in ‘output’ folder. The report displays detailed summary of the test run and graphical statistics of all the scenarios executed. This is achieved using extent report plugins.

6.	The ‘StepDefinition.java’ holds the gluecode which links all the matching steps in the feature file while execution.

7.	The Stepdefinitions can be made even more resusable so that they can be used against any rest api

8. 6 test scenarios have been added in the feature file – 3 automated with tag @automation and 3 manual with tag @manual. However, many more test cases can be added for the APIs.
