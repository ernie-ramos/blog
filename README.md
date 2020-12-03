# General Data Loading with Redux from outside API

## Components are generally responsible for fetching data they need by calling an action creator

### Component gets rendered onto the screen

PostList components needs to get a list of posts from the API

### Component's 'componentDidMount' lifecycle method gets called

Access to lifecycle methods

### We call action creator from 'componentDidMount'

Any time PostList is rendered, action creator is automatically called

## Action creators are reponsible for making API requests (This is where Redux-Thunk is used)

### Action creator runs code to make an API request

Axios is used to make the request

### API respondes with data

Responds with list of blog posts

### Action creator returns an 'action' with the fetched data on the 'payload' property

Action creator returns an action object, dispatch method sends info to all reducers

## We get fetched data into a component by generating new state in our redux store, then getting that into our component through mapStateToProps

### Some reducer sees the action, returns the data off the 'payload'

Reducer watching for the type given to the action

### Because we generated some new state object, redux/react-redux cause our React app to be rerendered

State changes so app rerenders

## Middleware in Redux

Function that gets called with every action we dispatch

Has the ability to STOP, MODIFY, or otherwise change actions

Tons of open source middleware exist

Most popular use of middleware is for dealing with async actions

We using Redux-Thunk to solve our async issues

## Rules of Reducers

Must return any value besides 'undefined'

Produces 'state', or data to be used inside of your app using only previous state and the action (reducers are pure)

Must not return reach 'out of itself' to decide what value to return

Must not mutate its input 'state' argument
