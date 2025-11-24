# VITYARTHI-
The aim of the project is to design a program that works as a plain ticket booking and seat selection simulator. This program offers easy seat booking and a user friendly interface.
## ✈️ SKY JET: Flight Booking System

This is a simple command-line interface (CLI) application developed in Python to simulate a basic flight booking process, including selecting a destination, choosing a flight, handling payment confirmation, and selecting seats.

-----

## 📋 Features

  * **Passenger Input:** Gathers the number of passengers and their names.
  * **Fixed Boarding:** Boarding location is fixed as **Bhopal (BHO)**.
  * **Destination Selection:** Allows selection of three major destinations:
      * **Delhi (DEL)**
      * **Varanasi (VNS)**
      * **Lucknow (LKO)**
  * **Flight Selection:** Displays a list of available flights with prices for the chosen destination.
  * **Payment Simulation:** Calculates the total cost based on the number of passengers and selected flight, and simulates a bank account verification and payment confirmation process.
  * **Seat Allocation:** Displays a simple seat matrix and allows the user to select available seats.
      * `"O"` represents an **empty seat**.
      * `"X"` represents a **booked seat** (some seats are pre-booked based on the number of passengers).
  * **Ticket Generation:** Displays a final flight detail summary (ticket) upon successful booking and payment.

-----

## 🛠️ Requirements

This script is written in **Python 3** and requires no external libraries. It runs entirely in the standard command-line environment.

-----

## 🚀 How to Run the Program

1.  **Save the code:** Save the provided Python code into a file named, for example, `sky_jet_booking.py`.

2.  **Open your terminal/command prompt.**

3.  **Navigate to the directory** where you saved the file.

4.  **Execute the script** using the Python interpreter:

    ```bash
    python sky_jet_booking.py
    ```

5.  **Follow the on-screen prompts** to complete your booking.

-----

## 🗃️ Code Structure and Key Logic

### 1\. User Input and Initialization

  * The script initializes variables like `pasa` (number of passengers) and `namelist` (list of passenger names).
  * A `for` loop gathers names for all passengers.

### 2\. Destination Selection

  * The user is prompted to select a destination using three-letter airport codes (`DEL`, `VNS`, `LKO`).
  * An `if/elif/else` structure handles destination validation.

### 3\. Flight Data

  * Flight options are stored in dictionaries (`Flight1`, `Flight2`, `Flight3`) with flight number and price information, keyed by a serial number (1, 2, 3...).

### 4\. Flight Booking and Pricing

  * Based on the `Destination`, the corresponding flight dictionary is displayed.
  * The user enters a serial number to select a flight.
  * The total cost (`money`) is calculated as:
    $$money = pasa \times \text{Flight Price}$$

### 5\. Payment and Confirmation

  * The script simulates bank details input (`bankno`, `password`) and final confirmation (`confirm`). The booking proceeds only if `confirm == 1`.

### 6\. Seat Matrix (`seats` dictionary)

  * A dictionary named `seats` defines the airplane layout (A1 to H4), initially set to `"O"` (Empty).
  * The `layout` string is a formatted multiline string that visually represents the seat map.
  * A conditional block (`if pasa == 1:` etc.) pre-allocates some seats (`"X"`) based on the total number of passengers before the allocation process starts.

### 7\. Seat Allocation Logic

  * A `while pasa - cnt > 0:` loop runs until all passengers have selected a seat.
  * It checks if the entered seat (`chair`) is valid and not already booked (`seats[chair] == "X"`).
  * On successful selection, the seat status is changed to `"X"`, and the seat code is added to the `buyed` list.

### 8\. Final Ticket

  * The final `if` blocks display all booking details, including the generated PNR (placeholder), airline, selected seats, route, times (placeholder), passenger names, and the final price paid.

-----

## 💡 Possible Enhancements

  * Implement a separate function for the seat allocation process to improve code modularity.
  * Use a better data structure (like a list of dictionaries or a custom class) for flights instead of separate dictionaries, making it easier to manage and scale.
  * Add real-time date/time selection instead of hardcoded placeholders.
  * Implement robust input validation (e.g., ensuring `int(input())` calls are wrapped in `try-except` blocks to handle non-numeric inputs gracefully).
