# wnreactstatehooks
It solves some problems
- Stateful logic is not easily re-used between components
- Components which use lifecycle methods to manage logic paths can quickly become unmanageable
- Classes are confusing for developers who are not JavaScript experts and classes present problems for future dreams of react
 AOT compilation


#### 29:00
convert class to function. 

class
```
import React from 'react';
export class CounterClass extends React.Component {
 state = {
  counter: 0;
 }
 
 increment = () => {
  this.setState({
   counter: this.state.counter +1
  });
 }
 
 render() {
  return <>
   <div>Counter: {this.state.counter}</div>
   <div><button onClick={this.increnemt}></button></div>
  </>
 }
}
```
statehook
```
import React, {useState} from 'react';
export const CounterHook = () => {
 const [counter, setCounter] = useState(0);
 const increment = () => {
  setCounter(counter + 1);
 }
 

  return <>
   <div>Counter: {counter}</div>
   <div><button onClick={increnemt}></button></div>
  </>;
}
```
