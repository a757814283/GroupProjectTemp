# GroupProject_Group64_381

Group: 64
Name: 
Deng Haoyang(13183789)
HE Haoran(13269272)
WU Fei(13327704)

Application link:https://groupproject-group64-381.onrender.com/

********************************************
# Register
Through the registration interface, each user can register his account and enter the library management system by entering the username and password.

If so, the “User Name Already Used” will be displayed.

Each user has a username and password;
Example
[
	{userid: user1, password: 123},
	{userid: user2, password: 456},
	{suerid: user3, password: 789}

]

********************************************
# Login
Through the login interface, each user can enter the book management system by entering the user name and password.

If you are not registered, the “Wrong Username or Password” will be displayed.

If you have registered, you will enter the main page after successful login.

After successful login, userid is stored in seesion.

********************************************
# Logout
In the home page, each user can log out their account by clicking logout.

********************************************
# CRUD service
- Add new
The add new link in index.ejs, when clicked, takes you to createbook.ejs
-	A book document  contain the following attributes: 
	1)	title: String,
   	2)	author: String,
	3)	year: Number

All properties are required

Add book button is post request, and all information is in body of request.

When the key is clicked, the received data is assigned to a new book object, saved, and then directed back to the index.ejs

********************************************
# CRUD service
- Read
-  There are two options to read and find book list all information or searching by book id.

1) List all information
index.ejs will be displayed with all book object;


2) Searching by book information
Input the book author or book year to be searched, and display the input in the index. ;
Click the search button in index.ejs,Get the data through get.Assign it to a new book object, query according to the object properties.;
If there is a result, output the book object to the search_result.ejs page for rendering;


********************************************
# CRUD service
- edit
Go to edit.ejs after clicking the edit link next to the book. 

In this page, the user can update the book information, and in the above properties, all the properties can be changed.

 After the changes are made, the new data is saved and directed back to the index page

-	A book document  contain the following attributes: 
	1)	title: String,
   	2)	author: String,
	3)	year: Number

********************************************
# CRUD service
- Delete
-	The user can delete the book information through the delete buttons.

********************************************
# RESTful
In this project, there are three HTTP request types, post, get .
- Post:

  - Create:	/api/books/add

![image](https://github.com/a757814283/GroupProject_Group64_381/assets/31002826/1a163e4e-80b3-41ab-ad40-2b162bdeb0aa)
USEAGE: POST /api/books/add
Body: x-www-form-urlencoded: { title: 'title', author: 'author', year: 'year' }

 - Delete:	/api/books/delete/:id

![image](https://github.com/a757814283/GroupProject_Group64_381/assets/31002826/d746565a-9d02-4895-bcc7-42ccc6f22840)
USEAGE: POST /api/books/delete/id

 - Update:	/api/books/update/:id

![image](https://github.com/a757814283/GroupProject_Group64_381/assets/31002826/c4ea03d5-c4b0-40f4-bc49-045ec9997815)
USEAGE: POST /api/books/update/id
Body: x-www-form-urlencoded: { title: 'title', author: 'author', year: 'year' }

- GET:

 - List: /api/books

![image](https://github.com/a757814283/GroupProject_Group64_381/assets/31002826/2189fcdd-1f9b-420c-bfba-9475aefacbef)
USEAGE: GET /api/books/

- Search:  /api/books/search?

![image](https://github.com/a757814283/GroupProject_Group64_381/assets/31002826/71a062d0-bd14-4769-a4a8-4f3206e98a9d)
USEAGE: GET /api/books/search?author=AuthorName&year=2023


