# Matching Memory

## Codecademy Project

When introducing Redux to a React application, you transfer the responsibility of state management over to Redux. This is great because Redux is really good at state management, but this also hinders React’s optimized UI rendering. That is why <code>react-redux</code> was created to bind the UI rendering of React to the state management of Redux.

This project explores where <code>react-redux</code> fits into an application by finishing off the implementation of a one-player matching game.

The application consists of 5 React components:

1. <code>App</code>: The root component, <code>App</code> renders the <code>Score</code> and <code>Board</code> components.
2. <code>Score</code>: Child of the <code>App</code> component, <code>Score</code> will display the number of matched cards.
3. <code>Board</code>: Child of the <code>App</code> component, <code>Board</code> will create the card grid for gameplay.
4. <code>CardRow</code>: Child of the <code>Board</code> component, <code>CardRow</code> renders a row of <code>Card</code> components.
5. <code>Card</code>: Child of the <code>CardRow</code> component, <code>Card</code> displays the card content when flipped over.

One goal of this project will be to show that a nested component like <code>Card</code> can access data and dispatch actions as easily as a higher-level component like <code>App</code> or <code>Score</code>.

Most of the Redux store logic is implemented in **boardSlice.js**. This includes initializing the <code>state</code>, the reducers, and the action creators.

The application <code>state</code> is an array of 12 objects with each object representing a card:

```
// card object
{
  id: uniqueID, 
  contents: wordString, 
  visible: visibleBoolean, 
  matched: matchedBoolean
}
```

There are 3 actions needed to run the game:

- <code>setGame</code>: randomize the card array and set visible and matched of all cards to false
- <code>flipCard</code>: set visible of the specified card id to true
- <code>resetCards</code>: set visible to false on unmatched cards

To complete this project you will add a `<Provider />` component, implement selectors, retrieve data from the <code>store</code> with <code>useSelector()</code>, and dispatch actions with the help of <code>useDispatch()</code>. With all of this ahead of you, explore the starting code of the application and then move on to the first task to begin implementing the matching game.