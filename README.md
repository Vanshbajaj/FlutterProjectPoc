👜 WalletWise – Personal Finance Tracker
A Flutter POC to manage personal finances, track expenses, visualize analytics, and integrate public APIs.

📝 Overview
WalletWise is a Flutter mobile application designed to help users manage daily expenses, view spending insights, and integrate with multiple public APIs for live data.
The app follows Clean Architecture and uses Riverpod for scalable and testable state management.

✨ Features
1. 🔐 Authentication


Simple login (Firebase Auth or optional local mock)


Persist user session until logout


2. 💸 Expense Management


Add, edit, and delete expenses


Fields: amount, currency, category, date, notes


Automatic currency conversion via Frankfurter API


Expense list with search, category filters & date range filters


Detailed expense view


3. 📊 Dashboard & Analytics


Monthly spending summary


Recent transactions widget


Category-wise spending chart (pie/donut)


Optional daily/weekly bar chart


4. 🌐 Public API Integrations


Quotable API: Daily motivational quote (cached)


DummyJSON API: Load sample products → convert into dummy expenses


Frankfurter API: Exchange rates & currency conversion


5. ⚙️ Settings


Change base currency


Theme switch (Light / Dark / System)


Toggle dashboard quote


Load sample expenses


Logout


6. 📶 Offline Support


Cached exchange rates & quotes


Local database ensures full offline functionality (Hive / Drift / sqflite)


7. 💾 Local Storage


Store expenses


Save user preferences


Cache API responses



🛠 Tech Stack


Flutter 3.x+


Riverpod (state management)


Clean Architecture (Domain / Data / Presentation)


Local DB: Hive / Drift / sqflite


APIs: Frankfurter, Quotable, DummyJSON


Testing: Unit & Widget tests


CI/CD: GitHub Actions (formatting, analyze, tests)


Codegen: freezed, json_serializable (optional but recommended)



📁 Project Structure
lib/
 └── src/
      ├── core/           # Shared utilities, errors, network handlers
      ├── features/       # Feature modules
      │     ├── auth/
      │     ├── expenses/
      │     ├── dashboard/
      │     ├── settings/
      │     └── sample_data/
      ├── app.dart        # App initialization (theme, routes)
      └── main.dart       # Entry point


🚀 Getting Started
Prerequisites


Flutter SDK 3.x+


Dart ≥ 3.0


Android Studio / VSCode


Git

Install dependencies:
flutter pub get

Generate code (if using freezed / json_serializable):
flutter pub run build_runner build --delete-conflicting-outputs

Run the app:
flutter run


🔧 Testing
Run all unit and widget tests:
flutter test


📌 Notes


Riverpod powers the state management throughout the app.


Local caching ensures reliable offline behavior.


Public API integrations:


Frankfurter – currency conversion


Quotable – daily quote


DummyJSON – load sample product data
