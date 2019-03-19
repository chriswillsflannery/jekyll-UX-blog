---
layout: post
title:  "To-Do List App with Gatsby + React"
date:   2019-03-17 14:48:23 -0500
categories: React
---
Disclaimer: I am brand new to development and developer terminology! At best, this post will probably come off as a whole bunch of garbled nonsense but I hope that in the future I can come back and reference it and it will help me clear up any questions I might have when working in Gatsby. If you have any questions, feel free to email me at: chriswillsflannery@gmail.com

-

With help from V School's "Learn React for Free" Scrimba video series, I created a to-do app built with Gatsby and React. It runs in the browser and is customizable to the user's needs within the React code. You can view the finished product here:

[https://relaxed-mcclintock-495015.netlify.com/](https://relaxed-mcclintock-495015.netlify.com/)

This is one of the first React apps I've built, and has served as a learning experience in my javascript/React journey. Something worth mentioning is that Gatsby is a site-generator framework for React, and functions basically as a Bootstrap-type software built using a React hierarchy. The project structure is a little different than your generic `create-react app`; it comes with an Index.js file which is basically the top level component, and several child components like Layout.js, Header.js, and SEO.js, which pass information up to Index. In the Index.js file, I imported and referenced a new file, App.js, which I created within the pre-built Components folder. App.js is where I built the actual to-do app.

App.js has several child components; TodoItem.js (which contains the template for a single to-do item), and todoItems.js, which is an array containing several objects; each object contains text data for individual to-do items and the whole component is a hard-coded representation of API data (which I have not yet learned how to implement in React.)

How App.js works:

`import React from "react"
import TodoItem from "./TodoItem"
import todosData from "./todosData"`
React, individual To-Do template and simulated API data are imported

`class App extends React.Component {
  constructor() {
    super()
    this.state = {
      todos: todosData
    }
    this.handleClick = this.handleClick.bind(this)
  }`
  A new React Component class called App is created. Because we are using state to pass in information from todosData, we need to include a constructor method and then call super below it (common practice). State (using the keyword 'this' because 'this' refers to information passed in from the React Component - if this was all written in an ordinary function rather than a component class, we would not need to use the 'this' keyword) is defined as an object, and this object contains the key 'todos'. This key is given a value of an array of information. In our case this array is the data being passed in from todosData in the todosData.js file. In the last line of the constructor method, we bind the function handleClick() to our constructor. This step actually happens quite a bit later on, but appears high up in the code.

  `handleClick(id) {
    this.setState(prevState => {
      const newTodos = prevState.todos.map(todo => {
        if (todo.id === id) {
          todo.completed = !todo.completed
        }
        return todo
      })
      return {
        todos: newTodos
      }
    })
  }`
  handleClick() is a method we call on the component class which refers to any instance of when a user clicks on, in our case, one of the checkboxes. When the checkbox is clicked, handleClick will use the built-in function setState() to define a new state for that particular DOM item. setState() looks at the previous state of that item, and switches its state from true to false or vice versa by comparing the id of the item clicked to the corresponding id in the todosData array. It then returns the item with the switched state as part of a brand new array. In this way, any time a user clicks one of the checkboxes, React actually re-renders the entire array of checkboxes to reflect the new state.

  `  render() {
    const todoItems = this.state.todos.map(item => <TodoItem key={item.id} item={item} handleClick={this.handleClick}/>)

    return (
      <div className="todo-list">
        {todoItems}
      </div>
    )
  }
}

export default App`
Every React Component has a required method called render. In it, we define a new variable todoItems which looks at the basic template for a Todo Item (as defined in TodoItem.js) and for every object in the passed-in todosData file, fills out the information in the template with the corresponding todosData data. By passing this information in as props, the TodoItem.js template can be used and re-used as needed, as many times as we want. This is part of what makes React so powerful and fast - by having a hierarchy of information where props and state are passed down as needed and information is passed up as needed, each component can have a clear, defined purpose and DOM objects are only re-rendered on a per-need basis.



View the source code here:

[https://github.com/chriswillsflannery/gatsby-todoList](https://github.com/chriswillsflannery/gatsby-todoList)
