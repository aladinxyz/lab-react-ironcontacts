![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | React IronContacts

<details>
  <summary>
   <h2>Learning Goals</h2>
  </summary>

  This exercise allows you to practice and apply the concepts and techniques taught in class. 

  Upon completion of this exercise, you will be able to:

  - Use the `useState` hook to create state variables and add state to React components.
  - Use state variable setter functions to update state and trigger component re-render.
  - Use methods `map()` and `filter()` to render array data as a list of elements.
  - Use the `key` attribute in React components to set a unique key for each element in a list.
  - Remove items from a list.
  - Use operators `?` and `&&` to conditionally render content.
  - Create event handler functions to handle user interactions and browser events.
  - Create controlled components to manage the form inputs.

  <br>
  <hr> 

</details>

## Introduction

After Ironhack, you have decided to work in the movie industry, and you've found a job where you need to manage the contacts of a famous producer.

Your task is to create a contact management app for the producer using React.

## Setup

- Fork this repo

- Clone this repo

- Open the LAB and start:

  ```bash
  $ cd lab-react-ironcontacts
  $ npm install
  $ npm start
  ```


## Submission

- Upon completion, run the following commands:

  ```bash
  git add .
  git commit -m "done"
  git push origin master
  ```

- Create a Pull Request so that your TAs can check your work.


## Getting Started

Clean the `App.js` component so that it has the following structure:

```jsx
// src/App.js
import "./App.css";

function App() {
  return <div className="App"></div>;
}
export default App;
```

## Instructions

### Iteration 1 | Display 5 Contacts

Let's take a look at the starter code.

Inside the `src` folder we have a `contacts.json` file containing the producer's contacts. Import the `contacts.json` file to `App.js`. Once done, create a state variable named `contacts` and store an **array containing the first 5 contacts**.

Display that array of 5 contacts as a list in a `<table>` and display the `picture`, `name`, and `popularity` of each contact.

For now, let's render the content in `App.js`. This being said, don't proceed to create a dedicated component for the contact list. The reason will become a bit clearer later when we add the delete button next to each contact. You are probably not yet familiar with the concept of "lifting state up" and passing callbacks as props. For this reason, it is better to render everything in one component for the moment.

Let's proceed.

To import `contacts.json` in `App.js`, you can use:

```js
import contacts from "./contacts.json";
```

At the end of this iteration, your application should look like this:

<details>
  <summary> Check image inside </summary>

![Screenshot - Iteration 1](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-1.png)

</details>

### Iteration 2 | Conditionally Display Awards Info

The producer would like to see the information about the _awards_ that contact has won.

Update the list and add two more columns "Won an Oscar" and "Won an Emmy", at the end of the table. Then, depending on the value `wonOscar` and `wonEmmy` of each contact, conditionally render a trophy icon :trophy: or no content.

Once done, your application should look like this:

<details>

<summary>Check image inside</summary>

![Screenshot - Iteration 2](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-2.png)

</details>

### Iteration 3 | Add New Random Contacts

In your application, create a _Add Random Contact_ button. Every time you click on this button, it should add a new random contact to the `contacts`. You should get random contacts from the remaining contacts that are still not showing.

First, randomly select a contact from the array of remaining contacts. Then add that contact to the array that lives in your state (that's the previously created array of 5 contacts). Do not modify the state directly. Instead, use the state updater function returned from the `useState()`.

At the end of this iteration, your website will probably look like this:

<details>
  <summary> Check image inside </summary>

![Screenshot - Iteration 3](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-3.png)

</details>

### Iteration 4 | Sort Contacts by Name and Popularity

The producer asked you to add two new buttons to help them sort their contacts. When you click on one of the buttons, it should **sort the table by `name`** (alphabetically), and when you click the other, it should **sort by `popularity`** (highest first).

Once you have sorted the array, remember to update the state variable holding the contacts.

This is what you should have at the end of this iteration:

<details>
  <summary> Check image inside </summary>

![Screenshot - Iteration 4](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-4.png)

</details>

### Iteration 5 | Remove Contacts

The producer also would like to remove some of their contacts. Implement a _Delete_ button on each row of your `<table>` that will let the user remove the contact they clicked.

When they click, you should get the `id` of that actor and use it to remove the contact from the array. Remember to update the state variable holding the contacts after you remove the contact!

When done, your app should look like this (after playing a little bit with the _Delete_ button):

<details>
  <summary> Check image inside </summary>

![Screenshot - Iteration 5](https://education-team-2020.s3.eu-west-1.amazonaws.com/web-dev/labs/lab-react-ironcontacts-5.png)

</details>

### Iteration 6 | Bonus | Styling

Unfortunately, this contact list isn't production-ready. We are in the movie business! It has to sparkle! Add some beautiful CSS to make the app "pop".

Happy coding! :blue_heart:

<br>

## FAQs


<details>
  <summary>I am stuck and don't know how to solve the problem or where to start. What should I do?</summary>

  <br>

  If you are stuck in your code and don't know how to solve the problem or where to start, you should take a step back and try to form a clear question about the specific issue you are facing. This will help you narrow down the problem and come up with potential solutions.

  For example, is it a concept that you don't understand, or are you receiving an error message that you don't know how to fix? It is usually helpful to try to state the problem as clearly as possible, including any error messages you are receiving. This can help you communicate the issue to others and potentially get help from classmates or online resources. 

  Once you have a clear understanding of the problem, you will be able to start working toward the solution.

  <br>

  [Back to top](#faqs)

</details>

<details>
  <summary>I got the error: "Cannot find module 'Node.js'". How can I resolve it?</summary>

  <br>

  The error "Cannot find module" in a Node.js application means that the module you are trying to import or use does not exist in your project or cannot be found by Node.js.

  There are a few things you can try to resolve the issue:

  1. **Dependencies are not installed**: Make sure that all dependencies are installed.
   To do this, run the command `npm install` in the root folder of your project.
   This will install all of the dependencies listed in the project's `package.json` file, and ensure that all of the modules that your Node'js application requires are available.

  2. **Module is not installed**: Make sure that the *package* you are trying to use is listed in the project's `package.json` and that it is installed.
   To do this, run the command `npm install <package_name>`, replacing the `<package_name>` with the name of the package.
   This will add the package to the list of dependencies in the `package.json` file, and install it in the project.

  3. **Module is not imported:** Make sure that you've imported the module/package correctly and that the `import` statement is spelled correctly and available in the correct place in your code.

  4. **Wrong file path:** If you are importing another file as a module, make sure that the file you are trying to *import* is located in the correct folder and that you are using the correct file path.

  5. **Wrong module/package name:** Check the spelling of the package name you are trying to import.

  <br>

  [Back to top](#faqs)

</details>

<details>
  <summary>I got the message: "Something is already running at ... Would you like to run the app at another port instead? [Y/n]". What should I do?</summary>

  <br>

  This message means that another process is already using the specified port. This could be another instance of your React app, or it could be another application that is using that port.

  To resolve this, you can change the port your React app is running on by typing Y when prompted. This will kill the process and automatically start the server on another port.

  Another approach is to manually terminate the process using the port in question and then try running the app again.

  <br>

  [Back to top](#faqs)

</details>

<details>
  <summary>How do I display an <em>image</em> in a React component?</summary>

  <br>

  To display an image in a React component, you should first `import` the image in the component and then render it. Here is an example of how to do this:

  ```jsx
  import example from "./example.png"; // Import the image file

  function App() {
    return (
      <img src={example} alt="example" /> // Display the image
    )
  }

  export default App;
  ```

  In the above example, the `example` variable is assigned the value of the imported image file. The image is then displayed using the `<img>` element, with the `src` attribute set to the `example` variable.

  <br>

  [Back to top](#faqs)

</details>

<details>
  <summary>I got the warning in my React app:" 'variable' is assigned a value but never used: no-unused-vars". What should I do?</summary>

  <br>

  This warning is a linting error thrown by a linting tool in your React project, and it is warning you that the variable is created, but that it is never being used in your code.

  To resolve this issue, you can either use the variable in your code, or you can simply remove the variable if you don't need it.

  <br>

  [Back to top](#faqs)

</details>


<details>
  <summary>I got the warning: "Each child in a list should have a unique 'key' prop". How can I resolve it?</summary>

  <br>

  The warning *"Each child in a list should have a unique “key” prop"*  means that you are trying to render a list of elements, but one or more elements is missing the `key` prop.
  
  To fix this, add a `key` prop to each element you return from the `map()` when rendering the list. The key should be a unique identifier for that element, such as an item ID or the id of the document from the database.
  
  For example, if you have an array of objects with the following structure:

  ```js
  const projects = [
    { id: "127fae", name: "EatBCN", stack: "React, Express" },
    { id: "985afw", name: "Levels", stack: "React, Express" },
    { id: "347eef", name: "IronClub", stack: "React, Java" }
  ];
  ```

  <br>

  Inside your component, you would render the list in the following way:

  ```jsx
  {
    projects.map((el) => {
      return (
        <div key={el.id}>
          <h3>{project.name}</h3>
          <p> Tech Stack: {project.stack} </p>
        </div>
      
    })
  }
  ```

  In the above example, the objects in the `projects` array all have a common property `id`,  which is a unique id string, and therefore we can use it to set the `key` prop.

  When creating lists we must always assign the `key` prop to the outermost (enclosing) element returned from the `map()`, in this case the `div`. We are setting the `key` prop to each `div` element we render in the list.

  **Important**: You should not use *index* of the `map` as *key*. This is considered an *anti-pattern* that may lead to unpredictable results.

  <br>

  For more information, check: [React Docs - Rendering Lists](https://beta.reactjs.org/learn/rendering-lists#keeping-list-items-in-order-with-key)

  <br>

  [Back to top](#faqs)

</details>

<details>
  <summary>How to render a list of elements from an array in a React component?</summary>

  <br>

  To render a list of elements from an array in a React component, you can use the method `map()` to loop over the `projects` array and return JSX elements to be rendered. 

  To render a filtered list, where some items are skipped, you can use the `filter()` method.

  Each element returned should have a *unique* `key` prop assigned to them. It's important to note that the `key` prop should always be assigned to the outermost (enclosing) element returned from the `map()`.

  Here is an example of rendering a list of elements using the `map()` method:

  ```js
const projects = [
    { id: "127fae", name: "EatBCN", stack: "React, Express" },
    { id: "985afw", name: "Levels", stack: "React, Express" },
    { id: "347eef", name: "IronClub", stack: "React, Java" }
  ]

  function ProjectList() {
    return (
      <div>
        {
          projects.map((el) => {
            return (
              <div key={el.id}>
                <h3>{el.name}</h3>
                <p>Tech Stack: {el.stack}</p>
              </div>
            )
          })
        }
      </div>
    )
  }

  export default ProjectList;
  ```

  In the above code example, we use `map()` inside of the component to loop over the `projects` array, and for each project, return a `div` element with the `project.name` and the `project.stack` as its contents. 

  Each object in the `projects` array contains a common property `id` which we use as the `key` prop. 

  The `key` prop must be set on the outermost element returned from the `map()`, in this case, the `div` element.

  **Important**: You should not use *index* of the `map` as *key*. This is considered an *anti-pattern* that may lead to unpredictable results.

  For more information, check: [React Docs - Rendering Lists](https://beta.reactjs.org/learn/rendering-lists#keeping-list-items-in-order-with-key) 

  <br>

  [Back to top](#faqs)

</details>

<details>
  <summary>How do I update a state variable in my React component? How do I use the useState hook in my React component?</summary>

  <br>

  To update a state variable in a React component, you should use the `useState` hook. This hook returns an array with two elements: the **current value** of the state variable and a **function to update it**. Here is an example of how to use `useState` to update the `count` state variable:

  ```jsx
  import { useState } from "react";

  function MyComponent() {
    const [count, setCount] = useState(0);

    const handleClick = () => {
      setCount(count + 1);
    }

    return (
      <div>
        <button onClick={handleClick}> Increment </button>
        <p>Count: {count}</p>
      </div>
    )
  }
  ```

  In the above example, the `handleClick` function is called when the button is clicked, and it updates the `count` state variable by calling the `setCount` function with the new value: `setCount(count + 1)`. 
  The component will re-render every time a state variable gets updated.

  <br>

  [Back to top](#faqs)

</details>

<details>
  <summary>I am getting an error: "not defined". How do I fix it?</summary>

  <br>

  The "ReferenceError: variable is not defined" error in JavaScript occurs when you try to access a variable or a function that has not been defined yet or is out of scope. 

  To fix the issue, check that you have defined the variable or function that you are trying to use and double-check the spelling to make sure you are using the correct name.

  In case the variable or a function is defined in another file, make sure that the file has been imported or loaded correctly.

  <br>

  [Back to top](#faqs)

</details>

<details>
  <summary>I am unable to push changes to the repository. What should I do?</summary>

  <br>

  There are a couple of possible reasons why you may be unable to *push* changes to a Git repository:

  1. **You have not committed your changes:** Before you can push your changes to the repository, you need to commit them using the `git commit` command. Make sure you have committed your changes and try pushing again. To do this, run the following terminal commands from the project folder:

  ```bash
  git add .
  git commit -m "Your commit message"
  git push
  ```

  2. **You do not have permission to push to the repository:** If you have cloned the repository directly from the main Ironhack repository without making a *Fork* first, you do not have write access to the repository.
  To check which remote repository you have cloned, run the following terminal command from the project folder:

  ```bash
  git remote -v
  ```

  If the link shown is the same as the main Ironhack repository, you will need to fork the repository to your GitHub account first, and then clone your fork to your local machine to be able to push the changes.
  Note: You may want to make a copy of the code you have locally, to avoid losing it in the process.

  <br>

  [Back to top](#faqs)

</details>
