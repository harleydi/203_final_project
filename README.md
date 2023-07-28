# 203_final_project

## Overview

The WDI-200 Final Project will be used to guage whether or not a student is capable of semi-independent fullstack development. The project must be: created using the MERNstack (MongoDB, ExpressJS, ReactJS, and NodeJS), must include user login and registration functionality, and include core CRUD functionality (Create, Read, Update, and Delete).

The Final Project will be graded as follows. Implementation of the core requirements will constitute a passing grade. Implementation of all the core requirements with the stretch requirements will constitute a B grade. Implementation of core requirements, stretch requirements, and ANY super stretch requirement will constitute an A grade.

## Tech Stack

- [Required] Node - Runtime
- [Required] React - Client Framework
- [Required] Express - Server Framework
- [Required] MongoDB - Database
- [Required] Git - Code Versioning
- [Required] Github - Code Storage and Collaboration
- [Required] CORS - Express CORS Library
- [Required] bcryptJS - User Authentication
- [Required] JsonWebToken - User Auth Tokens
- [Suggested] Bootstrap - CSS Framework
- [Suggested] Nodemon - Server Hot Reloading
- [Suggested] React-Router - Client Side Routing
- [Suggested] JSDOC - Code Comment Framework
- [Suggested] uuidv4 - Unique ID Generator

## Requirements

### User Login and Registration

- [Core] 
  - A user should be able to register with the application.
  - A user should be able to login with the application.
	- The user's password should be encrypted via salt+hash algorithm.
	- A user ID Token should be generated using JsonWebToken. The ID Token should then be persisted on client side with local storage. The client should then check for the existence of the token before prompting the user to authenticate.
	- A user should be able to logout of the application and login with a different account.

### E-Commerce Store Server

- [Core]
	- RESTful API.
 	- Must have full CRUD functionalities. 	
	- The server should have a route that serves a list of products.
		- _Recommendation_: Get a list of products from the fakestore api and use those as the product list for this application. https://fakestoreapi.com/docs
	- The server should have a route that recieves a cart checkout request from the client. This route should create a new order document in the database. The order document should have its own ID, the ID of the user that checked out as well as the checked out cart items stored on it.
	
### E-Commerce Store Client

- [Core]
	- Navigation Bar	
		- The store should have a navigation bar that a user can use to navigate through the application pages.
	- Products Page
		- The store should have a products page that will display a list of store products fetched from the server. 
		- A user should be able to add a product from the products page to their cart.
	- Cart Page
		- A user should be able to see a list of products they added to their cart.
		- A user should be able to checkout with their cart. This should create a new order in the database with the user's cart info. 

- [Stretch] 
	- Navigation Bar	
		- The navigation bar should show the currently logged in user.
	- Products Page
		- The products page should be sortable and paginated.
		- The products page should have a search bar that will filter the products down to a specific result.
	- Cart Page
		- A user should be able to increment/decrement the quantity of each item in the cart.

- [Super-Stretch]
	- Profile and Order History Page
		- When a user completes checkout, the order ID should be pushed into an orderHistory array on the user document. 
		- The server should have a route that sends user information including a users order history. 
		- A user should be able to visit their profile page and see their user info. They should also be able to see their order history populated with orders.
		- A user should be able to input their profile info upon registration (name, phone, email, etc).
		- A user should be able to edit their profile information from the profile page. This will require an update route be created server-side to persist user data in the database.
	- Wishlist
		- A user should be able to generate a wishlist of products and save them in the database to a wishlist document.
		- A user should be able to navigate to a wishlist page that displays their wishlist of products.
		- A user should be able to generate a link that will share their wishlist with other users. I.E. A link is generated that has the id of a wishlist included in the url. The link should be able to be put into a new browser window and the wishlist of items should appear.
