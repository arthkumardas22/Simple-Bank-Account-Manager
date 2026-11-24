# Simple Bank Account Manager --- DSA Project

A console-based, menu-driven Java application that simulates basic
banking operations and demonstrates core **Data Structures and
Algorithms (DSA)** concepts using a custom-built **singly linked list**.

## Project Information

  -----------------------------------------------------------------------
  Field                               Details
  ----------------------------------- -----------------------------------
  Project Title                       Simple Bank Account Manager

  Submitted By                        Arth Kumar Das

  Student ID / ERP                    RU-25-11807

  University                          Rungta International Skills
                                      University (RISU)

  Degree                              B.Tech.

  Branch                              Computer Science and Engineering
                                      --- AI/ML in association with
                                      Google

  Semester                            Third Semester

  Subject                             Data Structures and Algorithms

  Course Code                         RU-200-01-00029

  Programming Language                Java

  Academic Session                    2026--27

  Faculty Guide                       Professor Santanu Sasmal
  -----------------------------------------------------------------------

## Overview

The Simple Bank Account Manager is an academic banking simulation. It
allows a user to create and manage bank accounts through a numbered
console menu. Account records are stored in a custom singly linked list
rather than a built-in collection, making operations such as traversal,
insertion, deletion and searching easier to study.

The project uses Java object-oriented programming principles and
`BigDecimal` for accurate monetary calculations.

## Features

-   Create an account with a unique account number.
-   Deposit money into an account.
-   Withdraw money while preventing overdrafts.
-   View an account balance.
-   Search for an account by account number.
-   Update the account holder's name.
-   Close (delete) an account.
-   Display all accounts.
-   Sort accounts by account number, holder name or balance.
-   Validate inputs and handle invalid entries.
-   Optional file handling to save and reload account records.

## Data Structures and Algorithms

### Primary data structure: Singly Linked List

Each node stores a `BankAccount` object and a reference to the next
node. The list can grow or shrink dynamically without shifting existing
records.

### Secondary structure: Array Snapshot

The linked list can be copied into an array and sorted. This array
snapshot is used to demonstrate binary search, which requires sorted
data and constant-time index access.

### Algorithms

  -----------------------------------------------------------------------
  Algorithm               Purpose                 Time Complexity
  ----------------------- ----------------------- -----------------------
  Linear Search           Find an account in the  O(n)
                          linked list             

  Binary Search           Find an account in a    O(log n)
                          sorted array snapshot   

  Merge Sort              Sort linked-list        O(n log n)
                          accounts                

  Insertion Sort          Sort the array snapshot O(n²) average/worst
  -----------------------------------------------------------------------

*Building the array snapshot takes O(n) time. Binary search is performed
only after the array has been sorted.*

## Project Structure

The planned design is divided into the following Java classes:

  -----------------------------------------------------------------------
  Class                               Responsibility
  ----------------------------------- -----------------------------------
  `BankAccount`                       Stores account number, holder name
                                      and balance; provides deposit and
                                      withdrawal operations.

  `Node`                              Represents one linked-list node
                                      containing a bank account and a
                                      next reference.

  `AccountList`                       Implements linked-list insertion,
                                      searching, deletion, conversion to
                                      an array and merge sort.

  `BankManager`                       Applies banking rules and manages
                                      account operations and validation.

  `Main`                              Displays the menu, accepts console
                                      input and calls `BankManager`.

  `FileStorage` *(optional)*          Saves and loads account records
                                      using Java I/O.
  -----------------------------------------------------------------------

## Technology Requirements

-   **Language:** Java
-   **JDK:** 17 or later
-   **RAM:** 4 GB minimum
-   **Storage:** 500 MB free space
-   **Operating Systems:** Windows, Linux or macOS
-   **IDE options:** VS Code, IntelliJ IDEA, Eclipse or NetBeans
-   **Tools:** Terminal / Command Prompt; Git is optional

## How to Run

1.  Install JDK 17 or later.
2.  Open the project folder in your preferred Java IDE or terminal.
3.  Compile the Java source files.
4.  Run the class containing the `main()` method.

For a terminal-based project whose source files are in the current
directory, the general commands are:

``` bash
javac *.java
java Main
```

> **Note:** These commands assume the source files use the default
> package and the entry-point class is named `Main`. Adjust the commands
> if your project uses a package or a different class name.

## Sample Menu

``` text
===== SIMPLE BANK ACCOUNT MANAGER =====
1. Create account
2. Deposit
3. Withdraw
4. Show balance
5. Search
6. Update name
7. Close account
8. List accounts
9. Sort accounts
0. Exit
```

## Validation and Error Handling

The application is designed to:

-   Reject duplicate or non-positive account numbers.
-   Reject empty account-holder names.
-   Reject negative opening balances and non-positive transaction
    amounts.
-   Prevent withdrawals that exceed the available balance.
-   Display an account-not-found message when an account number does not
    exist.
-   Handle invalid or non-numeric menu input without terminating
    unexpectedly.

## Important Design Decisions

-   `BigDecimal` is used for monetary values to avoid floating-point
    rounding errors.
-   Account fields are private and are accessed or modified through
    methods.
-   A custom linked list is used so that pointer manipulation and
    operation costs remain visible for DSA learning.
-   Binary search is demonstrated on a sorted array snapshot, not
    directly on the linked list.

## Scope and Limitations

This project is an educational simulation, not a production banking
system. A graphical interface, networking, real payments, authentication
and security hardening, multi-user concurrency and database integration
are outside the core scope.

Optional enhancements include file-based persistence, a hash-table index
for faster average account lookup, and a stack-based transaction
history.

## Learning Outcomes

Through this project, the implementation demonstrates:

-   Practical use of classes, objects, constructors and encapsulation in
    Java.
-   Implementation of a custom singly linked list.
-   Searching and sorting techniques.
-   Comparison of array and linked-list operations.
-   Time and auxiliary-space complexity analysis.
-   Input validation and basic exception handling.

## Author

**Arth Kumar Das**\
ERP: `RU-25-11807`\
Rungta International Skills University

------------------------------------------------------------------------

*This README describes the project design from the project synopsis.
Optional file persistence and other enhancements should be marked as
implemented only after they have been developed and tested.*
