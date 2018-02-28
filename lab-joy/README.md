# Lab 31 - Budget Tracker
Joy Hou, Feb 26, 2018

## Problem Domain
We are using React and Redux to create a budget tracker application where we can create, update, and delete budget items.

## Components
### src/components/app/index.js
The App component creates a store and passes it as a prop into Provider for Redux, and also sets the route for the default path "/" to the Dashboard component. The main module renders this App component to the DOM.

### src/components/dashboard/dashboard.js
The Dashboard component renders the main page of the app and is displayed at the "/" route. It uses react-redux's connect to map state and dispatchable methods to props, displays a CategoryForm for adding categories to the app state, and displays a CategoryItem for each category in the app state.

### src/components/category/category-form/category-form.js
The CategoryForm component handles change and submit of the form to create a new budget item. It uses an onComplete prop to be a function that is invoked when the CategoryForms state when the form is submitted. It uses a buttonText prop to determine the submit button's text. It also uses a category prop that initializes the state of the form.

### src/components/category/category-item/category-item.js
The CategoryItem component handles editing and deletion of each category item, and uses react-redux's connect to map state and dispatchable methods to props. Each item displays the category's name and budget amount as well as a delete button. When the category item is double clicked, a CategoryForm is displayed to update the item onComplete.