# Python Playwright Base Project

## Project Architecture

This project uses Python and Playwright for automating web application tests. The project structure is organized as follows:

**Inside Pytest:**
- **specs/**: Contains automated test cases.
- **pages/**: Contains page objects.
- **clients/**: Contains API clients.
- **examples/**: Contains variations for parametrized tests
- **Mocks/**: Contains mocks to be used on tests.
- **support/**: Contains utilities and helper functions.
- **reports/**: Contains test execution reports.


## Setting Up Your Machine

### Required Installations:

- **Python 3**: Programming language used in the tests.
- **Playwright**: Browser automation tool.
- **Node.js**: Required for Playwright.
- **Cmder for Windows**: Provides bash functionalities (Terminal) for Windows.

## Configuring the Test Automation Environment

To perform automation, you need to install some resources as described below:

### Windows

#### 1. Installing Cmder Console

- Download from: [Cmder Release](https://github.com/cmderdev/cmder/releases/download/v1.3.14/cmder.zip)
- Unzip to the C:\Cmder folder
- Select cmder.exe and drag it to your Windows taskbar to create a shortcut
- Run cmder.exe

#### 2. Installing Python 3

- Download from: [Python Downloads](https://www.python.org/downloads/)
- Run the downloaded file and follow the instructions by clicking 'next'
- Select the 3 checkboxes shown and continue clicking 'next' until 'finish'
- In the Cmder Console, type the command `python --version`, if the installation is correct, the installed version will appear

#### 3. Installing Node.js

- Download from: [Node.js Downloads](https://nodejs.org/en/download/)
- Run the downloaded file and follow the instructions by clicking 'next' until 'finish'
- In the Cmder Console, type the command `node --version`, if the installation is correct, the installed version will appear

#### 4. Installing Playwright

After installing Node.js, within Cmder type:
bash
npm install -D @playwright/test
npx playwright install




#### 5. Configuring the Project
In the project directory, create a pytest.ini file with the following content:

ini
[pytest]
addopts = "-v --alluredir=./reports/allure-results --clean-alluredir --reruns 2"
filterwarnings = ['ignore::UserWarning']

- Test Automation
We will use Playwright for test automation.

- Project Structure
tests/: Contains automated test cases.

pages/: Contains page objects.

utils/: Contains utilities and helper functions.

reports/: Contains test execution reports.

- Using Tags
We use tags to differentiate scenarios by groups, functionalities, or test stages. Tags are inserted in the line below the function name. In the terminal, to run scenarios named with tags, use the following command:

bash
pytest -m tag_name
Running Automated Tests
To run automated tests, use the following commands from the root folder of our project.

- To run all implemented scenarios, use the following code:

bash
pytest ./tests/
To run all scenarios and generate a report with screenshots, use the following code:

bash
