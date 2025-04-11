# Saucelabs Automation

Saucelabs Automation is an automated testing project aimed at validating the functionality of the SauceDemo application—a sample e-commerce site at Saucelabs. 
The project leverages Java, Cucumber (with Gherkin), and Maven to write clear, reusable, and maintainable BDD tests. The development environment is IntelliJ IDEA 2024.2.4.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Tests](#running-the-tests)
- [How to push to Git repository](#how-to-push-to-git-repository)
- [Configuration](#configuration)


---

## Project Overview

The Saucelabs Automation project automates the testing of the SauceDemo application. It:
- Uses Java for automation logic.
- Implements BDD tests written in Cucumber with Gherkin syntax to ensure scenarios are easy to read and understand.
- Manages project dependencies using Maven.
- Integrates with Sauce Labs to perform cross-browser testing.

The focus of this project is to deliver readable, maintainable, and reusable tests that can easily be extended to cover additional features and use cases.

---

## Prerequisites

Before you can run the project, ensure that you have the following software installed:

- **IntelliJ IDEA 2024.2.4** – or your preferred Java IDE.
- **Java JDK 8 or higher**
- **Maven** – for dependency management and build automation.
- **Cucumber for Java** – the testing framework for BDD.
- **Gherkin** – for writing the test scenarios in a natural language format.
-  Web drivers corresponding to browsers you wish to automate (e.g., ChromeDriver for Google Chrome).

---

## Installation

1. **Clone the Repository:**

   ```bash
   git clone https://your-repository-url/saucelabs-automation.git
   cd saucelabs-automation

## Running the tests
 1) Run the test by using TestRunner in runners package.
 2) Goto feature file and Run specific test that is required.
 3) Run using maven commands.

   ```bash
    # To run whole project
      mvn test 
    # single tag
      mvn "-Dcucumber.options=--tags @login --features src/test/resources/features/login.feature" test 
  ```

## How to push to Git repository

   ```bash
   git add .
   git commit -m "commit message"
   git push -u origin master 
```


## configuration

log4j.properties: Ensure that your logging configuration is correctly set up. 
For immediate log flushing and proper log grouping, confirm that ImmediateFlush is enabled.

Browser Configuration: The project reads the browser type from properties. 
Update your properties file (or the Configuration class) with the desired browser (e.g., Chrome, Firefox).

