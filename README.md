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

Todos is a Web App that can be used to organize your todo or task list. It has features that allows user to:

- Add todo
- Edit todo
- Delete todo
- Mark todo as completed
- Filtering todo by displaying all todos, active todos, or completed todos

## Technical Documentation

Todos Web App is an app that built based on MVC (Model-View-Controller) architecture. Each of this parts handles its own task and functions. 

1. Model is used to manage data of the application, receiving input from controller and doing CRUD operations.

2. View is used to format and display the data to the user.

3. Controller is used to connect view so that it can interract with model, mostly to pass data that need to be updated.

### Files Structure

#### HTML

- **index.html** - App homepage

#### CSS

- **index.css** - App CSS styles

#### JS

- **app.js** - Make new todo list
- **model.js** - Model instance to connect between storage and view
- **controller.js** - Connecting view with model
- **helper.js** - Get element and attach event listener, attach handler to event for elements, controlling html elements with javascript in general
- **store.js** - Controlling client side storage using localStorage
- **template.js** - Setting up default template
- **view.js** - Triggering functions from controller and rendering view to the user

## User Guide

### Add Todo

<image width="400px" src='./screenshots/add-todo.png' />
<p>Click on the input field as shown, write down your task, and hit enter to save it.</p>

### Edit Todo

<image width="400px" src='./screenshots/edit-todo.png' />
<p>Double click on the task or todo as shown, the input field will be enabled, edit your task, and hit enter to save it. You can also click escape key to undo your changes.</p>

### Set Completed Todo

<image width="400px" src='./screenshots/set-complete-todo.png' />
<p>If you have completed your task or todo, simply click empty circle on the left side of the task to set it to complete. You can also click it again to set it back to active.</p>

### Delete Todo

<image width="400px" src='./screenshots/delete-todo.png' />
<p>If you have completed your task or todo, or you might be thinking that the task is no longer useful, you can click X icon on the right side of the task to set it to complete. Keep in mind that deleted todo cannot be restored, so be careful.</p>

### Todos Options

<image width="400px" src='./screenshots/todos-options.png' />
<p>In the bottom of main content there is an options that can be useful. Starting from the left side there is a counter for your active todo or task. And move to the center bottom part there is an options to filter the todo or task that will be shown, you can choose all, active, and the completed ones. And the last one on the right side there is a button to remove all of the completed todos.</p>

## Performance Audit

<p>The Performance Audit was done by using Chrome's Developer Tools (Lighthouse). This will be used to measure and compare between our own app and the competitor.</p>

### Competitors Website

<p>TodoListMe is a task management website that aims to have the highest usability factor possible to get todo listing done with minimum effort required. This website will be the site that used to compare with todos, a website that’s currently in development progress. Any results from this audit could be taken to improve todos website.</p>

<image width="100%" src='./screenshots/todolistme-audit.png' />

#### Performance

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

#### Accessibility

<table>
  <tr>
    <td>Problem</td>
    <td>Consequences</td>
    <td>Solution</td>
  </tr>
  <tr>
    <td>Background and foreground colors do not have a sufficient contrast ratio.</td>
    <td>Difficult for many users to read.</td>
    <td>Find the right color combination.</td>
  </tr>
  <tr>
    <td>frame or iframe elements do not have a title.</td>
    <td>Contents is not describable in screen reader.</td>
    <td>Add specific title for each elements.</td>
  </tr>
  <tr>
    <td>Image elements do not have [alt] attributes.</td>
    <td>Informative elements will not be descriptive for the users.</td>
    <td>Add specific [alt] attributes for each elements.</td>
  </tr>
  <tr>
    <td>Form elements do not have associated labels.</td>
    <td>Forms is not describable in screen reader.</td>
    <td>Add correlated label for each input elements.</td>
  </tr>
</table>

#### Best Practices

<table>
  <tr>
    <td>Problem</td>
    <td>Consequences</td>
    <td>Solution</td>
  </tr>
  <tr>
    <td>JavaScript Libraries with security vulnerabilities(JQuery).</td>
    <td>Could be easily exploited by attackers.</td>
    <td>Update library version.</td>
  </tr>
  <tr>
    <td>Serve low resolution images.</td>
    <td>Not proportional to the display size.</td>
    <td>Use high resolution image to increase clarity and pixel ratio.</td>
  </tr>
</table>

#### SEO

<table>
  <tr>
    <td>Problem</td>
    <td>Consequences</td>
    <td>Solution</td>
  </tr>
  <tr>
    <td>No meta tag to optimize usage on mobile screens.</td>
    <td>Some fonts and tap targets will be too small for mobile users.</td>
    <td>Use meta tag with [name] attribute and add width or initial-scale.</td>
  </tr>
</table>

### Todos Website

<p>Our app overall score is already high, but there will always be rooms for improvisation, let's look at what part that need to be improved.</p>

<image width="100%" src='./screenshots/todos-audit.png' />

#### Best Practices

<table>
  <tr>
    <td>Problem</td>
    <td>Consequences</td>
    <td>Solution</td>
  </tr>
  <tr>
    <td>Logging of an error request.</td>
    <td>A possibility that there is still unresolved problems.</td>
    <td>Check the the request.</td>
  </tr>
</table>

#### SEO

<table>
  <tr>
    <td>Problem</td>
    <td>Consequences</td>
    <td>Solution</td>
  </tr>
  <tr>
    <td>No meta tag to optimize usage on mobile screens.</td>
    <td>Most of the users will have to pinch to zoom to be able read the content properly.</td>
    <td>Use meta tag with [name] attribute and add width or initial-scale.</td>
  </tr>
  <tr>
    <td>No meta tag for app description.</td>
    <td>Website appeared in search results will be not descriptive enough.</td>
    <td>Include meta descriptions to summarize page content.</td>
  </tr>
</table>