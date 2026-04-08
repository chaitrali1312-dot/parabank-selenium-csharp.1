# Parabank Automation Framework (C# + Selenium)

## Description
Automation framework for :contentReference[oaicite:1]{index=1}  
Covers **Login** and **Registration** flows with positive & negative testing.

---

2. Tech Stack
- C# (.NET 6 or above)
- Selenium WebDriver
- NUnit
- ExtentReports
- Chrome browser

---

3. Project Structure
ParabankAutomation/
│
├── Config/ # Config files like appsettings.json
├── Drivers/ # WebDriver setup
├── Pages/ # Page Object Model classes
├── Tests/ # NUnit test classes
├── Utilities/ # Helpers: Wait, Logger, Screenshot, Reports
├── TestData/ # Test data generation
├── Reports/ # HTML test reports
├── Screenshots/ # Screenshots for failed tests
├── README.md
└── TestStrategy.md



4. Configuration

**File:** `Config/appsettings.json`

```json
{
  "BaseUrl": "https://parabank.parasoft.com/",
  "ValidUser": {
    "Username": "john",
    "Password": "demo"
  },
  "Timeout": 10
}

5. Setup Instructions
git clone https://github.com/your-username/parabank-automation.git

dotnet restore

6. Execute test
dotnet test

7. Reports & Logs
ExtentReports: Detailed HTML report with test results, status, and screenshots (Reports/TestReport.html)
Screenshots: Captured automatically in /Screenshots on test failure
Logs: Step-by-step execution logs stored in /Logs/log.txt

8. Automation Features
Page Object Model (POM): Clean separation of UI actions from test code
Explicit waits using WaitHelper for stability
Dynamic test data generation (UserData.cs)
Logging with Logger.cs
Screenshots on failure with ScreenshotHelper.cs
ExtentReports HTML reporting via ReportManager.cs
Parallel execution for faster test runs
Independent tests: no dependencies between tests

