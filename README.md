Sapphire 💎 | Intelligent Personal Finance Engine
Sapphire is a robust personal finance management tool built for Android. Unlike basic expense trackers, Sapphire combines a centralized logic engine with custom data visualization to give users a high-definition view of their financial health.
![alt text](https://img.shields.io/badge/Platform-Android-brightgreen.svg)

![alt text](https://img.shields.io/badge/Language-Kotlin-blue.svg)

![alt text](https://img.shields.io/badge/Design-Material--3-blueviolet.svg)

![alt text](https://img.shields.io/badge/Version-1.2-orange.svg)
📖 Table of Contents
Overview
Core Modules
Key Features in Depth
Technical Architecture
Installation & Setup
Usage Workflow
Roadmap
Contributors
🧐 Overview
Sapphire was developed to solve the problem of "invisible spending." By providing real-time alerts and visual trends, it shifts the user from passive tracking to active financial management. The app uses an In-Memory Data Engine for high-speed calculations and instant UI updates.
🧩 Core Modules
💰 Finance Engine (Logic Hub)
The "brain" of the application. It handles:
Balance Reconciliation: Automatically calculates balance as (Total Income - Total Expenses - Goal Deposits).
Categorization: Tags transactions into "Food", "Transport", "Shopping", or "Other".
Insight Generation: Evaluates spending patterns (Healthy vs. Moderate vs. High).
📊 Analytics Module
Features a custom-drawn SimpleBarChartView using the Android Canvas API. It visualizes the top three spending categories to help users identify their biggest "money leaks" at a glance.
🎯 Savings & Goals
Allows users to move money from their main balance into "locked" goal accounts.
Types: Travel, Emergency, Device, General.
Tracks percentage completion for every goal.
✨ Key Features in Depth
📸 Digital Receipt Attachment
Users can optionally attach images to any transaction. This is handled via the Android Activity Result API, allowing for seamless integration with the system gallery. The URI is stored within the Transaction object for future reference.
📅 Smart Date Integration
The app includes a built-in Calendar Picker that ensures dates are formatted consistently. If a date isn't selected, the system intelligently defaults to "Today."
⚠️ Proactive Alert System
The engine compares totalExpenses() against totalBudget() in real-time. If the threshold is exceeded, the AlertsActivity displays a warning message, acting as a digital financial advisor.
🏗 Technical Architecture
Pattern: Singleton Pattern. The FinanceEngine is an object in Kotlin, ensuring data consistency across all activities (Home, Analytics, Goals).
UI Layer:
ConstraintLayout for complex, flat-hierarchy designs.
Material3 components for modern aesthetic (Cards, Chips, Toggles).
Custom Views: Direct onDraw(canvas) implementation for the Bar Chart to minimize dependency on heavy 3rd-party graphing libraries.
Navigation: A strictly managed 5-item BottomNavigationView to comply with Android UX standards.
⚙️ Installation & Setup
Prerequisites
Android Studio Hedgehog 
JDK 17.
Android API Level 26 (Oreo) 
Steps

🔄 Usage Workflow
Registration: Create a local account.
Set Budget: Navigate to the Budget tab and define your monthly spending limit.
Log Activity: Click the FAB (+) to add income or expenses. Select a category and optionally snap a photo of the receipt.
Check Analytics: Visit the Analytics tab to see your Bar Chart update dynamically.
Save: Create a Goal and deposit your surplus balance to watch your progress bar grow.
🗺 Roadmap

Data Persistence: Implement Room Database to save data after the app closes.

Biometric Lock: Fingerprint/FaceID access for financial privacy.

Currency Conversion: Support for multiple currencies using a real-time API.

Dark Mode: Full optimization for nighttime usage.

Export Feature: Export monthly spending reports to PDF or CSV.
🤝 Contributors
Your Name - Lead Developer & Logic Architect - GitHub Profile
🛡 License
This project is licensed under the MIT License - see the LICENSE file for details.
Sapphire — Building a brighter financial future, one transaction at a time. 💎


## 📺 App Walkthrough & Demo

Below is a visual overview of the Sapphire Finance Engine in action, demonstrating the user journey from authentication to advanced financial insights.

### 🎥 Feature Showcase
<!-- Replace the link below with your actual video link or a GIF of the video -->
[Click here to watch video](https://drive.google.com/file/d/1Zd7CKI0x6nGhVsjpBIiEn_3Lf0pUcL-1/view?usp=drivesdk)
GITLINK(https://github.com/ThatoMatabane)
### 🛠 Key Workflow (As seen in the Demo)

1. **Onboarding & Security**
   - **Splash Screen:** Branded entry point.
   - **User Authentication:** A secure Registration and Login system where users sign up with Full Name, Email, and Password. 
   - **Personalized Experience:** The dashboard greets users with a "Welcome Back" text specifically for their account.

2. **The Intelligent Dashboard**
   - **Real-Time Balancing:** View Total Balance, Budget, and Expenses at a glance.
   - **Dynamic Visualization:** A custom Bar Chart that updates instantly as transactions are added.
   - **Recent Transactions:** A clean, scrollable list (RecyclerView) showing the latest financial activity with color-coded indicators (Red for Expenses, Green for Income).

3. **Advanced Transaction Entry**
   - **Income/Expense Toggle:** Easily switch between money coming in and going out.
   - **Smart Pickers:** Integrated Date Picker for historical accuracy.
   - **Category Chips:** Quick-select categories like Food, Transport, and Shopping.
   - **Multimedia Support:** Optionally attach receipt photos or descriptive images directly from the device gallery.

4. **Savings Vault & Goal Setting**
   - **Structured Goals:** Create specific savings targets (e.g., Emergency Fund) with target amounts.
   - **Deposit System:** Move funds from the main balance into a specific goal with a single tap.
   - **Progress Visualization:** A dedicated progress bar showing exactly how close you are to reaching your financial dreams.

5. **Financial Insights & Gamification**
   - **Spending Patterns:** The engine analyzes data to detect "High Spending Trends."
   - **Savings Opportunities:** Automated advice based on the current balance.
   - **Recommended Actions:** Actionable tips (e.g., "Save R25 daily") to help users reach their targets faster.

---
