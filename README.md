# Kent-s-Beginner-Guide-to-React
This repo contains my learnings from the course Beginner's Guide to React by Kent C. Dodds.

#### What I have learnt : 

##### Lesson 01 : Create a user Interface with Vanilla Javascript and DOM    

1. Using the DOM API to create a new element and append it as an child to an existing DOM element.


##### Lesson 02 : Create a User Interface with React’s createElement API

1. How to use the React.createElement API and different ways to pass children.
2. How react can be added to a project. The delivery through unpkg's CDN being the easiest and fastest way.

##### Lesson 03 : Create a User Interface with React’s createElement API

1. The current syntax of using React.createElement is not very developer friendly. So, react team came up with JSX to allow HTML like syntax in Javascript.
2. Since browsers do not understand the JSX directly, we have to use a transpiler like babel to convert JSX into React/Javascript that browsers can understand.
3. The standalone version of babel can be added using Unpkg's CDN directly to the webpage, babel looks for scripts with type 'text/babel' and then add the converted script to the webpage. This method is okay for a developer environment but not recommended in production. Use a pre-compiler for production.

#### Lesson 04 : Use JSX effectively with React

1. Anything inside '{}' can be a valid javascript expression in JSX. 
2. Using the above property, multiple arguments can be appended to an object and this object can be passed to the element. 
3. The order of the arguments passed to the element matters. The last one wins. This can be utilised in over-riding some of the parameters of an object that was previously passed as argument.

#### Lesson 05 : Render two elements side-by-side with React Fragments

1. React.Fragment allows us to render two elements to the root without having to contain them inside a container div.
2. This is helpful when we need an exact structure (without any container div) for elements like a table.


#### Lesson 06 : Create a Simple Reusable React Component

1. One of the main advantage of using React is the ability it provides to re use components. 
2. Make a function with first letter capitalised and make it return a JSX element. 
This way this function can be used just like a HTML tag while creating react elements.

#### Lesson 07 : Create a Simple Reusable React Component

1. As re-usable components will most likely be consumed by other people, to make sure that these are used properly, we can add validator functions on each prop type(As javascript does not have any build in type checking). One way to do that is to add a validator function on Component.proptypes property. These validator functions can also be re used by making them data-type specific.
2. Seeing the popularity and the requirement of proptypes property, react team released prop type module on npm making it easier to add validator functions. You need to anly specify the intended type of the prop.
3. As prop type check adds extra burden on rendering, this could be a performance bottleneck. So proptypes does not exist on the production version of react. 
4. There are some tools which can help remove proptypes from the production codebase but most probably these are included in the bundling toolkits you are already using.

#### Lesson 08 : Understand and Use Interpolation in JSX

1. HTML and Javascript already provide the concept of interpolation i.e. depending upon where in the file you are, you can use different language features or complete different language altogether. 
e.g. One can write CSS inside the style tags of HTML files and JS inside the script tag. Inside the template literals (``), everything is interpreted as string, but inside ${__} Javascript expressions can be used.
2. JSX also supports interpolation inside {__}.
3. Interpolation inside curly braces supports Javascript expressions only, no conditional statements, loops or other constructs (same as template literals inside JS).
4. One enters JSX land when inside <tags> in the Javascript and JS land again inside the curly braces.
5. JSX tags and {} can be nested as many as times as possible.


#### Lesson 09 : Rerender a React Application

1. When DOM is updated using just JS, the whole element is replaced with a new one. (No surprises there). But when we render the same element (with some updates) using React, React does not update the whole element, insted it intelligentally calculates the the part which has changed and updates just that.
2. There are some advantages to the approach taken by React.Because the updated element is the same element as before but just with updated values, user does not loose the interation which he/she was having with the element e.g. focus state remains.

#### Lesson 10 : Style React Components with className and inline Styles

1. A big advantage of using React is that it supports components, so whenever we encounter a part of UI which is used at more than one place, its better to make a react component out of it.
2. While writing defination of a component, make sure that the user can still override all the configuration of the compoenent if they want to. (Spread the user provided props after the default ones)
3. Instead of using the CSS class names like box-small, try to use more abstract concept like a size prop (with possible values as small, medium). This way the details of the implementation can be put entirely into the component code and away from the developer using the component.
4. The reason the word 'className' is used instead of 'class' is because the 'class' is reserved and would create problem when used in regular javascript code.
5. CSS properties are passed to the prop style in the form of an object in camelCase. CamelCase to make them consistent with standard DOM 'sytle' Javascript property. 


#### Lesson 11 : Use Event Handlers with React

1. One good thing about how react handles the event handlers is that the handler is added at the element itself, it makes it readable and easy to follow along.
2. React wraps the original DOM event inside a SyntheticEvent Object to do some serious optimization. This object is almost equal to the DOM event. 

#### Lesson 12 : Manage state in a React Component with the useState hook

1. If we maintain state of a compenent inside the component defination, we loose the state once the garbage collector runs. Its hard to do state management on our own using just the concept of objects holding references to older states. 
1. React Hooks allows us to hook or connect a state with a component and whenever the user does something, we update the state and then react updates the compenent as a 'reaction'.
2. The 'useState' API provides ability to maintain independent states inside the same components. 
