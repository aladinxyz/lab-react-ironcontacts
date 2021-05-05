![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | React IronContacts

## Introduction

After Ironhack, you have decided to work in the movie industry, and you've found a job where you need to manage the contacts of a famous producer.

We are going to create a contact management app with React for this producer.

<!-- You can find the starter code in the starter code folder of this GitHub repo. -->

## Setup

- Fork this repo
- Clone this repo

```shell
$ cd lab-react-ironcontacts
$ npm install
$ npm start
```

## Submission

- Upon completion, run the following commands

  ```
  git add .
  git commit -m "done"
  git push origin master
  ```

- Create Pull Request so your TAs can check up your work.

## Instructions

### Iteration 1 | Display 5 Contacts

Let's take a look at the starter code.

Inside `src` folder, we can find `contacts.json`, a JSON file with the producer's contacts. Import this file and **create an array of the 5 first contacts** to use as your initial state.

Display that array of 5 contacts in a `<table>` and display the `picture`, `name`, and `popularity` of each contact.

For now, let's add all the code to `App.js`. This being said, don't proceed to create a dedicated component to render the contact list. This will become a bit more clear later when we add the delete button next to each contact. Unless you are already familiar with the concept of "lifting state up", you won't be able to actually remove contacts so having the whole code in one component that actually renders the contacts, allows us to mitigate this even if we are not using the lifting state up approach.

Let's proceed.

To import `contacts.json` in `App.js`, you can simply use:

```js
import contacts from "./contacts.json";
```

At the end of this iteration, your application should look like this:

<details>
  <summary> Check image inside </summary>

![Screenshot](https://i.imgur.com/fPuwZXv.png)

</details>

### Iteration 2 | Add New Random Contacts

In your application, create an _Add Random Contact_ button so that every time you click on this button, it adds a new random actor.

First, randomly select a contact from the larger `contacts` array. Then add that contact to the array that lives in your state (that's the previously created array of 5). Don't forget to `setState()` to cause React to re-render the app.

At the end of this iteration, your website will probably look like this:

<details>
  <summary> Check image inside </summary>

![Screenshot](https://i.imgur.com/GuNyYiU.png)

</details>

### Iteration 3 | Sort Contacts By Name And Popularity

The producer asked you to add two new buttons to help them sort their contacts. When you click on one of the buttons, it should **sort the table by `name`** (alphabetically) and when you click the other, it should **sort by `popularity`** (highest first).

Don't forget to `setState()` after you sort!

This is what you may have at the end of this iteration:

<details>
  <summary> Check image inside </summary>

![Screenshot](https://i.imgur.com/vUDGZ7Y.png)

</details>

### Iteration 4 | Remove Contacts

The producer also would like to remove some of their contacts. Implement a _Delete_ button on each row of your `<table>` that will let the user remove the contact they clicked.

When they click, you should get the id of that actor and use it to remove the contact from the array. Don't forget to `setState()` after you remove the contact!

At the end of this iteration, your app may look like this (after playing a little bit with the _Delete_ button):

<details>
  <summary> Check image inside </summary>

![Screenshot](https://i.imgur.com/N3K1K1k.png)

</details>

### Iteration 5 | Bonus | Styling

Unfortunately, this contact list isn't production-ready. This is the movie business! It has to sparkle! Add some beautiful CSS to make the app "pop".

Happy coding! :heart:
