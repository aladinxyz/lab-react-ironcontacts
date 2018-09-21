![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# IronContacts

## Introduction

After Ironhack, you have decided to work in the movie industry and you've found a job where you need to manage the contacts of a famous producer.

We are going to create contact management app with React for this producer.

You can find the starter code in the starter code folder of this GitHub repo.

## Submission

- Upon completion, run the following commands

  ```
  git add .
  git commit -m "done"
  git push origin master
  ```

- Create Pull Request so your TAs can check up your work.



## Installation

```
$ cd starter-code
$ npm install
$ npm start
```


## Instructions

### Iteration 1 | Display 5 Contacts

Let's take a look at the starter code.

Inside `src` folder, we can find `contacts.json`, a JSON file with the producer's contacts. Import this file and **create an array of the 5 first contacts** to use as your initial state.

Display that array of 5 contacts in a `<table>` and display the `picture`, `name`, and `popularity` of each contact.

To import `contacts.json` in `App.js`, you can simply use:

```js
import contacts from './contacts.json'
```

At the end of this iteration, your application should look like this:

![Screenshot](https://i.imgur.com/fPuwZXv.png)


### Iteration 2 | Add New Random Contacts

In your application, create a "*Add Random Contact* button so that every time you click on this button it adds a new random actor.

First randomly select a contact from the larger `contacts` array. Then add that contact the array of 5 in your state. Don't forget to `setState()` to cause React to re-render the app.

At the end of this iteration, your website will probably look like this:

![Screenshot](https://i.imgur.com/GuNyYiU.png)


### Iteration 3 | Sort Contacts By Name And Popularity

The producer asked you to add two new buttons to help them to sort their contacts. When you click on one of the buttons it should **sort the table by `name`** (alphabetically) and when click the other it should **sort by `popularity`** (highest first).

Don't forget to `setState()` after you sort!

This is what you may have at the end of this iteration:

![Screenshot](https://i.imgur.com/vUDGZ7Y.png)


### Iteration 4 | Remove Contacts

The producer also would like to remove some of their contacts. Implement a "*Delete*" button on each row of your `<table>` that will let the user remove the contact they clicked.

When they click, you should get the index of the array of that actor and use it to remove the contact from the array. Don't forget to `setState()` after you remove the contact!

At the end of this iteration, your web page may look like this after playing a little bit with the "*Delete*" buttons.

![Screenshot](https://i.imgur.com/N3K1K1k.png)


### Iteration 5 | Bonus | Styling

Unfortunately, this contact list isn't really production ready. This is the movie business! It's got to sparkle! Add some nice CSS to make the app "pop".


Happy coding! :heart:

