
# Furni-Track: Concurrent Furniture Inventory & Order Management System
## 94% FINAL MARK FOR THIS 5 MONTH PROJECT

## Overview
NB: This is a Final year Comp 315 group project for Exception Handlers

Furni-Track is a multithreaded furniture store and inventory management system developed in C++. The system supports real-time inventory updates, concurrent customer order processing, secure user authentication, and synchronized inventory management.

The application functions as both an e-commerce platform and an inventory management solution, ensuring that stock levels remain accurate even when multiple customers place orders simultaneously.

---

## Problem

Traditional inventory systems often experience:

* Race conditions when multiple users access stock simultaneously
* Inconsistent inventory records during concurrent transactions
* Order processing conflicts resulting in incorrect stock quantities
* Limited synchronization between inventory and customer orders

These challenges can lead to overselling, inaccurate stock counts, and poor customer experiences.

---

## Solution

Furni-Track provides:

* Real-time inventory synchronization
* Concurrent order processing using multithreading
* Thread-safe inventory updates
* Deadlock prevention strategies
* Secure user authentication for administrators and customers
* Reliable stock consistency across all transactions
* Smart pointer-based memory management

---

## Key Features

### User Authentication

* Admin registration and login
* Customer registration and login
* Access control for system operations

### Inventory Management

* Add products
* Remove products
* Update products
* Search products
* Sort products
* Real-time stock monitoring

### Order Processing

* Shopping cart management
* Order placement
* Stock availability verification
* Automatic inventory updates
* Order acceptance and rejection based on stock levels

### Error Handling

* Product not found
* Insufficient stock
* Invalid user actions
* Authentication failures

---

## System Architecture

### Major Components

* Inventory Manager
* Order Processor
* Graphical User Interface (GUI)

### Data Flow

User → GUI → Inventory Management → Order Processing → Inventory Updates

### Concurrency

* Multiple customer orders processed simultaneously
* Shared inventory accessed by multiple threads
* Real-time stock synchronization
* Mutex protection for critical inventory operations

---

## Thread Safety & Concurrency

The system uses multithreading to support simultaneous customer interactions.

### Concurrency Controls

* Mutex locks protect shared inventory data
* Stock consistency is maintained across threads
* Race conditions are prevented during inventory updates
* Orders are validated before stock modification

### Benefits

* Safe concurrent order processing
* Reliable inventory management
* Improved system responsiveness
* Accurate stock levels at all times

---

## Containers & Memory Management

### 1) Smart Pointers were used

#### 2) unique_ptr were used 

Used for:

* Cart item management

Benefits:

* Automatic memory cleanup
* Ownership safety
* Reduced memory leaks

#### shared_ptr

Used for:

* Inventory product management

Benefits:

* Shared ownership across system components
* Efficient resource management

### STL Containers

 Container | Purpose                               
 vector    : Store cart items and orders           
 map       : Manage products and inventory records 

---

## Tech Stack

* C++
* Object-Oriented Programming (OOP)
* STL Containers
* Multithreading
* Mutex Synchronization
* Smart Pointers (unique_ptr & shared_ptr)
* GUI Development

---

## Testing & Validation

The system was tested under multiple scenarios:

### Test Cases

* Multiple customers ordering the same product
* Large inventory management
* Insufficient stock handling
* Concurrent inventory updates
* User authentication validation

### Results

The system successfully:

* Maintained stock consistency
* Prevented race conditions
* Processed concurrent orders correctly
* Ensured reliable inventory synchronization

---

## Challenges & Lessons Learned

### Technical Challenges

* Concurrency control
* Real-time inventory synchronization
* Error handling
* Data integrity protection

### Solutions Implemented

* Mutex-based synchronization
* Deadlock prevention techniques
* Access control mechanisms
* Validation checks during order processing

### Key Lessons

* Shared data requires synchronization
* Race conditions can cause undefined behavior
* Thread safety is critical in inventory systems
* Smart pointers simplify memory management and improve reliability

---

This system was presented to the whole class and lecturer   

## Authors

### COMP315 Group

* Musa Mofokeng
* Lesego Makoe
* Nontokozo Mthembu
* Luyanda Nkomo
* Sbonelo Maphanga
* Qinisani Ngcobo
* Sakhile Shezi

---

## Acknowledgements

Developed as a COMP315 group project focused on demonstrating advanced C++ concepts including multithreading, concurrency control, synchronization, memory management, and software engineering best practices.
