Flight Booking System Documentation
 
The Flight Booking System is a console-based application implemented in C++ that allows users to book flights by entering their personal details. It demonstrates a comprehensive understanding of Object-Oriented Programming (OOP) concepts such as inheritance, polymorphism, encapsulation, and exception handling.

 Features
Add Flights:Predefined flights can be added to the system.
Book Seats: Users can book a seat on a flight by entering their details and selecting a flight.
Display Bookings:The system displays all the bookings, showing flight details and passenger information.
Exception Handling: Handles cases where a flight is not found.

Classes and Methods

Class: `Person`
Purpose:Base class for storing basic person information.
Data Members:
  - `string name`: Stores the name of the person.
  - `int age`: Stores the age of the person.

- Methods:
  - `Person(string n, int a)`: Constructor to initialize name and age.
  - `virtual void displayInfo()`: Displays the person's information.

Class: `Passenger`
Purpose:Derived class from `Person` that adds passport information.
Data Members:
  - `string passportNumber`: Stores the passport number of the passenger.

Methods:
  - `Passenger(string n, int a, string pNum)`: Constructor to initialize name, age, and passport number.
  - `void displayInfo() override`: Displays the passenger's information.

Class: `Flight`
Purpose:Manages flight details and passengers.
- Data Members
  - `string flightNumber`: Stores the flight number.
  - `string destination`: Stores the flight destination.
  - `vector<Passenger> passengers`: Stores the list of passengers on the flight.


Class: `Booking`
Purpose: Manages multiple flights and bookings.
- Data Members:
  - `vector<Flight> flights`: Stores the list of flights.
- Methods:
  - `void addFlight(Flight f)`: Adds a flight to the system.
  - `void bookSeat(string flightNumber, Passenger p)`: Books a seat for a passenger on a specified flight.
  - `void displayBookings()`: Displays all flights and their bookings.

How to Use

1. Run the Program:
   Compile and run the program using a C++ compiler.

2. Enter Details:
   - The program will prompt you to enter your name, age, and passport number.
   - You will then be presented with available flights and asked to enter the flight number you want to book.

3. View Bookings:
   - The system will display all flights and their corresponding passengers after booking.

Example Usage

Enter your name: meshack maweu
Enter your age: 20
Enter your passport number: P123456
Available flights: 
1. BA101 to kenya
2. BA202 to London
3. BA303 to USA
Enter flight number to book: BA101

Flight Number: BA101, Destination: Kenya
Passenger Info - Name: meshack maweu, Age: 20, Passport Number: P123456

Exception Handling
- If an invalid flight number is entered, the system will display an error message: "Error: Flight not found".

Code Structure

cpp
int main() {
    try {
        // Setup and user interaction code
    }
    catch (const exception &e) {
        cerr << "Error: " << e.what() << endl;
    }
    return 0;
}

The Flight Booking System is a simple yet comprehensive demonstration of OOP concepts in C++. It allows users to interactively book flights and handles common errors gracefully. This system can be expanded with more features such as cancellation, multiple flight classes, etc., making it a solid foundation for a more complex flight booking application.
