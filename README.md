# Hotel Management System

This project is a **C++ Hotel Management System** that allows managing rooms, checking in guests, searching for customer information, and handling reservations. It offers an interactive console-based system for handling various hotel operations such as room management, customer check-in/check-out, and generating guest summary reports.

## Table of Contents

- [Features](#features)
- [System Overview](#system-overview)
- [Class Breakdown](#class-breakdown)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Example Workflow](#example-workflow)
- [License](#license)

## Features

- **Manage Rooms**: Add new rooms, search existing rooms, and view room availability.
- **Check-In**: Register a customer for a particular room and capture details such as name, address, phone number, booking ID, etc.
- **Check-Out**: Generate a bill based on the number of days stayed and show the total payable amount.
- **Available Rooms**: View all available rooms and their details.
- **Search Customer**: Look up customer information by name.
- **Guest Summary Report**: Display the list of all checked-in guests, including their personal and booking details.

## System Overview

This project uses classes to represent customers, rooms, and the hotel management system. The key classes include `Customer`, `Room`, and `HotelMgnt`. Operations like adding rooms, checking in guests, and generating guest reports are carried out via member functions of these classes.

The program offers a simple text-based menu where the user can select different options to perform the necessary operations.

## Class Breakdown

### 1. `Customer`
- **Attributes**: 
  - `name`, `address`, `phone`, `from_date`, `to_date`, `payment_advance`, `booking_id`
- Represents the details of a customer staying at the hotel.

### 2. `Room`
- **Attributes**:
  - `type`, `stype`, `ac`, `roomNumber`, `rent`, `status`, `Customer cust`
- **Functions**:
  - `addRoom(int rno)`: Adds a room with specified attributes.
  - `searchRoom(int rno)`: Searches for a room by its room number.
  - `deleteRoom(int rno)`: Removes a room from the system.
  - `displayRoom(Room room)`: Displays the details of a room.

### 3. `HotelMgnt`
- Inherits from `Room`.
- **Functions**:
  - `checkIn()`: Handles guest check-in, including entering customer details.
  - `getAvailRoom()`: Displays available rooms.
  - `searchCustomer(char *name)`: Searches for a customer by their name.
  - `checkOut(int roomNum)`: Checks a customer out of a room and generates a bill.
  - `guestSummaryReport()`: Displays the summary report of all checked-in guests.

## Getting Started

### Prerequisites
To run the program, you need a C++ compiler installed on your system, such as:

- **g++** (part of GCC)
- **Microsoft Visual C++**
  
### Compilation

Use the following command to compile the program:

```bash
g++ -o hotel_management hotel_management.cpp
```

### Execution

Run the compiled program using:

```bash
./hotel_management
```

## Usage

Upon execution, the system presents the following options:

```
######## Hotel Management #########

1. Manage Rooms
2. Check-In Room
3. Available Rooms
4. Search Customer
5. Check-Out Room
6. Guest Summary Report
7. Exit
```

### Available Options:

1. **Manage Rooms**: Add a room, search for a room, or return to the main menu.
2. **Check-In Room**: Enter guest details to reserve a room.
3. **Available Rooms**: Display the list of rooms that are currently available.
4. **Search Customer**: Find a customer by their name.
5. **Check-Out Room**: Process guest check-out and calculate the bill.
6. **Guest Summary Report**: Show a report of all checked-in guests.
7. **Exit**: Close the program.

## Example Workflow

1. **Manage Rooms**: Add room details such as type (AC/Non-AC), comfort level, size, and rent.
2. **Check-In**: Enter guest details like name, address, phone, dates, and payment.
3. **Available Rooms**: View rooms that are available for check-in.
4. **Search Customer**: Find customer details using their name.
5. **Check-Out**: Calculate the total bill for a customer and mark the room as available.

## License

This project is open-source and available for modification or enhancement under the terms of your selected license.