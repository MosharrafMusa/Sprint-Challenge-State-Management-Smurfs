1. What problem does the context API help solve?
   Answer:
   Context API helps to simplify state management. It gives the developer the ability to use intermediate components to pass (shared) global data to many different components of the application without having to do prop drilling.

2. In your own words, describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

Answer:
Actions- plain Javascript object that contains information. Actions have type feilds that tells what kind of action to perform and a payload that holds the data to change to.

Reducer- holds if statements or switch case statements and perform an action depending on the type and tells the store how and what to change state to.

Store- Holds the state where every component has access to the state. It's the only place which represents original state.

STORE is the single source of truth because it containes all of the state values in your app.

3. What is the difference between Application state and Component state? When would be a good time to use one over the other?

Answer:
Component state should be used if the component is solely using it for itself. The changes in that state should not affect others. IE: Highligting a component.

Application state, on the other hand, affects any component that is connected to it. IE: Fetched data from a API call passed down as props.

4. Describe `redux-thunk`, what does it allow us to do? How does it change our `action-creators`?

Answer:
Redux-thunk is a library that allows redux to manipulate the store with asynchronous actions. A thunk is a function returned by a function.

This concept allows the function to be saved, modified, and then called later by external code.

This changes the action-creators by having the action functions return a function instead of an object. This would normally not permitted by redux, but redux-thunk is a middleware that intercepts the action dispatches and checks to see if a function is returned instead. This allows us to appropriately place the dispatch call in the then and catch methods so it can send actions to the store when the async work is done.

5. What is your favorite state management system you've learned and this sprint? Please explain why!

Answer:
Context API is my favorite so far, it allows me to access state throughout my app. Also, Context API is way more convenient to implement than Redux. I want to get better with redux, because I think it's more commonly used.
