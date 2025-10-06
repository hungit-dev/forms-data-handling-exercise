# User Management Exercise Instructions

This README contains instructions for extending the user management application as part of the exercise.

---

## Add User Details

Expand the User model we created to include more details. Implement the following fields and validations:

- **Email**  
  - Required  
  - Must be formatted properly  

- **Age**  
  - Optional  
  - Must be a number between 18 and 120  

- **Bio**  
  - Optional  
  - Maximum 200 characters  

> Don’t forget to update the view to display these new fields!

---

## Implement Searching

What if we want to search for a specific user in a list of thousands? We’ll need a new route and view that lets clients search our list of users.

1. Add a form with a **GET method** (in `createUser.ejs` or another view) which accepts a **name** or **email** (or both!).  
2. Create a new route `/search` which accepts a **GET request**.  
3. Add the search logic to your controller which searches your list for a matching user.  
   - **Note:** Form data sent via a GET request will not be available via `req.body`. You will need to use `req.query` instead.  
4. Your GET request should handle searching for the user and then render the search result.  
5. Display the search results in a new view: `search.ejs`.
