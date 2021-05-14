# Interview Answers
Be prepared to demonstrate your understanding of this week's concepts by answering questions on the following topics. These will not be counted as a part of your sprint score but will be helpful for preparing you for your endorsement interview, and enhancing overall understanding.

1. What problem does the context API help solve?
        
        Context API is an alternateive to prop drilling.  Rather than having to recieve props from a parent or grandparent component, you can simply Consume props from whatever is wrapped in the Provider!  This way you don't have to pass props at every single level.

2. In your own words, describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

        Actions are essentially the delivery system from our component to our reducer.  They function returning an object that contains a type (required for the reducer's switch statement) and, if its necessary, a payload (new data that we will put into state).

        Reducers are the function that is generating a new state.  It uses a switch statement in order to know how to update the state. What data we use to generate a new state comes from a payload recieved from the Action.

        Store is similar to what it sounds like.  It is an immutable shopping center for our components!  Each component can CONNECT to the store and shop for which pieces of state it needs.  No drilling of state required :)  It is a single source of truth in the sense that it is holding the Application State.  If other components want to change the state the must use actions to transfer how they are going to do that to the SINGLE SOURCE. 

3. What does `redux-thunk` allow us to do? How does it change our `action-creators`?
    
        Redux-thunk is middleware. This means that before the ACTION gets to the REDUCER, it is intercepted by this middleware, manipulated in some way, and then it gets passed on to the REDUCER.  Thunk allows us to make asynchronous actions.   

4. What is your favorite state management system you've learned and this sprint? Please explain why!

        I think that entirely depends on the scale of the project... if its a small project useState seems fine to me.  As soon as it starts getting bigger, and if I were the one setting up the project I would prefer Context API.  It seems a lot easier to set up and I'm hoping that becauase it's newer, it only gets better in the future.  But I do think Redux is a very powerful tool and I might ultimately prefer that one for larger projects.  It might take a second for me to get used to how the STORE is operating, but I feel like I would be able to figure out how to navigate it in a reasonable amount of time. 