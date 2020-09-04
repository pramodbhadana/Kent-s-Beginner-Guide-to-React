# Kent-s-Beginner-Guide-to-React
This repo contains my learnings from the course Beginner's Guide to React by Kent C. Dodds.

#### What I have learnt : 

##### Lesson 1 : Create a user Interface with Vanilla Javascript and DOM    

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