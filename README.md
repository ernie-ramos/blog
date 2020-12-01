# General Data Loading with Redux from outside API

## Component gets rendered onto the screen

PostList components needs to get a list of posts from the API

## Component's 'componentDidMount' lifecycle method gets called

Access to lifecycle methods

## We call action creator from 'componentDidMount'

Any time PostList is rendered, action creator is automatically called

## Action creator runs code to make an API request

Axios is used to make the request

## API respondes with data

Responds with list of blog posts

## Action creator returns an 'action' with the fetched data on the 'payload' property

Action creator returns an action object, dispatch method sends info to all reducers

## Some reducer sees the action, returns the data off the 'payload'

Reducer watching for the type given to the action

## Because we generated some new state object, redux/react-redux cause our React app to be rerendered

State changes so app rerenders
