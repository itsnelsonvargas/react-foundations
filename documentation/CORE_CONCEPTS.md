 # React Core Concepts

There are three core concepts of React that you'll need to be familiar with to start building React applications. These are:

1. **Components**
User interfaces can be broken down into **smaller building blocks called components.**

Components **allow you to build self-contained, reusable snippets of code**. If you think of components as LEGO bricks, **you can take these individual bricks and combine them together to form larger structures**. If you need to update a piece of the UI, you can update the specific component or brick.

This modularity allows your code to be more maintainable as it grows because you can add, update, and delete components without touching the rest of our application.

The nice thing about React components is that they are just JavaScript. Let's see how you can write a React component, from a JavaScript perspective:

 - **Creating Components**
 In React, components are functions. Inside your script tag, create a new function called header:
```
 <script type="text/jsx">
  const app = document.getElementById('app');
 
  function header() {}
 
  const root = ReactDOM.createRoot(app);
  root.render(<h1>Develop. Preview. Ship.</h1>);
</script>
```
 - **Nesting Components**
 Applications usually include more content than a single component. You can nest React components inside each other like you would regular HTML elements.


 - **Component Trees**
 You can keep nesting React components this way to form component trees.

 For example, your top-level HomePage component could hold a Header, an Article, and a Footer Component. And each of those components could in turn have their own child components and so on. For example, the Header component could contain a Logo, Title and Navigation component.

 This modular format allows you to reuse components in different places inside your app.

2. **Props**


3. **State**    