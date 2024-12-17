# Project Report

## Introduction

Our team consists of the following members:

- **[Yihsin Chiang]** - **[yic241]**
- **[Zhongyan Tang]** - **[zht34]**
- **[Yongjin Du]** - **[yod16]**
- **[Shuangyi Li]** - **[shl369]**

We developed a web application aimed at **creating a recipe-sharing platform**. The application enables users to **upload their recipes and food photos, search for recipes, view detailed instructions, click like buttons, and leave comments on recipes**.

---

## Objective

The primary objectives and goals of this project were:

1. **Solve a problem**: Provide a platform for **users to share, discover, and interact with food recipes conveniently**.
2. **Learning Goals**: Learn and apply technologies such as **Node.js, Express.js, MongoDB, ejs, and Bootstrap**.
3. **Additional Features**:
   - Implemented **photo uploads using base64 encoding** to display images.
   - Added **like and comment functionalities** to allow user interaction.
   - Introduced **most liked recipe display** to showcase the top recipes.
   - Implemented a **daily random recipe feature** for user discovery.
   - Added **categorization of recipes** into Breakfast, Lunch, and Dinner based on user input.

---

## Team Members' Contributions

- **[Yihsin Chiang]**:
  - Worked on **backend API development using Express and MongoDB**.
  - Developed **user authentication, role management, and password hashing**.
- **[Yongjin Du]**:
  - Implemented **frontend recipe components using React**.
  - Added **responsive design using Bootstrap and frontend integration**.
- **[Zhongyan Tang]**:

  - Designed the **database schema** for `User`, `Recipe`, `Like`, and `Comment` models.
  - Worked on **comment and like functionality with thorough API testing using Postman**.

- **[Shuangyi Li]**:
  - Developed **logic for most liked recipes and daily random recipe features**.
  - Implemented **categorization of recipes** into Breakfast, Lunch, and Dinner.

---

## Technical Architecture

We used the following technologies and libraries:

- **Frontend**: React.js, Bootstrap
- **Backend**: Node.js, Express.js
- **Database**: MongoDB (with Mongoose)
- **Authentication**: bcrypt for password hashing
- **Additional Tools**: Postman for API testing, Glitch for deployment

### MVC Model Breakdown:

- **Models** (stored in `models/`):
  - `User.js` - Handles user account data, including roles, authentication, and hashed passwords.
  - `Profile.js` - Stores user details such as name, photo, and introduction.
  - `Recipe.js` - Manages recipes, including description, ingredients, instructions, and base64-encoded photos.
  - `Comment.js` - Stores user comments linked to recipes.
  - `Like.js` - Tracks likes on recipes and comments.
  - `RecipeUser.js` - Links recipes and users for many-to-many relationships.
- **Views** (stored in `views/`):
  - `index.ejs` - Main page displaying the recipe list.
  - `add_recipe.ejs` - View to add new recipes.
  - `recipe.ejs` - Displays detailed recipe information, likes, and comments.
  - `profile.ejs` - User profile view for managing personal information.
  - `admin.ejs` - Admin dashboard for managing users and recipes.
  - `search.ejs` - Search page for finding recipes.
  - `login.ejs` and `register.ejs` - Authentication views for user login and registration.
- **Controllers** (stored in `routes/`):
  - `admin.js` - Handles admin-related functionalities.
  - `users.js` - Manages user accounts, including registration and login.
  - `recipes.js` - Manages recipe-related operations such as create, update, and delete.
  - `profile.js` - Handles profile data for users.
  - `index.js` - Main route for serving views and integrating logic.

---

## Challenges

We faced the following challenges:

1. **Base64 Encoding**: Handling and storing images in MongoDB required careful management to ensure performance.
2. **Authentication**: Implementing secure password hashing and role-based access control using bcrypt.
3. **Frontend-Backend Integration**: Debugging issues with API calls and React state management.
4. **Auto-Categorization**: Creating a reliable mechanism to categorize recipes dynamically into Breakfast, Lunch, and Dinner.
5. **Time Constraints**: Limited time restricted us from implementing advanced features, such as **real-time notifications**.

---

## Future Work

If given more time, we would like to:

1. Add **real-time notifications** for comments and likes using WebSockets.
2. Implement **pagination and search functionality** for recipe browsing.
3. Improve **user photo upload** using third-party storage solutions like AWS S3.
4. Enhance the **auto-categorization logic** to allow user-defined categories.
5. Add a **recipe rating system** to complement the like feature.
6. Enhance the UI/UX with animations and additional Bootstrap features.

---

## Conclusion

Through this project, we gained hands-on experience with:

1. **Full-stack web development** using Node.js, React, and MongoDB.
2. Implementing **secure user authentication** and managing complex data relationships.
3. Understanding the **MVC architecture** and how to design scalable web applications.

We believe this project deepened our understanding of modern web technologies and frameworks, providing skills we can apply to future projects.

---

## Resources

1. MongoDB Documentation: [https://docs.mongodb.com](https://docs.mongodb.com)
2. Express.js Guide: [https://expressjs.com](https://expressjs.com)
3. React Docs: [https://reactjs.org](https://reactjs.org)
4. bcrypt Tutorial: [https://www.npmjs.com/package/bcrypt](https://www.npmjs.com/package/bcrypt)
5. Bootstrap Guide: [https://getbootstrap.com](https://getbootstrap.com)
6. Postman API Testing: [https://www.postman.com](https://www.postman.com)

---

## Testing Instructions

To test the application functionality:

1. Clone the project repository from **https://github.com/EasonJiang94/RecipeSharingProject.git**.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the server:
   ```bash
   npm start
   ```
4. Access the application at `http://localhost:3000`.
5. Test APIs using Postman:
   - User authentication endpoints: `POST /login`, `POST /signup`
   - Recipe CRUD endpoints: `GET /recipes`, `POST /recipes`, etc.
   - Test **most liked recipes** and **daily random recipe** endpoints.

For additional details, refer to the project README.md.

---

_This report was written in Markdown and saved as `Report.md`._
