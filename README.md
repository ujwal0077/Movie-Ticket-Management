

This project is a console-based movie ticket booking system implemented in C++. The system allows users to select movies, choose show timings, register for a membership card, and make payments.

## Features

- **View Movie Timings**: Users can see the available movies and their show timings.
- **Contact Information**: Users can get contact information for further inquiries.
- **Membership Registration**: Users can register for a DTCard, which provides various benefits and discounts.
- **Ticket Booking**: Users can book tickets by providing their details and choosing show timings.

## Classes and Functions

### Classes

1. **ticket**: 
   - Contains attributes for the user's name and contact number.

    ```cpp
    class ticket {
    public:
        char name[10];
        char cno[10];
    } t; // object definition for ticket
    ```

2. **card**: 
   - Inherits from the `ticket` class and contains additional attributes for the user's address and email ID.

    ```cpp
    class card : public ticket {
    public:
        char address[1000];
        char emailid[20];
    } v; // object definition for card
    ```

### Functions

1. **menu()**: 
   - Displays the main menu options for the user.

    ```cpp
    void menu() {
        cout << "\n\t\t\t ----------------------------------";
        cout << "\n\t\t\t\t BOX OFFICE";
        cout << "\n\t\t\t ----------------------------------";
        cout << "\n\t\t\t\t Welcome Customer!";
        cout << "\n\n\t\t\t\t <1> Movie Timings";
        cout << "\n\t\t\t\t <2> Contact Us";
        cout << "\n\t\t\t\t <3> DTCard Registration";
        cout << "\n\t\t\t\t <4> Exit \n\n";
        cout << "\t\t\t\tEnter Your Choice :" << "\t";
    }
    ```

2. **main()**: 
   - Handles the main logic and flow of the program, including displaying the menu, handling user input, and calling other functions based on the user's choice.

    ```cpp
    int main() {
        system("CLS");
        int choice, movie, b, N, x, cardid;
        char ans;
        
        do {
            menu();
            while (!(cin >> choice) && (choice < 1 || choice > 4)) {
                cout << "Invalid selection - Please input 1 to 4 only.\n";
                cin.clear();
                cin.ignore(numeric_limits<streamsize>::max(), '\n');
            }
            switch (choice) {
                case 1:
                    // Handle movie timings selection and booking
                    break;
                case 2:
                    // Display contact information
                    break;
                case 3:
                    // Handle DTCard registration
                    break;
                case 4:
                    // Exit the program
                    break;
                default:
                    cout << "Invalid input.";
            }
        } while (ans == 'y');
    }
    ```

3. **pay(int a)**: 
   - Handles the payment process for the tickets.

    ```cpp
    void pay(int a) {
        // Payment logic
    }
    ```

4. **card()**: 
   - Handles the registration process for the DTCard.

    ```cpp
    void card() {
        // DTCard registration logic
    }
    ```

## How to Run

1. **Compile the code**: Use a C++ compiler to compile the source code. For example:
    ```
    g++ movie_ticket_booking.cpp -o movie_ticket_booking
    ```

2. **Run the executable**:
    ```
    ./movie_ticket_booking
    ```

## Requirements

- C++ compiler
- Standard C++ libraries

