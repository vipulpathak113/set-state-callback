# callback-chunk

A React library used in getting callbacks for setstate for Hooks. 

## It solves the problem in functional component using hooks
Currently we do not get any callback for setState in functional components like we used to get in class components which is sometimes creates problem as setstate is asynchronous and we need to use latest value just after setting the state. So it helps in addressing this problem.

## Installation

npm:
```bash
npm install set-state-callback
```

Yarn:
```bash
yarn add set-state-callback
```
## Usage

Import the module:
```javascript
import useStateCallback from 'set-state-callback'
```

## Example

```javascript
import useStateCallback from 'set-state-callback'

const [state,setState]= useStateCallback();

const testFunc=()=>{

setState(newValueToSet,(newValue)=>{

    console.log(newValue) // This will be the new value you just set in the state.
    
    //Now you get the callback for setState where you can proceed using the latest value

})
}

```
