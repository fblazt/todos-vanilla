# Todos Documentation

## Table of Contents

- [About](#about)
- [Technical Documentation](#technical-documentation)
- [User Guide](#user-guide)
  - [Add Todo](#add-todo)
  - [Edit Todo](#edit-todo)
  - [Set Completed Todo](#set-completed-todo)
  - [Delete Todo](#delete-todo)
  - [Todos Options](#todos-options)
- [Performance Audit](#performance-audit)

## About

Todos is a Web App that can be used to organize your to-do or task list.

## Technical Documentation

Todos Web App is an app that built based on MVC (Model-View-Controller) architecture. Each of this parts handles its own task and functions. 

1. Model is used to manage data of the application, receiving input from controller and doing CRUD operations.

2. View is used to format and display the data to the user.

3. Controller is used to connect view so that it can interract with model, mostly to pass data that need to be updated.

### Files

#### HTML

<b>index.html</b> - App homepage

#### CSS

<b>index.css</b> - App CSS styles

#### JS

<b>app.js</b> - Make new to-do list.
<br>
<b>model.js</b> - Model instance to connect between storage and view.
<br>
<b>controller.js</b> - Connecting view with model.
<br>
<b>helper.js</b> - Get element and attach event listener, attach handler to event for elements, basically controlling html elements with javascript.
<br>
<b>store.js</b> - Controlling client side storage using localStorage.
<br>
<b>template.js</b> - Setting up default template.
<br>
<b>view.js</b> - Triggering functions from controller and rendering view to the user.

## User Guide

### Add Todo

<image width="400px" src='./screenshots/add-todo.png' />
<p>Click on the input field as shown, write down your task, and hit enter to save it.</p>

### Edit Todo

<image width="400px" src='./screenshots/edit-todo.png' />
<p>Double click on the task or to-do as shown, the input field will be enabled, edit your task, and hit enter to save it. You can also click escape key to undo your changes.</p>

### Set Completed Todo

<image width="400px" src='./screenshots/set-complete-todo.png' />
<p>If you have completed your task or to-do, simply click empty circle on the left side of the task to set it to complete. You can also click it again to set it back to active.</p>

### Delete Todo

<image width="400px" src='./screenshots/delete-todo.png' />
<p>If you have completed your task or to-do, or you might be thinking that the task is no longer useful, you can click X icon on the right side of the task to set it to complete. Keep in mind that deleted todo cannot be restored, so be careful.</p>

### Todos Options

<image width="400px" src='./screenshots/todos-options.png' />
<p>In the bottom of main content there is an options that can be useful. Starting from the left side there is a counter for your active to-do or task. And move to the center bottom part there is an options to filter the to-do or task that will be shown, you can choose all, active, and the completed ones. And the last one on the right side there is a button to remove all of the completed todos.</p>

## Performance Audit

<p>TodoListMe is a task management website that aims to have the highest usability factor possible to get todo listing done with minimum effort required. This website will be the site that used to compare with todos, a website that’s currently in development progress. Any results from this audit could be taken to improve todos website.</p>

<table>
  <tr>
    <td>Problem</td>
    <td>Consequences</td>
    <td>Solution</td>
  </tr>
  <tr>
    <td>Unused JavaScript codes.</td>
    <td>The website loads slower.</td>
    <td>Removing the unnecessary lines of code to reduce bytes consumed by network activity or request.</td>
  </tr>
  <tr>
    <td>Serving or providing images in next-gen formats.</td>
    <td>Slower download times and bigger data consumption.</td>
    <td>Use images with better compressions.</td>
  </tr>
  <tr>
    <td>Third-party code load performance.</td>
    <td>The website loads slower.</td>
    <td>Limiting redundant third-party providers and loading some of the codes after primary data for the page is finished loading.</td>
  </tr>
  <tr>
    <td>Image elements do not have explicit size.</td>
    <td>Images might be rendered in different sizes depending on the device used by the user.</td>
    <td>Set an explicit width and height on each image element.</td>
  </tr>
  <tr>
    <td>Using document.write()</td>
    <td>Might delay page load on slow connection devices.</td>
    <td>Get element by getElementsByName() or getElementById() and change the content using .innerHTML</td>
  </tr>
</table>