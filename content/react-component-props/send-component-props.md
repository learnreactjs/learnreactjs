# Sending Component Props

Sending properties (Props) to a component when it is used, not when it is defined. 

For example, the below `MyComponent` component is defined first. Then, to send a prop to the `MyComponent` component, name="Brian" is added to the component when it is used (i.e. when `<MyComponent name="Brian" />` is rendered).

```javascript
class MyComponent extends React.Component {
  render() {
    return <div>{this.props.name}</div>;
  }
}

ReactDOM.render(
  <MyComponent name="Brian" />, 
  document.getElementById('app')
);
```

Keep in mind anywhere a component is used a property can be sent to it. For example, the code from the previous section demonstrates the use of the `MyComponent` component and name property from within the `App` component.

```javascript
class MyComponent extends React.Component {
  render() {
    return <div>{this.props.name}</div>;
  }
}

class App extends React.Component {
  render() {
    return (
      <div>
        <MyComponent name="Brian" />
        <MyComponent name="Ryan" />
      </div>
    );
  }
}

ReactDOM.render(
  <App />, 
  document.getElementById('app')
);
```
