# General Data Loading with Redux from outside API

## Component gets rendered onto the screen

PostList components needs to get a list of posts from the API

## Component's 'componentDidMount' lifecycle method gets called

Access to lifecycle methods

## Components are generally responsible for fetching data they need by calling an action creator

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
