# Library Management System

This Python-based Library Management System allows for managing books and members in a library setting. The system supports adding and removing books, borrowing and returning books, and viewing information about books and borrowed items.

## Features

- **Manage Books**: Add new books, remove existing books, and view detailed information about each book.
- **Member Management**: Add new members and manage their borrowed books.
- **Book Operations**: Borrow and return books with automatic updates to availability.
- **Interactive Interface**: Provides a user-friendly command-line interface for interaction.

## Classes

### `Book`

Represents a book in the library with attributes such as title, author, ISBN, publication year, price, and the number of available copies. 

**Methods:**
- `__init__(title, author, ISBN, publication_year, price)`: Initializes a new book.
- `display_info()`: Displays detailed information about the book.
- `borrow_book()`: Allows borrowing the book if available.
- `return_book()`: Processes the return of the book.

### `Member`

Represents a library member with attributes such as name, member ID, and a list of borrowed books.

**Methods:**
- `__init__(name, member_id)`: Initializes a new member.
- `borrow_book(book)`: Allows the member to borrow a book.
- `return_book(book)`: Allows the member to return a borrowed book.
- `display_borrowed_books()`: Displays the list of books borrowed by the member.

### `Library`

Represents the library system which manages books and members.

**Methods:**
- `__init__()`: Initializes a new library.
- `add_book(book)`: Adds a new book to the library.
- `remove_book(ISBN)`: Removes a book from the library by ISBN.
- `find_book_by_title(title)`: Finds and returns a book by its title.
- `find_member_by_id(member_id)`: Finds and returns a member by their ID.
- `add_member(member)`: Adds a new member to the library.

## Usage

1. **Initialization**: The system initializes with a pre-defined set of books and a member.
2. **User Interaction**: Users can interact with the system through a command-line interface, choosing options to view book info, borrow/return books, add/remove books, and view borrowed books.

