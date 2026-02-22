# 🛒 POS Payment Processing System (C++)

## 📌 Overview
This is an Object-Oriented Point of Sale (POS) payment processing application built in C++. The system simulates a real-world checkout environment by handling multiple payment methods (Cash, Credit/Debit Cards, and Mobile Payments), generating unique authorization codes, and logging transactions to a local text file for permanent record keeping.

## 🧠 Core C++ Concepts Demonstrated
This project goes beyond basic algorithms and showcases structural software engineering principles:
* **Object-Oriented Programming (OOP):** Utilizes separate classes (`PaymentProcessor` and `TransactionManager`) to enforce the Single Responsibility Principle.
* **Dynamic Memory Management:** Safely allocates and deallocates memory using pointers (`new` and `delete`) to manage active transactions without memory leaks.
* **File I/O Operations:** Automatically logs successful transactions to `transactions.txt` and isolates failed/declined attempts into a separate `payment_errors.log` file using the `<fstream>` library.
* **Data Structures:** Leverages C++ STL `vector` to maintain transaction history and `map` for categorizing payment statistics.
* **Randomization & Time:** Simulates real-world bank authorization approvals and records precise timestamps using `<ctime>` and `<cstdlib>`.

## 🚀 Features
* Validates credit card formats (16-digit length, MM/YY expiry, CVV length).
* Calculates exact change for cash transactions.
* Simulates network latency/declines (90% approval rate for cards, 95% for mobile).
* Persistent logging system so transaction data is not lost when the program closes.

## 💻 Build & Execution
This program is written in standard C++ and can be compiled using the G++ compiler via the command line.

**Example compilation (Windows):**
```cmd
g++ pos_system.cpp -o pos_system
.\pos_system.exe
