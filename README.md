# ContactsManagerSolution

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Build Status](https://img.shields.io/github/actions/workflow/status/yamenArmeet/ContactsManagerSolution/dotnet.yml?branch=main)](https://github.com/yamenArmeet/ContactsManagerSolution/actions)
[![.NET](https://img.shields.io/badge/.NET-6%2B-blue)](https://dotnet.microsoft.com)

A modular, clean-architecture contacts management solution built in .NET. This project demonstrates layered separation, dependency injection, and test coverage, enabling you to manage contacts (CRUD) in a robust and maintainable way.

---

## 📌 Table of Contents

1. [Features](#features)
2. [Architecture](#architecture)
3. [Getting Started](#getting-started)

   * [Prerequisites](#prerequisites)
   * [Installation](#installation)
   * [Configuration](#configuration)
   * [Run the Project](#run-the-project)
4. [Testing](#testing)
5. [Usage](#usage)
6. [Project Structure](#project-structure)
7. [Technologies & Tools](#technologies--tools)
8. [Contributing](#contributing)
9. [License](#license)
10. [Contact](#contact)

---

## 🚀 Features

* Create, Read, Update, Delete (CRUD) for contacts
* Validation and business rules handled in service layer
* Repository / data access abstraction
* Unit tests and integration tests
* Clean architecture (Core / Infrastructure / UI / Tests)
* Easy to extend (e.g., add UI, API, alternate storage)

---

## 🏗 Architecture

The solution uses a layered architecture to separate concerns:

* **Core** — Domain models, interfaces, business logic contracts
* **Infrastructure** — Implementations of repositories / data persistence
* **UI** — The user interface (or entry point)
* **Tests** — Unit and integration tests

Dependency inversion is applied: higher-level layers depend on abstractions in Core, not concrete implementations.

---

## 🛠 Getting Started

### Prerequisites

* .NET SDK (6.0 or newer)
* IDE (Visual Studio / VS Code / Rider)
* Git

### Installation

```bash
git clone https://github.com/yamenArmeet/ContactsManagerSolution.git
cd ContactsManagerSolution
dotnet restore
dotnet build
```

### Configuration

If your Infrastructure layer uses a database (e.g., SQL Server, SQLite), update connection strings (e.g., in `appsettings.json` or environment variables) as needed. Run migrations if applicable:

```bash
dotnet ef database update --project ContactsManager.Infrastructure
```

*(Skip if using in-memory or file-based storage.)*

### Run the Project

Launch the UI (or whatever your front-end is). For example:

```bash
dotnet run --project ContactsManager.UI
```

Or open the solution in Visual Studio, set the UI or startup project, and run (F5).

---

## ✅ Testing

Run all tests with:

```bash
dotnet test
```

You can also run individual test projects, for example:

```bash
dotnet test ContactsManager.ServiceTests
dotnet test ContactsManager.IntegrationTests
```

Ensure all tests pass before merging changes.

---

## 📋 Usage

1. Launch the UI or API interface.
2. Use the “Add Contact” form to create a new contact (name, phone, email, etc.).
3. View the contact list.
4. Edit or delete contacts as needed.
5. Optionally, add filters, search, validations, etc.

You can enhance this section with screenshots or sample API endpoints once your UI or API is in place.

---

## 💾 Project Structure

```
ContactsManagerSolution/
├── ContactsManager.Core/             # Domain models, interfaces, business logic contracts  
├── ContactsManager.Infrastructure/   # Data persistence, repository implementations  
├── ContactsManager.UI/               # UI or entry-point (console, GUI, API)  
├── ContactsManager.ServiceTests/     # Unit tests for service/business logic  
├── ContactsManager.ControllerTests/  # (If present) tests for controllers / API  
├── ContactsManager.IntegrationTests/ # Integration / end-to-end tests  
└── ContactsManagerSolution.sln       # Solution file  
```

---

## 🧰 Technologies & Tools

* **C# / .NET 6+**
* (If applicable) **Entity Framework Core**
* xUnit / NUnit / MSTest (depending on your test framework)
* Dependency Injection
* Clean Architecture / Onion Architecture principles
* (Optional) AutoMapper, FluentValidation, Logging frameworks

---

## 🤝 Contributing

We welcome contributions! To contribute:

1. Fork the repository
2. Create a feature branch:

```bash
git checkout -b feature/YourFeatureName
```

3. Implement your changes, adhering to existing styles and architecture
4. Write tests for new features or fixes
5. Run all tests locally
6. Commit with descriptive messages
7. Create a Pull Request (PR)

Please ensure your PR passes all tests and follows code review guidelines.

---

## 🪪 License

This project is licensed under the **MIT License**.
See the [LICENSE](LICENSE) file for details.

---

## 📬 Contact

**Yamen Armeet**
GitHub: [yamenArmeet](https://github.com/yamenArmeet)
Email: [yamen.nasri.armeet@gmail.com](mailto:yamen.nasri.armeet@gmail.com)
LinkedIn / Website: (optional)

---

*Thank you for using or contributing to ContactsManagerSolution!*
