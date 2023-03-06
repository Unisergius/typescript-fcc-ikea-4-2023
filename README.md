# typescript-fcc-ikea-4-2023
Meetup about Typescript

## Location

Ikea's Restaurant - Mar Shopping Algarve

## DateTime

8 March 2023 @ 7PM

## Subject

Intro to TypeScript

## Table of Contents

1. Why TypeScript?
2. Does it have drawbacks?
3. Transpiling
4. Install TypeScript 
  4.1 Install NPM / NodeJS if needed
5. Concepts 
  5.1 Types
  5.2 Interfaces
  5.3 Generics 
  5.4 Type-casting 
  5.5 Strict Mode
6. Literature
7. Thank you

## Why TypeScript?

If you're a web developer, chances are you coded in JavaScript.
Either Javascript on the frontend as it was originally intended,
or in the backend with NodeJS (You are not safe 💀). 
JavaScript grew from being a simple scripting language that allowed 
you to make websites more interactive, to be able to create full blown
applications as powerful as desktop apps. 

JavaScript became super popular with *Asynchronous JavaScript and XML* , *jQuery*, *MooTools*, *Node.js*, etc.. (and now the plethora of JavaScript frameworks like Vue.js and React). 

As time passed, the need for JavaScript to be a more reliable language rose.

Let's look at some unexpected things JavaScript can do.
You are probably familiarized with these shenanigans. 

```js 
    let foo = "2";
    let bar = 2;
    console.log("a) ", foo + bar);  
    console.log("b) ", foo - bar); 
``` 

Will the first log display 4?
What about the second log?

```js
    const car = {
      brand : 'Fiat',
      model : '500',
    }
    console.log("My car has " + car.numberOfWheels + " wheels");
```

Should JS let me access an unexisting property of car?

These are just examples of what JavaScript doesn't control. 
From here you have two options:

  a)  Accept JavaScript doesn't react as we logically expect. 
      You now have to be very careful and know every peculiar behavior
      JavaScript can output to your content. Testing becomes harder.
      Unpredictable bugs can happen.

  b)  If you ever coded in C# or Java you know just how shady and unpredictable   
      JavaScript code can be. So look into a tool that can help you create more 
      reliable, robust JavaScript code.  

  Spoilers, it's TypeScript.

  ### Enter TypeScript

  TypeScript is a *typed superset* of JavaScript. It *extends* from 
  JavaScript therefor accepts JS as legal code.

  But TypeScript checks for syntax, expected types and illegal operations.
  It helps you catch unexpected JS behavior before you apply your code to 
  your application. 

  But get this, your code in TypeScript is not what is going to be run.
  TypeScript is *transpiled* into JavaScript! And then the output JS code 
  gets to run. 
  
  This way, you'll catch any unexpected javascript errors and behaviors 
  before running code and you'll save a bunch of time developing your
  app.

  ## Does it have drawbacks?

  As noted before, TypeScript needs to be transpiled. So it can take some
  time to convert into JavaScript in larger projects.

  For JavaScript experts, TypeScript can just get in the way, specially for
  solo developers. 

  ## Transpiling TypeScript into JavaScript

  
 
