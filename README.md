# mapDispatchToProps Lab

## Objectives

Implement a __mapDispatchToProps()__ function to connect a Redux action to a component event

## Overview

In this lab you will be implementing a __mapDispatchToProps()__ function for an 
application that helps us keep track of our favorite restaurants. Our __React__ 
application is kept separate from our __Redux__ application through the use of 
the __Provider__ component and the __connect()__ function. When you have completed 
the lab, there should be no reference to the store in any component other than the 
__Provider__.

## Instructions

Much of the functionality of the app is already built out for you. We have two components: a `RestaurantInput` component that consists of a simple form to add a new restaurant, and a `Restaurants` component that renders the names of the restaurants to the page. Redux has already been set up through `index.js` and the reducer `manageRestaurants`. In addition, the `Restaurants` component has been connected to the store and a __mapStateToProps()__ function created to provide the list of restaurants to the component as props. You should not need to change or add any code in the `Restaurants` component. 

Your task is to write a __mapDispatchToProps()__ function in the `RestaurantInput` component, which will allow us to pass dispatched actions as props. Remember that __mapDispatchToProps()__ is provided `dispatch` as an argument (passed in by `connect` when called), so we can wrap an imported action with `dispatch` within __mapDispatchToProps()__. Don't forget that the action provided in `actions/restaurants.js` is a function that _must be called_ in order to return the action object.

NOTE: in the previous codealong, we wrote both the  `mapStateToProps` and `mapDispatchToProps` functions in our `App.js` file. For this application, however, we have separated our form code from the code rendering the list of restaurants. There is no reason we can't use __connect()__ with both components. In `Restaurants.js`, we have already implemented __connect()__ to wrap the `Restaurants` component while, in `RestaurantInput.js`, you will use it to wrap the `RestaurantInput` component. However, recall that __connect()__ passes `dispatch` as the *second* argument. Since you won't have a `mapStateToProps` action in your `RestaurantInput` component, you can simply pass `null` as the first argument to `connect`.
