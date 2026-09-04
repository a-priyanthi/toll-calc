# Vehicle Toll Calculation System

A console-based Java application for managing vehicle registrations and calculating toll charges based on vehicle type. The project demonstrates core Object-Oriented Programming principles including abstraction, inheritance, method overriding, static members, constructors, and final variables.

## Overview

The Vehicle Toll Calculation System provides a simple menu-driven interface for registering different types of vehicles and calculating their corresponding toll charges.

The system currently supports three vehicle categories:

* Car
* Bus
* Truck

Each vehicle type inherits common properties and behavior from an abstract `vehicle` class while implementing its own toll calculation logic.

## Features

* Register vehicles by vehicle number
* Support for multiple vehicle types
* Vehicle-specific toll calculation
* Maintain a global vehicle count
* Store registered vehicle numbers
* Display registered vehicle details
* Menu-driven command-line interface
* Object-oriented class structure

## Toll Structure

The system uses a common base amount of `$50` in addition to the vehicle-specific toll.

| Vehicle Type | Base Toll | Additional Amount | Total Toll |
| ------------ | --------- | ----------------- | ---------- |
| Car          | $200      | $50               | $250       |
| Bus          | $300      | $50               | $350       |
| Truck        | $400      | $50               | $450       |

The base amount is maintained as a static final value in the parent class, allowing it to be shared across all vehicle types.

## Object-Oriented Design

### Abstraction

The `vehicle` class is declared as an abstract class and defines the common structure for all vehicle types.

```java
abstract class vehicle
{
    final int num;
    abstract int calc();
}
```

The `calc()` method is abstract because each vehicle category has a different toll calculation.

### Inheritance

The `car`, `bus`, and `truck` classes extend the `vehicle` class.

```java
class car extends vehicle
class bus extends vehicle
class truck extends vehicle
```

This allows the subclasses to reuse the common vehicle properties and methods.

### Method Overriding

Each subclass provides its own implementation of the `calc()` method.

```java
int calc()
{
    return 200 + m;
}
```

The corresponding toll values are implemented independently for buses and trucks.

### Static Members

The system uses static members to maintain information shared across all vehicle objects.

```java
static int count;
static int reg[] = new int[10];
```

`count` maintains the total number of registered vehicles, while `reg` stores their vehicle numbers.

### Final Variable

The vehicle number is declared using the `final` keyword:

```java
final int num;
```

Once initialized through the constructor, the vehicle number cannot be modified.

### Static Initialization Block

The common additional toll amount is initialized using a static initialization block:

```java
static
{
    m = 50;
}
```

This ensures that the value is initialized when the class is loaded.

## Program Flow

```text
Start
  |
  v
Display Menu
  |
  +----> Register Car ------> Calculate Toll
  |
  +----> Register Bus ------> Calculate Toll
  |
  +----> Register Truck ----> Calculate Toll
  |
  +----> Display Count -----> Display Vehicle Numbers
  |
  +----> Exit
  |
  v
End
```

## Project Structure

```text
Vehicle-Toll-Calculation/
│
├── vtc.java
└── README.md
```

The complete implementation is contained in `vtc.java`, which includes:

* `vehicle` — Abstract parent class
* `car` — Car implementation
* `bus` — Bus implementation
* `truck` — Truck implementation
* `vtc` — Main class containing the application logic

## Requirements

* Java Development Kit (JDK) 8 or later
* Command-line terminal or any Java-compatible IDE

## Installation and Execution

### Clone the Repository

```bash
git clone <repository-url>
cd Vehicle-Toll-Calculation
```

### Compile

```bash
javac vtc.java
```

### Run

```bash
java vtc
```

## Usage

After starting the application, the following menu is displayed:

```text
VEHICLE TOLL CALCULATION -----------------------
1.Car
2.Bus
3.Truck
4.Count
5.Exit

Enter Choice:
```

### Register a Vehicle

Select the corresponding vehicle type and enter its vehicle number.

Example:

```text
Enter Choice:
1

Enter vehicle number:
1234

Vehicle number: 1234
Toll amount: $250
```

### Display Vehicle Count

Select option `4` to display the number of registered vehicles and their vehicle numbers.

```text
Vehicle Count: 2
Vehicle number:1234
Vehicle number:5678
```

### Exit

Select option `5` to terminate the application.

## Technical Details

| Component         | Implementation        |
| ----------------- | --------------------- |
| Language          | Java                  |
| Input             | `Scanner`             |
| Architecture      | Object-Oriented       |
| Parent Class      | `vehicle`             |
| Subclasses        | `car`, `bus`, `truck` |
| Vehicle Storage   | Array                 |
| Vehicle Count     | Static variable       |
| Toll Calculation  | Method overriding     |
| Common Toll Value | Static final variable |
| Interface         | Command-line          |

## Limitations

The current implementation has a fixed storage capacity of 10 vehicles per vehicle type.

Additional limitations include:

* Vehicle numbers are not validated for duplicates.
* Vehicle data is not persisted after program termination.
* Toll rates are hard-coded.
* The application does not provide a graphical user interface.
* The program uses separate arrays for each vehicle category.

## Future Enhancements

The project can be extended with:

* Dynamic vehicle storage using `ArrayList`
* Vehicle number validation
* Duplicate vehicle detection
* Configurable toll rates
* Vehicle search functionality
* Vehicle removal functionality
* File-based data persistence
* Database integration
* Graphical user interface
* Transaction history and toll reports

## Learning Outcomes

This project provides practical experience with fundamental Java programming and Object-Oriented Programming concepts, particularly:

* Abstract classes
* Inheritance
* Polymorphism
* Method overriding
* Constructors
* Static members
* Final variables
* Arrays
* Control flow
* Menu-driven application design

## License

This project is intended for educational and learning purposes.

## Author

**Priyanthi**

Java OOP Project
