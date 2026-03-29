# PCCCS495 – Term II Project  
## 🏷️ Auction Bidding System

---

## 📌 Project Description

The **Auction Bidding System** is designed to facilitate online auctions for various types of items. It supports both **live auctions** (time-based) and **reserve auctions** (minimum price-based).

The system handles multiple bidders, manages auction lifecycles, enables real-time bidding, and ensures data persistence.

---

## 🎯 Key Requirements

- ✅ Support for different auction types (Live & Reserve)
- ✅ Item categorization (Physical & Digital)
- ✅ Bidder registration and management
- ✅ Bid validation and rule enforcement
- ✅ Observer pattern for notifications and logging
- ✅ File-based data persistence
- ✅ Command-line interface (CLI)
- ✅ Robust error handling

---

## 👥 Target Users

- **Buyers (Bidders):** Participate in auctions and place bids  
- **Sellers:** Create auctions and list items  
- **Admin (Optional):** Monitor and manage the system  

---

## 🚀 Core Features

- 🔨 Multiple auction types (Live & Reserve)
- 📦 Item management (Physical & Digital items)
- 👤 Bidder registration & tracking
- 💰 Bid validation and processing
- ⏱️ Auction lifecycle management
- 👁️ Observer-based notifications (Logger & Notifier)
- 💾 File-based data persistence
- 🖥️ Command-line interface (CLI)
- ⚠️ Exception handling system

---

## 🧠 OOP Concepts Used

- Abstraction  
- Inheritance  
- Polymorphism  
- Encapsulation  
- Exception Handling  
- Design Patterns:
  - Observer Pattern  
  - Template Method Pattern  

---

## 🏗️ Proposed Architecture

The system follows a **modular, layered architecture** ensuring separation of concerns and scalability.

### 📦 1. Presentation Layer (CLI)
- Implemented in `Main.java`
- Handles user input, menu display, and interaction  
- Acts as the **entry point**

---

### ⚙️ 2. Business Logic Layer
- Implemented in `core/AuctionManager.java`
- Manages auctions, bidders, and system coordination  
- Acts as the **central controller**

---

### 🔨 3. Domain Layer (Models)
- Located in `model/` and `auction/`
- Includes:
  - `Auction`, `LiveAuction`, `ReserveAuction`
  - `Item`, `PhysicalItem`, `DigitalItem`
  - `Bid`, `Bidder`

- Responsible for:
  - Core business logic  
  - Real-world entity representation  

---

### 👁️ 4. Observer Layer
- Located in `observer/`
- Components:
  - `AuctionObserver`
  - `AuctionLogger`
  - `BidderNotifier`

- Handles:
  - Event notifications  
  - Logging  
  - Bidder updates  

---

### 💾 5. Persistence Layer
- Implemented in `storage/FileManager.java`
- Handles saving and loading data from files  

---

### ⚠️ 6. Exception Handling
- Located in `exceptions/`
- Includes:
  - `InvalidBidException`
  - `AuctionClosedException`
  - `ReservePriceNotMetException`

---

## 🔄 System Flow


User (CLI)
↓
Main.java
↓
AuctionManager
↓
Auction / Item / Bidder
↓
Observers (Logger & Notifier)
↓
FileManager (Storage)


---

## ▶️ How to Run

### 📍 Steps (Windows PowerShell)

```
cd AuctionBiddingSystem
cd src
java Main.java


📈 Git Discipline Notes
Initial project setup
Added abstract Item class
Implemented PhysicalItem & DigitalItem
Created Bid and Bidder models
Designed abstract Auction class
Implemented LiveAuction & ReserveAuction
Added Observer Pattern (Logger & Notifier)
Built AuctionManager
Added custom exceptions
Implemented file persistence (FileManager)
Developed CLI (Main.java)
Testing and sample data added
Refactoring and documentation updates
🎉 Conclusion

This project demonstrates strong Object-Oriented Design, proper use of design patterns, and a scalable architecture. It serves as a solid foundation for building real-world auction platforms.
