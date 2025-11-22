# kodilla-advanced-tests

![Java](https://img.shields.io/badge/Java-21-blue)
![Gradle](https://img.shields.io/badge/Gradle-8-green)
![JUnit](https://img.shields.io/badge/JUnit-5.9.3-purple)
![Mockito](https://img.shields.io/badge/Mockito-5.3.1-orange)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

## Overview
This project contains exercises and homework tasks completed as part of a module in the **Kodilla "Automated Tester" Java course**, focusing on **Mocking** in Java 21.

The module focuses on:

- Parametrized tests
- Mockito mocks
- Stubbing and verifying interactions
- Execution model testing

The project was developed in **IntelliJ IDEA** as part of the learning path for future **QA/Test Automation Engineers**.

---

## Description
This repository includes **Java 21** code demonstrating practical testing techniques.

### 1. Execution Model
- Modeling orders, items, and invoices
- Implementing a shop with query and filter methods
- Building systematic test cases verifying:
    - Date ranges
    - Order existence
    - Object behaviors

### 2. Mockito
- Creating mocks for interfaces and classes
- Verifying method calls
- Stubbing return values
- Testing notification systems, including:
    - Mobile phone notifications
    - Weather alert system (homework)

### 3. Parametrized Tests
- Using value sources, CSV sources, and method sources
- Building reusable data providers
- Validating:
    - Number properties
    - String transformations
    - User sign-up validation
    - Gambling machine input correctness
    - BMI evaluation from parametrized CSV data

> The module develops strong practical testing skills used in real QA automation workflows.

---

## Project Structure

```
kodilla-advanced-tests/
├── build.gradle
├── gradlew
├── gradlew.bat
├── LICENSE
├── structure.txt
│
├── src/main/java/com/kodilla/
│ ├── Main.java
│ ├── execution_model/
│ │ ├── Invoice.java
│ │ ├── Item.java
│ │ └── homework/
│ │ ├── Order.java
│ │ └── Shop.java
│ ├── mockito/
│ │ ├── Client.java
│ │ ├── MobilePhone.java
│ │ ├── Notification.java
│ │ ├── NotificationService.java
│ │ └── homework/
│ │ ├── Location.java
│ │ ├── Notification.java
│ │ ├── User.java
│ │ └── WeatherNotificationService.java
│ └── parametrized_tests/
│ ├── NumberChecker.java
│ ├── StringManipulator.java
│ ├── StringValidator.java
│ └── homework/
│ ├── GamblingMachine.java
│ ├── InvalidNumbersException.java
│ ├── Person.java
│ └── UserValidator.java
└── src/test/java/com/kodilla/
├── execution_model/
│ ├── InvoiceTestSuite.java
│ └── homework/ShopTestSuite.java
├── mockito/
│ ├── MobilePhoneTestSuite.java
│ ├── NotificationServiceTestSuite.java
│ └── homework/WeatherNotificationServiceTestSuite.java
└── parametrized_tests/
├── NumberCheckerTestSuite.java
├── StringManipulatorTestSuite.java
├── StringSources.java
├── StringValidatorTestSuite.java
└── homework/
├── GamblingMachineTestSuite.java
├── PersonBMISources.java
├── PersonTestSuite.java
└── UserValidatorTestSuite.java
```
---

## Getting Started

### Dependencies

This project uses **JUnit 5.9.3**, **Mockito 5.3.1**, and the **Java plugin**.

**From `build.gradle`:**
```groovy
plugins {
    id 'java'
}

group = 'com.kodilla'
version = '1.0-SNAPSHOT'

repositories {
    mavenCentral()
}

dependencies {
    testImplementation 'org.junit.jupiter:junit-jupiter-api:5.9.3'
    testImplementation 'org.junit.jupiter:junit-jupiter-params:5.9.3'
    testImplementation 'org.mockito:mockito-core:5.3.1'
    testRuntimeOnly 'org.junit.jupiter:junit-jupiter-engine:5.9.3'
}

test {
    useJUnitPlatform()
}
```
## Test Suites Overview

### Execution Model Tests
These tests validate the core shop and order logic:

- **Item and invoice behavior** – ensures correct calculations and object properties
- **Order filtration** – verifies filtering methods work as expected
- **Shop logic correctness** – checks the functionality of query and filter methods
- **Date ranges and totals** – ensures correct handling of dates, totals, and order existence

### Mockito Tests
These tests focus on **interaction-based testing** with mocks and stubs:

- **Verifying notification sending** – checks if notifications are properly triggered
- **Stubbing and mocking client devices** – simulates client behavior without real objects
- **Testing weather alert service recipients** – ensures notifications are sent to correct users

> These tests ensure correct control flow and interaction with dependencies.

### Parametrized Tests
These tests cover **reusable test data and multiple scenarios**:

- **Numeric cases** – checks number validation and calculations
- **String formatting rules** – tests string transformations and manipulations
- **User input validation** – validates sign-up forms and user data
- **Gambling machine rules** – ensures correct behavior based on input
- **BMI classification tests** – evaluates BMI from parametrized CSV data

> Builds extensive familiarity with **JUnit 5 parametrized testing**.


---

## Optional Terminal Commands

**Build project:**

```bash
./gradlew build
```

**Run all tests:**

```bash
./gradlew test
```

**Clean project:**

```bash
./gradlew clean
```

---

## Authors

Created by:

**Joanna Kamińska**  
GitHub: https://github.com/joanna-kaminska-qa

---

## Version History

- **0.2** – README added, structural improvements
- **0.1** – Initial upload

---

## License

This project is licensed under the **MIT License**.  
See the `LICENSE` file for details.

---

## Acknowledgments

- Kodilla Automated Tester Java course
- Mockito documentation 
- JUnit 5 parameterized test docs 
- Java documentation