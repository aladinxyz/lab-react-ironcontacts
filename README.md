![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | React IronContacts

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
