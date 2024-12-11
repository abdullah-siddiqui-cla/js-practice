# Real-World Mini-App: Library Management System
You are tasked with building a small library management system using JavaScript. The app should allow users to manage books and calculate library statistics.

# Steps:
## Library Setup
- Create a library object with the following properties:
  - name: Name of the library (string).
  - books: An array of book objects. Each book has the properties:
    - id (unique identifier, number)
    - title (string)
    - author (string)
    - isAvailable (boolean, indicates if the book is available).
- Add 5 sample books to the books array.

## Add a New Book
- Write a function `addBook(library, book)` that:
    - Accepts the library object and a new book object.
    - Adds the new book to the books array, ensuring the id is unique.

## Find a Book
- Write a function `findBook(library, searchTerm)` that:
  - Accepts the library object and a searchTerm string.
  - Returns the first book whose title or author includes the search term (case insensitive).

## List Available Books
- Write a function `listAvailableBooks(library)` that:
    - Returns an array of all available books.
  
## Borrow a Book
- Write a function `borrowBook(library, bookId)` that:
  - Accepts the library object and a bookId.
  - Updates the `isAvailable` property of the book with the given ID to false.
  - Throws an error if the book is already borrowed or not found.

## Calculate Statistics
- Write a function `calculateStatistics(library)` that:
  - Uses `reduce` to calculate the total number of books.
  - Uses `filter` and `length` to calculate the number of available books.
  - Logs both values.

## Async Functionality
- Write a function `mockApiFetchBooks()` that:
  - Returns a Promise resolving with an array of book objects after 2 seconds.
  - Fetch the books using this function and add them to the library using `addBook`.

## Additional Features
- Add a method `displayLibraryInfo` to the library object that:
  - Logs the library name and the total number of books.
- Merge the `library` object with a `preferences` object that includes:
  - theme: "dark" or "light".
- Log the merged object.

## Bonus:
- Chain methods to:
  - Filter books with titles containing "JavaScript".
  - Map them to include only the title and author.
  - Log the resulting array.