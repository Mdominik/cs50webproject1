## Course: Web Programming with Python and JavaScript
### Project 1

In short, the website allows for searching for books in a database of 5000 records and sharing user's comments on specific books. It is possible to sign up an account and see other people's reviews.
Techstack: Python3.6, Flask, Bootstrap, SQL

**Requirements:**

- Registration: Users should be able to register for your website, providing (at minimum) a username and password.

- Login: Users, once registered, should be able to log in to your website with their username and password.

- Logout: Logged in users should be able to log out of the site.

- Import: Provided for you in this project is a file called books.csv, which is a spreadsheet in CSV format of 5000 different books. Each one has an ISBN number, a title, an author, and a publication year. In a Python file called import.py separate from your web application, write a program that will take the books and import them into your PostgreSQL database. You will first need to decide what table(s) to create, what columns those tables should have, and how they should relate to one another. Run this program by running python3 import.py to import the books into your database, and submit this program with the rest of your project code.

- Search: Once a user has logged in, they should be taken to a page where they can search for a book. Users should be able to type in the ISBN number of a book, the title of a book, or the author of a book. After performing the search, your website should display a list of possible matching results, or some sort of message if there were no matches. If the user typed in only part of a title, ISBN, or author name, your search page should find matches for those as well!

- Book Page: When users click on a book from the results of the search page, they should be taken to a book page, with details about the book: its title, author, publication year, ISBN number, and any reviews that users have left for the book on your website.

- Review Submission: On the book page, users should be able to submit a review: consisting of a rating on a scale of 1 to 5, as well as a text component to the review where the user can write their opinion about a book. Users should not be able to submit multiple reviews for the same book.

- Goodreads Review Data: On your book page, you should also display (if available) the average rating and number of ratings the work has received from Goodreads.

- API Access: If users make a GET request to your website’s /api/<isbn> route, where <isbn> is an ISBN number, your website should return a JSON response containing the book’s title, author, publication date, ISBN number, review count, and average score. The resulting JSON should follow the format [...]


**Files**

The projects consists of:
- application.py (Flask application)
- bookRecord.html (result of book search)
- bookSearch.html (book search form)
- homepage.html (main page. Shows logged in user's comments)
- layout.html (page layout with menu and footer)
- login.html (login form)
- signup.html (signup form)



**SQL Tables**

books:

1. *isbn* character varying	
2. *title* character varying	
3. *author* character varying	
4. *year* integer

users:

1. *id*	integer Auto Increment [nextval('users_id_seq')]	
2. *username*	character varying	
3. *password*	character varying

reviews:

1. *idreview*	integer Auto Increment [nextval('reviews_idreview_seq')]	
2. *iduser*	integer	
3. *isbn*	character varying	
4. *rating*	numeric	
5. *comment*	text	
6. *date*	date NULL

LINK: https://dommaz-cs50-project1-books.herokuapp.com/
