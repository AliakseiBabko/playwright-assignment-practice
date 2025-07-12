# playwright-assignment-practice

This repository is a hands-on practice project designed to prepare for a technical assessment involving API testing, UI automation with the Page Object Model (POM), and BDD integration.

The setup uses **Playwright** for robust end-to-end testing and **Cucumber.js** to implement Behavior-Driven Development (BDD).

***

## 🚀 Core Competencies Covered

1.  **API Testing**: Direct interaction with API endpoints to assert responses, status codes, and data integrity.
2.  **Playwright UI Automation**: Browser automation using modern Playwright features, structured with the **Page Object Model (POM)** for maintainable and scalable test code.
3.  **BDD Integration**: Linking business-readable Gherkin scenarios (`.feature` files) to the underlying Playwright UI code using Cucumber step definitions.

***

## 🛠️ Framework & Technologies

* **Test Runner**: [@playwright/test](https://playwright.dev/)
* **BDD Framework**: [@cucumber/cucumber](https://cucumber.io/)
* **Language**: [TypeScript](https://www.typescriptlang.org/)
* **Package Manager**: [npm](https://www.npmjs.com/)

***

## 📂 Project Structure

The project is organized to clearly separate the different testing concerns, mirroring the structure of a real-world assessment.

```plaintext
/
├── api/                  # Standalone API tests
├── features/             # BDD Gherkin .feature files
├── pages/                # Page Object Models (POMs) for UI automation
├── steps/                # Cucumber step definitions (glue code)
├── support/              # Helper files (e.g., Cucumber world setup)
├── reports/              # Output for test reports
├── .cucumber.js          # Configuration for Cucumber
├── package.json          # Project dependencies and scripts
└── tsconfig.json         # TypeScript configuration
```

***

## ⚙️ Setup and Installation

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    cd playwright-assignment-practice
    ```

2.  **Install dependencies:**
    This command installs Playwright, Cucumber, and all other required packages.
    ```bash
    npm install
    ```

3.  **Install Playwright browsers:**
    This one-time command downloads the browser binaries needed by Playwright.
    ```bash
    npx playwright install
    ```

***

## ▶️ How to Run Tests

This project contains two types of tests.

### 1. Run the BDD Scenarios (UI Tests)

This command executes the Cucumber feature files located in the `/features` directory.

```bash
npm test
```

### 2. Run the Standalone API Tests

To run only the API tests located in the `/api` directory, use the native Playwright test runner.

```bash
npx playwright test --grep @api
```
*(Note: This assumes you have added an `@api` tag to your API test descriptions, which is a good practice for filtering.)*

Or run a specific file:
```bash
npx playwright test api/posts.api.ts
```

***

## 📊 Viewing Reports

After running the tests, HTML reports are generated in the `/reports` directory.

* **BDD/UI Test Report**: Open `reports/cucumber-report.html` in your browser.
* **API Test Report**: If you run Playwright tests directly, a report will be generated in the `playwright-report` folder. Open `playwright-report/index.html` to view it.
