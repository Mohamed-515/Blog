# Blog
Internship Development project 

Project Overview: Blogy
Blogy is a web application designed for creating, editing, and managing blog posts. The application allows users to log in, create posts, edit or delete their own posts, and like or dislike posts. It features a responsive design using HTML, CSS, and JavaScript, and utilizes localStorage to store user data and blog posts.

1. File Structure
blogs.html: The main page that displays blog posts and allows users to like, dislike, edit, or delete posts.
create_blog.html: A page for creating new blog posts.
edit_blog.html: A page for editing existing blog posts.
delete_blog.html: A page for deleting blog posts.
login.html: A page for user login.
signup.html: A page for user registration.
styles.css: The CSS file for styling the application.
2. Detailed Explanation of Each HTML File
blogs.html
Purpose: This is the main page where all blog posts are displayed. It allows users to view posts, toggle post descriptions, like/dislike posts, and edit or delete their own posts.
Key Components:
Header: Contains an image and navigation buttons for login, signup, and logout.
Admin Buttons: Buttons for creating, editing, and deleting blogs, visible only when a user is logged in.
Blog Section: Displays a list of all blog posts. Each post can be liked or disliked, and if the post belongs to the current user, edit and delete options are shown.
Scripts:
Handles login/logout status.
Renders blog posts by fetching them from localStorage.
Handles like and dislike functionality with logic to toggle user votes and update the display.
create_blog.html
Purpose: Allows users to create a new blog post by filling out a form with a title, content, and optional image URL.
Key Components:
Form: Collects blog details (title, content, image URL).
Scripts:
Validates the form inputs and saves the new blog post to localStorage.
Redirects to blogs.html after successful submission.
edit_blog.html
Purpose: Enables users to edit existing blog posts.
Key Components:
Form: Populates with existing blog post details for editing.
Dropdown: Allows selection of a blog post to edit.
Scripts:
Loads existing blog posts into a dropdown.
Updates the blog post in localStorage with new details upon submission.
Handles cases where the blog title already exists.
delete_blog.html
Purpose: Allows users to delete a blog post.
Key Components:
Form: Contains a dropdown menu to select a blog post to delete.
Scripts:
Loads blog titles into the dropdown.
Deletes the selected blog post from localStorage and updates the display.
login.html
Purpose: Provides a login form for users to authenticate.
Key Components:
Form: Collects email and password.
Scripts:
Checks the provided credentials against user data stored in localStorage.
Redirects to blogs.html upon successful login.
signup.html
Purpose: Allows new users to sign up by providing their details.
Key Components:
Form: Collects full name, email, and password.
Scripts:
Saves the new user's information to localStorage after validating the form.
3. Styling with styles.css
Provides consistent styling for all pages, including layout adjustments, color schemes, and button styles.
4. Key JavaScript Functions
checkLoginStatus(): Checks if a user is logged in and shows/hides the appropriate buttons.
renderBlogPosts(): Renders blog posts dynamically on the page, including event listeners for like/dislike buttons.
handleLikeDislike(action, index): Manages the logic for liking and disliking posts.
simulateLogin() and logout(): Functions to handle demo login/logout for testing purposes.
5. Data Storage
The project uses localStorage to store:
Users: An array of user objects (email, password).
Blog Posts: An array of blog objects (title, content, image, date, likes, dislikes).
User Votes: An object storing the like/dislike status for each post by user.
6. Features and Functionality
User Authentication: Sign up, login, and logout functionality.
Blog Management: Create, edit, and delete blog posts.
Voting System: Users can like or dislike posts, with vote toggling.
Dynamic Rendering: Blog posts and user actions are dynamically updated based on interactions.