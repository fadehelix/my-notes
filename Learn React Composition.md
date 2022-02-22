#react #design-patterns

[https://www.google.com/search?channel=nrow5&client=firefox-b-d&q=react+component+strategy](https://www.google.com/search?channel=nrow5&client=firefox-b-d&q=react%20component%20strategy&authuser=0)  
  
  
React Tips & tricks  
building a static version requires a lot of typing and no thinking, and adding interactivity requires a lot of thinking and not a lot of typing  
  
  
State is reserved only for interactivity  
  
  
 In simpler examples, it’s usually easier to go top-down, and on larger projects, it’s easier to go bottom-up and write tests as you build.  
  
So we have two strategy of building components:  
  
top-down : easier to use in smaller apps : start with big all-in-one component and split it continuously.  
bottom-up : more efficient in complex apps as we can write tests  
  
  
Ask three questions about each piece of data:  
Is it passed in from a parent via props? If so, it probably isn’t state.  
Does it remain unchanged over time? If so, it probably isn’t state.  
Can you compute it based on any other state or props in your component? If so, it isn’t state.  
  
  
Verbose code that is easy to move around, change and remove is preferred to elegant code that is prematurely abstracted and hard to change  
  
  
Interesting resources:  
[https://dev.to/parnikagupta/one-way-data-binding-in-react-30ea](https://dev.to/parnikagupta/one-way-data-binding-in-react-30ea)