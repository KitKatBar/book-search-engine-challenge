# Book Search Engine Challenge - Never Get Lost In A Bookstore Again!
  
## Description

Most modern websites are driven by two things: data and user demands. This shouldn't come as a surprise, as the ability to personalize user data is the cornerstone of real-world web development today. And as user demands evolve, applications need to be more performant.

The application that I have built this week is a fully functioning Google Books API search engine built with a RESTful API which has been refactored to be a GraphQL API built with Apollo Server.  The app was built using the MERN stack, with a React front end, MongoDB database, and Node.js/Express.js server and API. It's already set up to allow users to save book searches to the back end.
        
## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)
- [How to Contribute](#how-to-contribute)
- [Questions](#questions)


## Installation

No installation is required! This code has been deployed to Netlify so that you can view it on your own device. To do so, please visit the following link: https://book-search-engine-challenge.onrender.com

## Usage

This project performs CRUD operations that interacts with the Google Books API search engine and a users database in MongoDB. The operations of this application are very simple!  You can create a user, read the user's list of saved books, update the user's list of books by choosing a book to add, and delete a book from the user's list of saved books.

Additionally, the Google Books API search engine reads in a search string and updates the render display with matching books.  However, this isn't stored in the database so it is not part of the MongoDB operations.

When you first load the application, you will see a header with the navigation bar texts 'Google Books Search', 'Search For Books' and 'Login/Sign Up'.  There will also be some large text and an entry box where you can type in the name of a book to search for and a button that lets you summit your input.

[!image showing the homepage when it is first loaded](https://github.com/KitKatBar/book-search-engine-challenge/blob/main/images/homepage-initial.png?raw=true)

Navigating to 'Google Books Search' or 'Search For Books' does nothing because they redirect you to the homepage, which you are already on.  Attempting to search for books while not logged in will yield search results, but you won't be able to save any of these books.

[!image showing what happens if you search for books while not logged in](https://github.com/KitKatBar/book-search-engine-challenge/blob/main/images/search-books-not-logged-in.png?raw=true)

When clicking on the 'Login/Sign Up' button, a modal will appear that lets the user login or sign up with an account.

[!image showing the login modal](https://github.com/KitKatBar/book-search-engine-challenge/blob/main/images/login-modal.png?raw=true)

[!image showing the sign up modal](https://github.com/KitKatBar/book-search-engine-challenge/blob/main/images/sign-up-modal.png?raw=true)

Since we don't have an account yet, lets sign up for one.  The form takes in the fields of a 'Username', 'Email' and 'Password'.  There are some minor validations on the 'Username' and 'Email' fields.  Both the 'Username' and 'Email' must be unique (meaning no one else has already registered with it) and the 'Email' uses a regex pattern to ensure that it is in the required format similar to something like 'your-name@your-domain.com'.  Attempting to submit the form with validation errors will result in a failed message.  While the error message should be more specific (I didn't write this so don't blame me), for demo purposes it is good enough for the time being.

[!image showing an error message when signing up with validation errors](https://github.com/KitKatBar/book-search-engine-challenge/blob/main/images/sign-up-error.png?raw=true)

Note that logging in with the wrong credentials will also display the same error message.

Once you have signed up, you will automatically be logged in and you'll see that your navigation bar has slightly changed.  There is an additional link to 'See Your Books' and the 'Login/Sign Up' will be replaced with a 'Logout'.

[!image showing the homepage when logged in](https://github.com/KitKatBar/book-search-engine-challenge/blob/main/images/homepage-logged-in.png?raw=true)

When you search for books, you'll now see that you have the option to save these books.

[!image showing what happens if you search for books while logged in](https://github.com/KitKatBar/book-search-engine-challenge/blob/main/images/search-books-logged-in.png?raw=true)

When you click on the 'Save this Book!' button, this book will get added to your list and it will be replaced with text reading 'This book has already been saved!' which is tinted out and cannot be interacted with.  This is to prevent having duplicate books added to your list.

[!image showing what happens when you save a book](https://github.com/KitKatBar/book-search-engine-challenge/blob/main/images/search-books-saved.png?raw=true)

When you navigation to the 'See Your Books' tab now, you'll see that the books you have saved appear in the list.  There will also be a 'Delete this Book!' button which allows you to delete the book and remove it from your list.  You can add it again if you wish.

[!image showing all your saved books](https://github.com/KitKatBar/book-search-engine-challenge/blob/main/images/saved-books.png?raw=true)

That's pretty much a detailed look at all the functionalities that this application offers so I hope you enjoy playing around and tinkering with it!

## Credits

MongoDB Atlas Setup Guide: https://coding-boot-camp.github.io/full-stack/mongodb/how-to-set-up-mongodb-atlas

Deploying on Render Using MongoDB Atlas Guide: https://coding-boot-camp.github.io/full-stack/mongodb/deploy-with-render-and-mongodb-atlas

Our instructor Drew Hoang for introducing us to MERN Stack and State this week.  It is interesting to see all these technologies come together (MongoDB, Express, React & Node) and how they can work with each other to create a web application.  It is also nice to have authentication to protect your application and also track your login state so you don't have to keep logging back in every time.  Additionally, he provides good metaphors for how to do exercises and also makes speed-run videos that are very insightful for providing information and for reviewing class material.

Our TA Kyle Vance for his continued guidance during class and taking the time to explain new concepts. He continues to provide direction for students and is straight to the point in his explainations.  He also spends so much time outside of classes to help students get thru the module challenges or even work on the projects, especially this past week!  I cannot express how much gratitude I have for him to give up his weekends helping out everyone!

Reyn Takahashi for providing a reference to his code since he was the driver (shared his screen) and worked closely with Kyle and we all just followed along in the Zoom calls.

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
This project was built using the MIT License. Please refer to the LICENSE in the repo for more information.
          
## How to Contribute

You can contribute to this project by providing better error messages for each circumstance instead of the same message for every error occurrence!

## Questions

This project was created by KitKatBar.
    
Click on [this link](https://github.com/KitKatBar) to see more of my other works!

Have additional questions about this project?  You can reach out to me with any inquiries at: katriel_chiu@msn.com