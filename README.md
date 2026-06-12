# 🛍️ DemoWebShop UI Test Automation Project

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=java)
![Selenium](https://img.shields.io/badge/Selenium-4.x-green?style=for-the-badge&logo=selenium)
![Maven](https://img.shields.io/badge/Maven-3.2.5+-blue?style=for-the-badge&logo=apache-maven)

**Automated GUI Testing Framework for Tricentis DemoWebShop E-Commerce Platform**

[Target Site](https://demowebshop.tricentis.com/)

## 📋 About The Project

This repository contains a professional GUI test automation framework designed for the [Tricentis DemoWebShop](https://demowebshop.tricentis.com/) e-commerce platform. Built utilizing **Java** and **Selenium WebDriver**, the framework rigorously executes automated scripts for core retail features, encompassing positive/negative user registrations, shopping cart calculations, checkout workflows, and downstream document generation.

### ✨ Key Features

- ✅ **Specification-Driven Coverage:** Comprehensive test mapping derived from functional user stories and acceptance criteria.
- ✅ **Negative Boundary Testing:** Strict verification of input constraints (e.g., duplicate email registrations and invalid authentication triggers).
- ✅ **End-to-End Checkout Pipeline:** Full automation of product selection, dynamic cart handling, billing details submission, and multi-stage checkout forms.
- ✅ **Downstream Document Verification:** Automated handling of order history validation and invoice generation verification.

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|:-----------|:--------|:--------|
| **Java** | 21 | Programming Language |
| **Selenium WebDriver** | 4.x | Browser Automation |
| **Maven** | 3.2.5+ | Build & Dependency Management |

## 📝 Test Scenarios (User Stories)

The project executes 9 business-critical user stories ensuring web application stability:

| ID | User Story / Feature | Description |
|:---|:-----------|:------------|
| 🔑 **US_201** | Register User | Validates a successful user sign-up flow across mandatory demographic and credential fields. |
| ❌ **US_202** | Negative Register User | Tests duplicate data constraints by asserting that trying to re-register with an existing email addresses triggers validation errors. |
| 🔓 **US_203** | User Login | Verifies secure session establishment for a valid registered entity, ensuring the user email renders on the global navigation header. |
| 🛒 **US_204** | Shopping Cart Control | Automates navigating product listing pages, selecting assets, adding them to the cart, and asserting dynamic pricing matrix calculations. |
| 💳 **US_205** | Checkout Process | Simulates an E2E purchasing route by filling out shipping coordinates, method selections, and payment forms. |
| 📄 **US_206** | Order History & Invoice | Enters the user account dashboard, parses the history grid to locate archived orders, and verifies invoice accessibility. |
| 🔄 **US_207** | Account Update | Validates that an active user can modify their dynamic profile attributes and persist changes safely. |
| 🔍 **US_208** | Product Search | Tests the multi-category search engine accuracy against boundary keywords and auto-suggestions. |
| 📉 **US_209** | Filter & Sort Control | Verifies catalog sorting algorithms (Price, Name, Relevance) and category filtering components. |

## 📁 Project Structure

```text
DemoWebShop_Automation/
│
├── 📄 pom.xml                          # Maven dependencies
├── 📄 README.md                        # Framework documentation
└── src/
    └── test/
        └── java/
            ├── US201_RegisterUser/             # Verification of user onboarding
            ├── US202_NegativeRegisterUser/     # Boundary checks for duplicate identity
            ├── US203_Login/                    # Session authorization flows
            ├── US204_ShoppingCartControl/      # Cart inventory & balance checks
            ├── US205_CheckoutProcess/          # End-to-end checkout execution
            ├── US206_OrderHistoryAndInvoice/   # Profile order history & PDF validation
            ├── US207_AccountUpdate/            # Dynamic profile updates
            ├── US208_ProductSearch/            # Catalog search verifications
            └── US209_FilterAndSortControl/     # Filter and catalog sorting tests
```
🏗️ Technical Architecture & Implementation
🎯 Modular Workspace Organization: Test scripts are decoupled cleanly into distinct user-story packages (US201 to US209), preventing multi-thread interference and minimizing code dependencies.

🔄 Asynchronous Sync Management: Leverages implicit and customized explicit waits within BaseDriver to manage dynamic checkout step animations without producing unstable results.

🛡️ Document Delivery Control: US_206 automates complex profile dashboard grids, cross-checking that transactional metadata perfectly aligns with downstream invoice generations.
