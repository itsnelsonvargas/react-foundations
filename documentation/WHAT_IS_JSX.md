 # What is JSX?

**JSX is a syntax extension for JavaScript** that allows you to describe your UI in a familiar HTML-like syntax. The nice thing about JSX is that apart from following [three JSX rules](https://react.dev/learn/writing-markup-with-jsx#the-rules-of-jsx), you don't need to learn any new symbols or syntax outside of HTML and JavaScript.

But browsers don't understand JSX out of the box, so you'll need a JavaScript compiler, such as a [Babel](https://babeljs.io/), to transform your JSX code into regular JavaScript.


 # Using variables in JSX

To use prop, add **curly braces {}**. These are a special JSX syntax that allows you to write regular JavaScript directly inside your JSX markup.

You can think of **curly braces** as a way to enter "JavaScript land" while you are in "JSX land". You can add any JavaScript expression (something that evaluates to a single value) inside curly braces. For example:

1. An **object property** with dot notation:
```
function Header({ title }) {
  console.log(title);
  return <h1>{title}</h1>;
}
```

2. A **template literal**:
```
function Header({ title }) {
  return <h1>{`Cool ${title}`}</h1>;
}
```

3. The **returned value of a function**:
```
function createTitle(title) {
  if (title) {
    return title;
  } else {
    return 'Default title';
  }
}
 
function Header({ title }) {
  return <h1>{createTitle(title)}</h1>;
}
```

4. Or **ternary operators**:
```
function Header({ title }) {
  return <h1>{title ? title : 'Default Title'}</h1>;
}
```
You can now pass any string to your title prop, or, if you used the ternary operator, you could even not pass a title prop at all, since you've accounted for the default case in your component:
```
function Header({ title }) {
  return <h1>{title ? title : 'Default title'}</h1>;
}
 
function HomePage() {
  return (
    <div>
      <Header />
    </div>
  );
}
```

Your component now accepts a generic title prop which you can reuse in different parts of your application. All you need to do is change the title string:
```
function HomePage() {
  return (
    <div>
      <Header title="React" />
      <Header title="A new title" />
    </div>
  );
}
```