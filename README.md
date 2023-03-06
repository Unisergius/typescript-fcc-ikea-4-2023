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

  So in summary: 
    * 

  ## Does it have drawbacks?

  ### You have to write more code...
  For programmers that don't like to 'unnecessary' code, TypeScript comes in their lives like Barney into Moe's tavern --Haha, Simpson's joke, I'll stop...--. 
  You'll have to declare types, write interfaces and overall be little more conscient of the type of data your program is flowing within its veins. 

  This is seen as a drawback initially, but if you're a former JS developer you'll notice something has changed in your normal project workflow. What normally would take some time using browser's Inspect tool or trying to replicate a reported bug with a specific set of instructions to replicate it, now bugs are catch right on the spot as you code. The extensive writing you took when declaring types, interfaces, using objects, and more, pays off with code reliability and less bugs discovered by your clients.

  You also have clearer code written, so your future 6-months-from-now self will thank you for that, when he/she has to read your code to implement a new feature / correct bugs.

  ### Takes a while to 'compile'...

  Ackshually 🤓, it's transpiling (I mean, whatever...).

  As noted before, TypeScript needs to be transpiled. So it can take some
  time to convert into JavaScript in larger projects.

  ## TypeScript setup

  ### Requirements

  * Node.JS - https://nodejs.org/en/download/
  * NPM - https://docs.npmjs.com/downloading-and-installing-node-js-and-npm

  Before installing these check if you have them on your terminal.

  ```sh
    node -v
    npm -v

  ```

  ### Typescript available globally on your machine

  After installing, upgrading or watching others do it, you can install typescript globally with npm:

  ```sh
    npm install -g typescript

  ```

  Now check if typescript runs fine with :

  ```
    tsc -v

  ```

  This should show you the latest version.

  ### Typescript just on this project

  Say you just want to use TypeScript in your current project:

  ```
    npm install typescript --save-dev

  ```

  --save-dev is your way to tell NPM you'll only use typescript in development
  mode. In a production version of your TS app, you'll have a tested and true app with few bugs as possible. The app is stable, and we're more concerned about performance and speed. 
  
  Typescript doesn't need to be transpiled over and over in a production stage. ( Super-ideally you won't develop in production stage, because that's just plain nuts. )
  
 
