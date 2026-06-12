# 🛍️ DemoWebShop UI Test Automation Project

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=java)
![Selenium](https://img.shields.io/badge/Selenium-4.x-green?style=for-the-badge&logo=selenium)
![Maven](https://img.shields.io/badge/Maven-3.2.5+-blue?style=for-the-badge&logo=apache-maven)

**Automated GUI Testing Framework for Tricentis DemoWebShop E-Commerce Platform**

[Target Site](https://demowebshop.tricentis.com/)

## 📋 About The Project

This repository contains a robust GUI test automation framework developed for the [Tricentis DemoWebShop](https://demowebshop.tricentis.com/) e-commerce platform. Built with **Java** and **Selenium WebDriver**, the framework focuses on validating critical user journey checkpoints—from registration and negative authentication limits to multi-layered search algorithms, catalog specification checks, and end-to-end checkout cycles.

### ✨ Key Features

- ✅ **User-Story Driven Architecture:** Test scripts directly aligned and validated against production execution patterns.
- ✅ **Compact Package Design:** Elements repositories and execution scripts are maintained side-by-side within a single functional package for high cohesion.
- ✅ **Dynamic UI Syncing:** Explicit wait parameters integrated natively inside the baseline `Parent.java` model to handle asynchronous loaders smoothly.
- ✅ **Robust Boundary Testing:** Detailed validation coverage for edge cases, including duplicated identity forms and corrupted promotional fields.

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|:-----------|:--------|:--------|
| **Java** | 21 | Programming Language |
| **Selenium WebDriver** | 4.x | Browser Automation |
| **Maven** | 3.2.5+ | Dependency and Build Lifecycle Management |

## 📝 Test Scenarios (User Stories)

The project executes 9 business-critical automation scenarios structured exactly according to the code definitions:

| ID | User Story / Test Script Class | Description |
|:---|:-----------|:------------|
| 🔑 **US_201** | `US201_Register_User` | Validates a successful user sign-up flow across mandatory demographic and credential fields. |
| ❌ **US_202** | `US202_Negative_Register_User` | Tests duplicate data constraints by asserting that trying to re-register with an existing email address triggers validation errors. |
| 🔓 **US_203** | `US203_Login` | Verifies secure session establishment for a valid registered entity, ensuring profile link persistence. |
| 🔍 **US_204** | `US204_Search_Order` | Tests the platform search index accuracy and item verification against target catalog keywords. |
| 🛒 **US_205** | `US205_Product_Check_Under` | Controls internal product specifications, catalog data mapping, and item card integrity checks. |
| 💳 **US_206** | `US206_Check_Out_Order` | Simulates a positive end-to-end purchasing route with billing, shipping, and order validation steps. |
| ⚠️ **US_207** | `US207_Negative_Check_Out` | Negative checkout boundary validations handling empty profile inputs and missing verification steps. |
| 🎟️ **US_208** | `US208_Negative_Gift_Cards_and_Cupons` | Validates robust UI error tooltip handling when supplying invalid inputs to gift cards and coupon promotion fields. |
| 📦 **US_209** | `US209_History_Orders` | Navigates the active user account dashboard to cross-check transactional order logs and account history. |

## 📁 Project Structure

```text
DemoWebShop_Automation/
│
├── 📄 pom.xml                          # Maven configuration
├── 📄 README.md                        # Framework documentation
└── src/
    └── test/
        └── java/
            ├── _DemoWebShop_/          # Core Automation Architecture (Tests & Elements)
            │   ├── Parent.java
            │   ├── US201_Elements.java
            │   ├── US201_Register_User.java
            │   ├── US202_Elements.java
            │   ├── US202_Negative_Register_User.java
            │   ├── US203_Elements.java
            │   ├── US203_Login.java
            │   ├── US204_Elements.java
            │   ├── US204_Search_Order.java
            │   ├── US205_Elements.java
            │   ├── US205_Product_Check_Under.java
            │   ├── US206_Check_Out_Order.java
            │   ├── US206_Elements.java
            │   ├── US207_Elements.java
            │   ├── US207_Negative_Check_Out.java
            │   ├── US208_Elements.java
            │   ├── US208_Negative_Gift_Cards_and_Cupons.java
            │   ├── US209_Elements.java
            │   └── US209_History_Orders.java
            │
            └── utility/                # Core Execution Engine Components
                ├── BaseDriver.java
                └── ConfigReader.java
