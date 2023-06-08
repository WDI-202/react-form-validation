# Form Validation App

This is a guide on how to create a Form Validation App using React. In this app, users can input their personal information in a form. The form will have different input fields like name, email, and password. The onChange event will handle the input fields, and each field will have its own state variable. The onSubmit event can be used to submit the form, display a success message, or handle form validation errors.

## Step 1: Setting Up the React App

1. Create a Github repository called `form-validation-app`, clone the repository down.
2. Create a new React app using the `npx create-react-app .` command inside the repository.
3. Navigate to the app's directory and open it in your code editor.

## Step 2: Create the Form Component

1. Create a `Components` directory in the `src` directory
2. Create a new file called `Form.js` in the `Components` directory.
3. Define the `Form` component in `Form.js`. Use `rfce` snippet.

## Step 3: Import React and useState

1. Import the `React` and `useState` modules at the top of `Form.js`.
2. Use the `useState` hook to create state variables for each input field (`name`, `email`, `password`).

## Step 4: Create the Form JSX

1. In the `return` statement of the `Form` component, create a `<form>` element to wrap the input fields.
2. Inside the form, create the input fields using the appropriate HTML tags (`<input>`, `<textarea>`, etc.).
3. Bind the value of each input field to its corresponding state variable using the `value` attribute.
4. Add an `onChange` event handler to each input field to update its state variable whenever the user types in the field.

## Step 5: Use the Form Component

1. Open the main `App.js` file.
2. Import the `Form` component at the top of `App.js`.
3. Inside the `App` component's `return` statement, use the `<Form>` component to render the form.

## Step 6: Test the input fields

1. Run `npm start` in your terminal
2. In your browser, `http://localhost:3000` test your inputs fields. Make sure the input field change as you type.
3. Check the React developer tool `Components` to see if the states are there.

## Step 7: Handle Form Submission

1. Add a submit button to the form using the `<button>` HTML tag.
2. Add an `onSubmit` event handler to the `<form>` element.
3. In the event handler function for the onSubmit, prevent the default form submission behavior using `event.preventDefault()`.
4. Perform any necessary form validation checks on the input data (Make sure all fields are filled in, email in email format, and password length should be between 6-12 in length) inside the event handler function.
5. Use the `useState` hook to create state variable for `errorMessage`, and `successMessage`.
6. If there are validation errors:
   - Update the state variables to indicate the specific validation errors for each field.
   - Display appropriate error messages to the user, indicating the validation errors.
7. If the form is valid:
   - Update the state variable to indicate a success message.

That's it! You have now created a Form Validation App using React. Users can input their personal information, and the form will handle input changes and form submission. Make sure to implement the form validation logic according to your specific requirements.

## Extra-Credits:

**Change to a Real Time Validation instead of Validation onSubmit**

- Add an error state variable for each input field. For example, you can create state variables such as nameError, emailError, passwordError, etc.
- Implement Validation and Update Error States in each of the onChange handlers to the corresponding input field. If the input is valid, set the respective error state to an empty string (''). If the input is invalid, set the respective error state to an appropriate error message.
- Display Error Messages below each input field, display the corresponding error message when it exists. For example, you can use a component or element to display the error message conditionally.
