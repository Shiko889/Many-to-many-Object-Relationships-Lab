# Book, Author, and Contract Management System

## Introduction
This project implements a system to manage books, authors, and contracts between authors and books. It allows tracking authors, books, and their contracts while providing functionalities to retrieve related information.

## Classes

### Book
- Attributes:
  - `title`: The title of the book.
  - `all_books`: A class variable to store all instances of books created.
- Methods:
  - `__init__(self, title)`: Initializes a new instance of the Book class with the provided title and adds it to the list of all books.

### Author
- Attributes:
  - `name`: The name of the author.
  - `all_authors`: A class variable to store all instances of authors created.
- Methods:
  - `__init__(self, name)`: Initializes a new instance of the Author class with the provided name and adds it to the list of all authors.
  - `contracts(self)`: Returns a list of contracts related to the author.
  - `books(self)`: Returns a list of books related to the author through contracts.
  - `sign_contract(self, book, date, royalties)`: Creates and returns a new Contract object between the author and the specified book with the given date and royalties.
  - `total_royalties(self)`: Returns the total royalties earned by the author from all contracts.

### Contract
- Attributes:
  - `author`: An instance of the Author class representing the author involved in the contract.
  - `book`: An instance of the Book class representing the book involved in the contract.
  - `date`: A string representing the date when the contract was signed.
  - `royalties`: An integer representing the percentage of royalties that the author will receive for the book.
  - `all_contracts`: A class variable to store all instances of contracts created.
- Methods:
  - `__init__(self, author, book, date, royalties)`: Initializes a new instance of the Contract class with the provided author, book, date, and royalties, and adds it to the list of all contracts.
  - `contracts_by_date(cls, date)`: A class method that returns all contracts with the specified date.



