# mapDispatchToProps Lab

## Objectives

Implement a **mapDispatchToProps()** function to connect a Redux action to a component event

## Overview

In this lab you will be implementing a **mapDispatchToProps()** function for an 
application that helps us keep track of our favorite restaurants. Our **React** 
application is kept separate from our **Redux** application through the use of 
the **Provider** component and the **connect()** function. When you have completed 
the lab, there should be no reference to the store in any component other than the 
**Provider**.

## Instructions

Much of the functionality of the app is already built out for you. We have two 
components: a `RestaurantInput` component that consists of a simple form to add a 
new restaurant, and a `Restaurants` component that renders the names of the 
restaurants to the page. Redux has already been set up through `index.js` and the 
reducer `manageRestaurants`. In addition, the `Restaurants` component has been 
connected to the store and a **mapStateToProps()** function implemented to provide
the list of restaurants to the component as props. 

Recall that, in the previous codealong, we wrote both the `mapStateToProps` and 
`mapDispatchToProps` functions in our `App.js` file. For this application, 
however, we have separated our form code from the code rendering the list of 
restaurants. There is no reason we can't use **connect()** with both components. 
Your task is to write a **mapDispatchToProps()** function in the `RestaurantInput` 
component, which will allow us to pass dispatched actions as props. Remember that 
**mapDispatchToProps()** is provided `dispatch` as an argument (passed in by 
`connect` when called), so we can wrap an imported action with `dispatch` within 
**mapDispatchToProps()**. Don't forget that the action provided in 
`actions/restaurants.js` is a function that _must be called_ in order to return 
the action object.

HINT: remember that **connect()** passes `dispatch` as the *second* argument. 
Since you won't have a `mapStateToProps` action in your `RestaurantInput` 
component, you can ensure that dispatch is passed to `mapDispatchToProps` by
passing `null` as the first argument to `connect`.
