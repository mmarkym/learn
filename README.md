# learn
🍬 Java Vending Machine — Design Patterns Showcase

A fully object-oriented Vending Machine simulation written in Java that demonstrates real, production-quality use of Design Patterns:

Strategy Pattern

Factory Method Pattern

Template Method Pattern

Interface-Based Design & Polymorphism

This project is structured to be clear, extendable, and beginner-friendly — but still engineered like real enterprise Java.

🚀 Features
✅ 1. Snack Selection (Factory Method)

The user chooses between:

Soda

Chips

The SnackFactory creates the correct snack object using a Factory Method.

✅ 2. Dynamic Pricing (Strategy Pattern)

Choose a pricing rule:

Normal price

Senior discount (10% off)

Weekend pricing (+20%)

Holiday pricing ($1 off)

Each pricing rule is a different PricingStrategy.

✅ 3. Payment Processing (Template Method)

Use either:

Cash

Card

PaymentProcessor.process() defines the algorithm:

validate → debit → printReceipt


Subclasses override only the steps that differ.

✅ 4. Clean, modular architecture

Patterns are separated into packages:

patterns.strategy        ← payment template method  
patterns.vending         ← snacks, pricing, factories  

🧩 Design Patterns Used
🔷 Strategy Pattern — Pricing

Each strategy implements:

double calculate(double basePrice);


Plug in new pricing without changing existing code.

🔷 Factory Method Pattern — Object Creation

Used to create:

Snack objects

Pricing strategies

Keeps object creation clean and centralized.

🔷 Template Method Pattern — Payment

PaymentProcessor defines the steps:

process() {
    validate();
    debit();
    printReceipt();
}


Subclasses implement the details.

📁 Project Structure
src/
 ├─ patterns/
 │   ├─ strategy/
 │   │    ├─ PaymentProcessor.java
 │   │    ├─ CashPayment.java
 │   │    └─ CardPayment.java
 │   │
 │   └─ vending/
 │        ├─ Snack.java
 │        ├─ Soda.java
 │        ├─ Chips.java
 │        ├─ SnackFactory.java
 │        ├─ PricingStrategy.java
 │        ├─ SeniorDiscount.java
 │        ├─ WeekendPrice.java
 │        ├─ HolidayPrice.java
 │        ├─ PricingStrategyFactory.java
 │        └─ VendingMain.java

▶️ Running the Program

Compile and run:

javac VendingMain.java
java VendingMain


The program will prompt you for:

Snack choice

Pricing strategy

Payment method

Then it will:

Calculate final price

Process the payment (Template Method)

Dispense the snack

🖼 UML Diagrams Included

Full Class Diagram (PlantUML)

Full Sequence Diagram (PlantUML)

🌟 Purpose of This Project

This project is a learning and practice environment for understanding how multiple design patterns can work together to build clean, maintainable Java applications.

It's perfect for:

Students

Self-learners

Returning programmers

Java portfolio building

🛠 Future Enhancements

Add Decorators: “Add ice”, “Extra flavor”, “Large size”

Add inventory system

Add logging strategy

Build a GUI (JavaFX version)

Add JUnit tests

❤️ Author

Created as part of a guided journey into Object-Oriented Programming and Design Patterns in Java.
