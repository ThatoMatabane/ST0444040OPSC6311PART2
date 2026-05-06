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
