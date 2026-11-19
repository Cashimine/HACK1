Build a responsive meal-planning web app called “Homemade.”

The app should allow users to generate a realistic seven-day meal plan using real meals and recipes. The user should be able to select preferences before generating the plan, including:

- Number of people
- Dietary preference: none, vegetarian, vegan, keto, low-carb, gluten-free
- Allergies or ingredients to avoid
- Meals per day: breakfast, lunch, dinner, and optional snacks
- Weekly grocery budget: a user-entered dollar amount
- Cooking skill level
- Maximum preparation time
- Ingredients the user already has

Core features:

1. Meal Plan Generator
- Generate a complete meal plan for the next seven days.
- Display each day in a clear card or calendar layout.
- Show the meal name, meal type, estimated preparation time, cooking time, servings, calories, and difficulty level.
- Use realistic meals with specific ingredients and detailed instructions.
- Avoid repeating the same meal unless the user allows leftovers.
- Include balanced meals with a variety of proteins, vegetables, grains, and other ingredients.
- Allow users to regenerate an individual meal without changing the rest of the week.
- Allow users to replace an entire day.
- Include a “Plan Next Week” or “Generate New Week” button.

2. Recipe Details
- When a user selects a meal, open a detailed recipe view.
- Display ingredients with quantities.
- Display step-by-step cooking instructions.
- Include preparation time, cooking time, total time, servings, difficulty, and nutrition information.
- Allow the serving size to be increased or decreased, automatically updating ingredient quantities.
- Add a button to mark a meal as a favorite.

3. Grocery List
- Automatically create a grocery list from all meals in the weekly plan.
- Combine duplicate ingredients and add their quantities together.
- Organize groceries into categories such as:
  - Produce
  - Meat and seafood
  - Dairy and eggs
  - Grains and bakery
  - Canned and packaged foods
  - Spices and sauces
  - Frozen foods
  - Other
- Allow users to check off purchased items.
- Allow users to add, edit, and delete grocery items.
- Include a “Clear completed items” button.
- Include print and download options.

4. User Interface
- Create a clean, modern, easy-to-use design.
- Use a responsive layout that works on desktop, tablet, and mobile devices.
- Include a navigation bar with:
  - Meal Plan
  - Recipes
  - Grocery List
  - Favorites
  - Settings
- Use clear buttons, readable typography, helpful icons, and accessible color contrast.
- Include loading states, empty states, success messages, and error messages.
- Make the interface beginner-friendly.

5. Data and Functionality
- Store meal plans, recipes, favorites, user preferences, and grocery list data using localStorage if no backend is available.
- Structure the code so a real recipe API or AI recipe-generation API can be added later.
- Create sample recipe data so the app works immediately.
- Validate all form inputs.
- Make sure grocery quantities are combined correctly.
- Make sure changing a recipe updates the grocery list.
- Preserve the current meal plan when the user refreshes the page.

6. Technical Requirements
- First inspect the existing project files and follow the current project structure.
- Use the existing framework and styling system if one is already present.
- If the project is empty, use HTML, CSS, and JavaScript or React with Vite.
- Separate the application into reusable components.
- Use semantic HTML and accessible form controls.
- Add comments explaining important logic.
- Do not use fake buttons or unfinished placeholder features.
- Make all major buttons and interactions functional.
- After implementation, test the app and fix layout or JavaScript errors.

Start by creating the main meal plan page and reusable components for meal cards, recipe details, preference forms, grocery categories, and navigation. Then implement the meal generation, recipe display, grocery-list combination, favorites, localStorage, and responsive styling.










Update the meal-planning app with the following features:

1. Shopping List Organization by Day
- Add a toggle that allows users to view the grocery list in either:
  - Combined weekly list
  - Separated by day
- When “Separated by Day” is selected, organize ingredients under headings such as:
  - Monday
  - Tuesday
  - Wednesday
  - Thursday
  - Friday
  - Saturday
  - Sunday
- Each ingredient should show its quantity and the meal it belongs to.
- Allow users to check off grocery items in either view.
- Keep checked items synchronized between the combined and daily views.
- Avoid duplicate ingredients within the same day.
- Preserve the selected shopping-list view after refreshing the page.

2. Favorites Difficulty Sorting
- Add difficulty information to every recipe: Easy, Medium, or Hard.
- Add difficulty filter buttons or a dropdown to the Favorites page.
- Allow users to sort or filter favorite meals by:
  - All difficulties
  - Easy
  - Medium
  - Hard
- Add an optional sort by recipe name, preparation time, or rating.
- Display the difficulty level clearly on each favorite recipe card.
- Show a helpful empty-state message if no favorite meals match the selected difficulty.

3. Meal Rating System
- Add a 0-to-5-star rating system to every recipe.
- Allow users to select ratings in whole-star increments, including 0 stars.
- Display the current user’s rating separately from the overall community rating.
- Calculate and display:
  - Average rating
  - Number of ratings
  - Visual star display
- Allow users to change their rating.
- Add accessible labels for the rating buttons so keyboard and screen-reader users can use them.
- Display ratings on meal cards, recipe-detail pages, favorites, and search results.
- Sort favorite meals by highest-rated or lowest-rated.
- If a meal has no ratings, display “No ratings yet.”

4. Shared Ratings and Data Storage
- Ratings must be visible to other users of the app, so do not store community ratings only in localStorage.
- If a backend is not currently available, create a clear data-service abstraction with sample shared rating data and explain where a real backend should be connected.
- If the project already uses a backend or database, store ratings with:
  - Recipe ID
  - User ID or anonymous user identifier
  - Rating value from 0 to 5
  - Date submitted
- Prevent one user from creating duplicate ratings for the same recipe.
- Update the average rating immediately after a rating is submitted or changed.
- Keep favorites and personal settings in localStorage if appropriate, but treat community ratings as shared database data.

5. Technical Requirements
- Inspect the existing project before making changes.
- Reuse the current components, styling, and data structures whenever possible.
- Create reusable components for:
  - Shopping-list view toggle
  - Daily grocery-list sections
  - Difficulty filter
  - Star-rating control
  - Rating summary
- Make sure changing a meal, regenerating a meal, or deleting a meal updates the shopping list and ratings correctly.
- Make the new features responsive on desktop, tablet, and mobile screens.
- Add loading, error, and empty states.
- Test all buttons, filters, rating controls, localStorage behavior, and responsive layouts.
- Do not replace working features or create nonfunctional placeholder buttons.
