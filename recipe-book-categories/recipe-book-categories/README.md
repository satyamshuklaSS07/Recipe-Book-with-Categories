# Whisk — Recipe Book with Categories

A responsive personal recipe book built with **HTML, CSS, and vanilla JavaScript**. Add, edit, view, search, sort, filter, and delete recipes. Your collection is stored in the browser with `localStorage`.

## Features
- Full recipe CRUD (create, read, update, delete)
- Categories: Breakfast, Lunch, Dinner, Dessert, and Snacks
- Search recipes by name, category, or ingredients
- Sort by recently added, name, or prep time
- Recipe detail view with ingredients and method
- Optional image URL for each recipe
- Confirmation before deleting
- Local persistence with `localStorage`
- Responsive layout and light/dark theme toggle
- Six sample recipes included on first launch

## Run locally
1. Download or clone this repository.
2. Open `index.html` in a browser.
3. Add a recipe using **New recipe**. Your data stays in that browser on that device.

No build tools or dependencies are required. Google Fonts are optional; the page uses fallback fonts if offline.

## Data structure
Each recipe is stored as an object with a unique `id`, `name`, `category`, `time`, `image`, `ingredients`, `instructions`, and `created` timestamp. The full array is serialized into `localStorage` under `whisk-recipes-v1`.

## Interview questions
1. **What is CRUD?** Create, Read, Update, and Delete—the four basic operations used to manage records.
2. **Why use `localStorage`?** It keeps small amounts of data in the browser across refreshes without needing a backend. It is device- and browser-specific.
3. **How are recipes filtered by category?** The app filters the recipe array against the selected category before rendering the cards.
4. **How does the search work?** It normalizes the query to lowercase and checks the recipe name, category, and ingredients.
5. **Why does every recipe need a unique ID?** An ID lets the app update or delete one exact recipe without confusing it with another recipe that has the same name.
6. **What is one limitation of this project?** Data is not synced across devices and can be cleared with browser storage. A backend would be needed for accounts and cloud sync.

## Project structure
```text
recipe-book-categories/
├── index.html
├── style.css
├── script.js
└── README.md
```
