# Sync v/s Async

**Synchronous**
Synchronous means the code runs in a particular sequence of instructions given in the program. Each instruction waits for the previous instruction to complete its execution.

**Asynchronous**
Due to synchronous programming, sometimes imp instructions get blocked due to some previous instructions, which causes a delay in the UI. Asynchronous code execution allows to execute next instructions immediately and doesn't block the flow.

# Callbacks
A callback is a function passed as an argument to another function.

# Callback Hell
Nested callbacks stacked below one another forming a pyramid structure (Pyramid of Doom)
This style of programmig becomes difficult to understand & manage.

*Example*

```Javascript
function getData(dataId, getNextData) {
    //2s
    setTimeout(() => {
        console.log("data", dataId);
        if (getNextData) {
            getNextData();
        }
    }, 2000);
}

//callback hell
getData(1, () => {
    console.log("getting  data2 ....");
    getData(2, () => {
        console.log("getting data3 ....");
        getData(3, () => {
            console.log("getting data4 ....");
            getData(4);
        });
    });
});
```

# Promises 
Promises is for "eventual" completion of task. It is an object in JS. It is a solution to callback hell.

*Syntax*
```javascript
let promise = new Promise((resolve, reject) => {....})

//function with 2 handlers(resolve, reject)
```
*resolve & reject are callbacks provided by JS*

A JS Promise object can be:
*   Pending: the result is undefined
*   Resolved: the result is a value (fulfilled)    **resolve(result)**
*   Rejected: the result is an error object        **reject
(error)**


*Promise has state (pending, fulfilled) & some result (result for resolve & error for reject).*

## How to use promises

.then() & .catch()

promise.then(( res ) => { .... })       //execute only when fulfilled

promise.catch(( err ) => { .... })     //execute only when reject


## Async-Await

**async function always returns a promise.**

```javascript
async function myFunc() { ... }
```

**await pauses the execution of its surrounding async function until the promise is settled.**