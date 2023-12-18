# library-management-system
Library Management System Project in Python

It will help to manage the following tasks:

1. Add new books to the database.
2. Issue books to the users or students.
3. Take borrowed books from the users or students.
4. Issue the book again to the person who is already holding that book.
5. Displays all the book records presented in the library with the total available piece   of each book (It shows all the records in a table view format).
6. Search a book by name. In this case, if the users don’t know the full name of the book, they can search by only a word or characters instead.
7. Update and delete the book records.
8. Displays the records of all the borrowers with the related information.

The Project Details :

The graphical interface of this project is managed by the Tkinter library. The PyMySQL package is used here to manage database operations using python. The project folder contains three python files, ‘main.py’, ‘custom.py’, and ‘credentials.py’.

As the name of ‘main.py’, it handles all the tasks related to library management. ‘custom.py’ has several information about the colors and fonts used in the main program (main.py). ‘credentials.py’ contains credentials to log in to the MySQL Server. Here, users need to enter their own Username and Password for the MySQL server.

As we’ll be interacting with the database, it’s essential to have MySQL Server installed on your system (You can find instructions on how to install MySQL on Windows, Linux, and Mac). If you’ve already completed this step, there’s no need to do it again.



****Requirements and Installation****

Use pip3 instead of pip for Linux and Mac.

Install PyMySQL
☛pip install PyMySQL

Install Tkinter
☛pip install tk



****Install MySQL server****



****Create a Database and Two Tables****
☛Create a table "book_list" under the "library_management" database

create table book_list(
	book_id VARCHAR(10) NOT NULL,
	book_name VARCHAR(50) NOT NULL,
	author VARCHAR(50) NOT NULL,
	edition VARCHAR(10) NOT NULL,
	price Int(6) NOT NULL,
	qty Int(4) NOT NULL,
	PRIMARY KEY ( book_id )
);

☛Create a table "borrow_record" under the same database
create table borrow_record(
	book_id VARCHAR(10) NOT NULL,
	book_name VARCHAR(50) NOT NULL,
	stu_roll VARCHAR(15) NOT NULL,
	stu_name VARCHAR(50) NOT NULL,
	course VARCHAR(10) NOT NULL,
	subject VARCHAR(30) NOT NULL,
	issue_date date NOT NULL,
	return_date date NOT NULL
);
