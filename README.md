# AccountProject

A simple Java-based GUI application for creating a new account with input validation and automated testing using JUnit. This project uses **Java Swing** for the user interface and **GitHub Actions** for Continuous Integration (CI).

## 📋 Features

- ✅ Form validation for:
  - First Name and Last Name (only letters, minimum 2 characters)
  - Email format (e.g., user@example.com)
  - Password and Confirm Password (minimum 6 characters, must match)
  - Date of Birth (format: dd/mm/yyyy)
- ✅ Responsive and user-friendly Swing interface
- ✅ Real-time feedback on form submission
- ✅ Unit tests using JUnit 5
- ✅ GitHub Actions CI workflow for automatic compilation and test execution

## 🗂️ Project Structure

```

AccountProject/
│
├── .github/workflows/
│   └── test.yml              # GitHub Actions workflow for CI
│
├── lib/
│   └── junit-platform-console-standalone-1.9.0.jar  # JUnit 5 runner
│
├── src/
│   ├── Account.java          # Validation logic
│   ├── AccountForm.java      # Swing UI
│   └── AccountTest.java      # Unit tests
│
└── images/
    └── screenshot.png
````

## 🚀 Getting Started

### Prerequisites

- Java 17 or above
- Git
- (Optional) An IDE like IntelliJ IDEA or Eclipse

### Running the Application

To launch the GUI form:

```bash
javac -d bin src/Account.java src/AccountForm.java
java -cp bin AccountForm
````

### Running Tests Manually

```bash
javac -d bin -cp "lib/junit-platform-console-standalone-1.9.0.jar" src/*.java
java -jar lib/junit-platform-console-standalone-1.9.0.jar --classpath bin --select-class AccountTest
```

## 🔁 CI/CD with GitHub Actions

Every `push` and `pull_request` triggers the GitHub Actions workflow defined in `.github/workflows/test.yml`. The workflow:

1. Checks out the repository
2. Sets up Java 17
3. Compiles the source files
4. Runs the JUnit tests using the JUnit Console Launcher

## 📷 Screenshots

Here is a screenshot of the account creation form:

![Account Form Screenshot](images/screenshot.png)

## 📄 License

This project is licensed under the MIT License - feel free to use, modify, and distribute.


