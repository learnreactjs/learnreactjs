# Using Built-in Element Factories

React provides built-in shortcuts for creating HTML element nodes. These shortcuts are called React element factories.

Using a built-in element factory (i.e. React.DOM.option()), the React element node `<li value="1">one</li>` can be created like:

```
// Uses React.DOM.option(props, children);
var reactNodeLi = React.DOM.option({value: '1'}, 'one');
```

Instead of using:

```
var reactNodeOption = React.createElement('option', { value: 1 }, "one");
```

Notes:

* If you are using JSX you might not ever use factories.
* React has a built-in helper for you to create custom factories. It's [React.createFactory(type)](https://facebook.github.io/react/docs/top-level-api.html#react.createfactory).
