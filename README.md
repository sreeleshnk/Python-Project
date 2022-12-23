------------------------------------------------------------------USED BOOK STORE MANAGEMENT SYSTEM------------------------------------------------------


INTRODUCTION
Used Book Management System is a Book store where users can search, request and buy used books for price lesser than the new books, the administrator handles the entire system. JavaScript and CSS are used to design the front end of the website and python for the backend requirements. DBSQLite is used as the backend database. The used book management system is a very simple website to handle. All clients have the option to request a book that is not on the books list in addition to purchasing books from the list of books that is readily available to them. An existing book may be removed from the list or added by the bookshop administrator. The administrator can view every book that a user has requested and work to make it available. The administrator can also view a list of all clients and their orders. Additionally, a number of filters are used to make the process of obtaining the books easier. The Python API is used to accomplish each of these functionalities. For various functionalities, the front-end makes calls to the Python API, and the Python API responds with the necessary answer. The information seen on the website is kept in a DBSQLite database and is retrieved, updated and deleted using the Python API.
In the system, Django Inbuilt Authentication is used. These secure APIs allow for the insertion, retrieval, and deletion of sensitive user data. The API receives a header for authorization that is backed by a password. The request will be processed further if it matches, and it will be discarded otherwise.

PROJECT OVERVIEW

Home Page:
A basic navigation bar and a carousel are made. Three images are added in the carousel. There are two main sections in the home page which are user sign-up and login.
 


Sign-Up Page:
The users who are visiting for the first time have to register from the Sign-up page. Here the users have to enter their First name, Last name, Username, a valid email and have to enter the password twice for authentication of the password. Later this password and the username will be used for authentication.
 
Login Page:
Once a user completes the registration (sign-up) process, the user can login on this login page using their credentials, which will authenticate and validate the username and password in the connected database. If the user credentials are correct then the user will sign in to the main page
 
Main Page:
After the Login process is completed, the user gets redirected to the main page, where they can see the list of books available. In the main page there is a drop down from which users can access the “request a book” page. Users can also logout using the logout button given in the top right-hand corner. In this main page users can see the details of the book like Book name, Author, Category, Price, Stock, Add to Cart and Quantity.
Users can click on buttons in the Add to cart section and choose the quantity which they want in the quantity section. Once the book has been added to the cart, in the top we can see the number of books added in the cart and if we click the cart we will be redirected to the cart. In the top beside the logout button there will be a text that welcomes the user with their name.

Cart:
After selecting the book, it will reflect in the cart option, by clicking the cart option the user is redirected to the cart and checkout page. Cart is connected to the checkout page so that a user can check out with the selected books from the website. The checkout process consists of billing details and payment methods. In billing details, the user needs to add full name, email address, contact number and address. There is a dropdown menu for the users to select the desired payment method and place order. A pop up will appear when the order is complete.
 
Users:
In the users drop down menu, there is a request for books option where the desired books can be requested by the users. A user can just give the book and author name in order to complete the request. Once the request is done a pop up appears showing the message that the user will be contacted once the book is available.
 
Admin:
Here is the built-in Django admin interface, where the admin can do actions like create, read, update and delete on all the tables. In the Admin panel admin can look into the users list of ordered books, can add new books and see the requested books by the users.

ARCHITECTURE:

The user initiates the flow. The internet user browses the web page. The server receives the request. The request then goes to the Django application, where it first goes to the urls functions, where it matches a url pattern to the user-entered url, then it goes to the views function, where it calls the matched function, then it integrates the respective models, which performs operations within the database, returns templates with static files, and finally displays to the output to the user.

TECHNOLOGIES USED:

1.	Backend Technologies 
• Python
• Django 
2.	Database Technologies 
• MySQLite
3.	Frontend Technologies 
• HTML
 • CSS
 • Javascript 
• Bootstrap
4.	Version Control 
• Git 

IMPLEMENTATION:

Project Structure
There are two main folders in the project namely Books and projectname. The Book folder consists of frontend files such as static, templates and other python files. Front End Link for homepage was taken from: https://www.free-css.com/free-css-templates/page282 and for Login page: https://startbootstrap.com/template/sb-admin. The URL used for calling python API is also present inside the Book folder.
In order for the API to retrieve and insert data into the tables, the database was designed and entries were made into tables. Testing was done to ensure that the API was operating properly after it had been successfully created. The code was then added to the GIT repository.

VERSION CONTROL

For version control and collaboration, we used Github. All the code was committed on the Git which helped us keep track of all the files and collaborate with each other remotely. All changes to the code and project over the time are available in the GIT.
 
DATABASE:

The website has four tables that are related to each other. The database was developed to store, update, delete and fetch the data for the website. We utilized SQLite, a relational database that comes with Django by default and is capable of handling a sizable quantity of data for the website.

PRODUCTION DEVELOPMENT:

The production development of the project includes the following steps. 
1.  Setup GIT
•	https://github.com/sreeleshnk/Python-Project
2. Setup VS Code
●	Download the Windows setup for Visual Studio Code. Run the installer (VSCodeUserSetup-version.exe) after downloading it. Run the file after that; it won't take more than a minute.
●	Click "next" after agreeing to the terms.
●	Press the finish button once all requests have been accepted. The default installation location for VS Code is "C:usersusernameAppDataLocalProgramsMicrosoft VS Code."
●	Your installation will be successful.
●	Run the file in VS Code using command: python manage.py runserver

3.SQlite Installation:
●	Get precompiled binaries for Windows by first visiting the SQLite official website's download page. The downloaded file should appear in the Windows Downloads directory once the download is finished.
●	The downloaded file should then be extracted into the C:sqlite directory by performing a right-click on it.
●	Next, launch Windows CMD and enter the command to change the directory to C:sqlite:
cd C:\sqlite
●	Next, use the following command to confirm the SQLite version:
sqlite3.exe
●	The output that follows contains the SQLite version.

CONCLUSION:

We have effectively built a Bookstore Website with a suitable front-end and back-end using this Django project. The administrator of the entire bookshop can easily handle all the data while saving a ton of time and effort.

INDIVIDUAL CONTRIBUTIONS:

@sreeleshnk :
books/views.py (index, usersignup, user_login, admin, delete_book, add_Books, Request_books, see_requested_books, delete_requested _books, customers_list, orders_list, data_view, checkout)
books/forms.py (BookForm, RequestBookForm)
books/decorators.py (decorator, admin_or_user)
/static
db.sqlite(database configuration)

@sreejithraghavan070 : 
books/models.py (customer, book ,order, request_book)
books/urls.py (Path admin(index, usersignup, user_login, logout, admin, customers_list, add_Books, delete_book,see_requested_books, delete_requested_books, border_lis, data_view) customers(users,request_book, checkout))

@Suchit : 
books/templates.
Changes to the HTML, CSS codes which are suitable for front-end and back-end codes. Used Bootstrap for the project.

@shamal94 :
books/projectname/settings.py 
books/projectname/urls.py



