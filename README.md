# React tutorial

## Components


### Syntax

```javascript
function MyComponent() {
    return <div>My component</div>;
}

<MyComponent />
```


### Expressions

```javascript
function MyComponent() {
    const name = 'Alex';

    return <div>{name} component</div>;
}
```


### Iterations

```javascript
function MyComponent() {
    const names = ['Alex', 'Sviridoff'];

    return (
        <ul>
            {names.map(item => (
                <li key={item}>{item}</li>
            ))}
        </ul>
    );
}
```


### Conditions

```javascript
function MyComponent() {
    const isEnabled = false;

    return (
        <div>
            {isEnabled
            ? <div>Is enabled</div>
            : <div>Is disabled</div>}
        </div>
    );
}
```


### Events

https://reactjs.org/docs/events.html#mouse-events

onClick, onChange, onSubmit  ...


```javascript
function MyComponent() {
    function onClick(event) {
        console.log('clicked');
    }

    return <div onClick={onClick}>My component</div>;
}
```

### Fragments

```javascript
function MyComponent(props) {
    return (
        <>
            <div>Alex</div>
            <div>Sviridoff</div>
        </>
    );
}

=>
    <div>Alex</div>
    <div>Sviridoff</div>
```


### Props

```javascript
function MyComponent(props) {
    return <div>My name {props.name}</div>;
}

<MyComponent name='Alex' />
```


### State

```javascript
function MyComponent() {
    const [time, setTime] = React.useState(0);

    return <div>Is {time}</div>;
}
```


### Update state

```javascript
function MyComponent() {
    const [time, setTime] = React.useState(0);
    
    setTime(2);

    return <div>Is {time}</div>;
}
```


### Props and State


![Props & state](https://scriptverse.academy/img/tutorials/reactjs-props-state.png)











