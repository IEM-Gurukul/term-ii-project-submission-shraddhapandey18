[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/pG3gvzt-)
# PCCCS495 – Term II Project

## AuctionBiddingSystem

---

## The Auction Bidding System is designed to facilitate online auctions for various types of items, supporting both live auctions with fixed durations and reserve auctions that require meeting a minimum price threshold. The system needs to handle multiple bidders, manage auction lifecycles, provide real-time bidding capabilities, and maintain data persistence.
 Key Requirements:
✅ Support for different auction types (live and reserve)
✅ Item categorization (physical and digital items)
✅ Bidder registration and management
✅ Bid validation and auction rules enforcement
✅ Observer pattern for notifications and logging
✅ File-based data persistence
✅ Command-line interface for user interaction
✅ Error handling for various failure scenarios
The system must demonstrate strong object-oriented programming principles including inheritance, polymorphism, abstraction, and encapsulation while providing a robust and user-friendly auction platform.
---

## The target users of this system are buyers who participate in auctions by placing bids, and sellers who create auctions to sell their items. Additionally, an admin can manage and monitor the system.

---

## The core features include multiple auction types, item and bidder management, bid validation, auction lifecycle handling, observer-based notifications, file persistence, CLI interaction, and robust error handling.

- 
- 
- 

---

## OOP Concepts Used

- Abstraction
- Inheritance
- Polymorphism
- Exception Handling
- Collections / Threads

---

## Proposed Architecture Description
The Auction Bidding System is designed using a modular, layered architecture that follows core Object-Oriented Programming (OOP) principles. The system is divided into multiple layers, each responsible for a specific functionality, ensuring clean structure, scalability, and maintainability.

📦 1. Presentation Layer (CLI)
Implemented in Main.java
Handles:
User input
Menu display
Interaction with the system

Acts as the entry point for the application.

⚙️ 2. Business Logic Layer
Implemented in core/AuctionManager.java
Handles:
Auction registration and retrieval
Bidder management
Coordination between system components

Acts as the central controller of the system.

🔨 3. Domain Layer (Models)
Located in model/ and auction/
Key classes:
Auction, LiveAuction, ReserveAuction
Item, PhysicalItem, DigitalItem
Bid, Bidder
Responsibilities:
Represent real-world entities
Implement business rules (e.g., bid validation)

This is the core of the application logic.

👁️ 4. Observer Layer
Located in observer/
Components:
AuctionObserver (interface)
AuctionLogger
BidderNotifier
Responsibilities:
Event handling
Logging auction activity
Notifying bidders

Implements the Observer Design Pattern for loose coupling.

💾 5. Persistence Layer
Implemented in storage/FileManager.java
Handles:
Saving auction and bidder data
Loading data from files

Provides file-based data persistence.

⚠️ 6. Exception Handling
Located in exceptions/
Custom exceptions:
InvalidBidException
AuctionClosedException
ReservePriceNotMetException

Ensures robust error handling and clear feedback.

🔄 System Flow
User (CLI)
   ↓
Main.java (Presentation Layer)
   ↓
AuctionManager (Business Logic)
   ↓
Auction / Item / Bidder (Domain Layer)
   ↓
Observers (Logger & Notifier)
   ↓
FileManager (Persistence)

---

## How to Run
From project root (Windows PowerShell):

cd c:\AuctionBiddingSystem
go to src and run terminal and run main "java Main.java"

---

## Git Discipline Notes
* Initial commit: Project setup with basic structure
* Add abstract Item base class with common properties
* Add PhysicalItem and DigitalItem concrete classes
* Add Bid immutable value object and Bidder class
* Add abstract Auction base class with template method pattern
* Add LiveAuction and ReserveAuction concrete implementations  
* Add observer pattern implementation
* Add AuctionManager central registry
* Add custom exception classes for error handling
* Add FileManager utility class for data persistence
* Add Main.java console UI with complete menu system
* Add comprehensive documentation and project files
* Test application functionality - demo runs successfully
* Add sample auction data and test results
* Implement auction manager and file persistence
* Add observer pattern for logging and notifications
* Implement auction system with multiple types
* Initial project structure and exceptions
* Refactor auction core, add observers & storage
* Update README with project information
