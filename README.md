# typescript-fcc-ikea-4-2023

Ikea Meetup about Typescript

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
5. Install NPM / NodeJS if needed
6. Concepts
7. Types
8. Interfaces
9. Generics
10. Type-casting
11. Strict Mode
12. Literature
13. Thank you

## Why TypeScript?

If you're a web developer, chances are you coded in JavaScript.
Either Javascript on the frontend as it was originally intended,
or in the backend with NodeJS (You are not safe 💀).
JavaScript grew from being a simple scripting language that allowed
you to make websites more interactive, to be able to create full blown
applications as powerful as desktop apps.

JavaScript became super popular with *Asynchronous JavaScript and XML* ,
*jQuery*, *MooTools*, *Node.js*, etc.. (and now the plethora of JavaScript frameworks like Vue.js and React).

As time passed, the need for JavaScript to be a more reliable language rose.
Something that would not slow us down with the typical shenanigans JS does, because
if you have a large enough app, everytime JS jiggles its jester bells, your company
loses time fixing them.

So Micro$oft got us TypeScript in 2012. What????

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

### You have to write more code

  For programmers that don't like to 'unnecessary' code, TypeScript comes in their lives like Barney into Moe's tavern --Haha, Simpson's joke, I'll stop...--.
  You'll have to declare types, write interfaces and overall be little more conscient of the type of data your program is flowing within its veins.

  This is seen as a drawback initially, but if you're a former JS developer you'll notice something has changed in your normal project workflow. What normally would take some time using browser's Inspect tool or trying to replicate a reported bug with a specific set of instructions to replicate it, now bugs are catch right on the spot as you code. The extensive writing you took when declaring types, interfaces, using objects, and more, pays off with code reliability and less bugs discovered by your clients.

  You also have clearer code written, so your future 6-months-from-now self will thank you for that, when he/she has to read your code to implement a new feature / correct bugs.

### Takes a while to 'compile'

  Ackshually 🤓, it's transpiling (I mean, whatever...).

  As noted before, TypeScript needs to be transpiled. So it can take some
  time to convert into JavaScript in larger projects.

## TypeScript setup

### Requirements

* Node.JS - <https://nodejs.org/en/download/>
* NPM - <https://docs.npmjs.com/downloading-and-installing-node-js-and-npm>

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

```sh
  tsc -v

```

  This should show you the latest version.

### Typescript just on a project

  Say you just want to use TypeScript in your current project:

```sh
  npm install typescript --save-dev

```

  > ℹ️ A little offtopic:  
  --save-dev is your way to tell NPM you'll only use typescript in development
  mode. In a production version of your TS app, you'll have a tested and true app with few bugs as possible. The app is stable, and we're more concerned about performance and speed.
  
  Typescript doesn't need to be transpiled over and over in a production stage. ( --Super-ideally-- you won't develop in production stage, because that's just plain nuts. )
  
## Concepts of TypeScript

### Types

Types are back in the menu boys 👹.

Let's fetch our sample above.

```js
    let foo = "2";
    let bar = 2;
    console.log("a) ", foo + bar);  
    console.log("b) ", foo - bar); 
```

Put this in a file called shenanigans-01.ts.
Next let's try doing the following and watch the output.

```sh
  node shenanigans-01.ts
```

Now compare it with the output of the following command

```sh
  tsc shenanigans-01.ts
```

TypeScript will come up and tell you to "Stop right there..." in good old Elder Scrolls angry guard fashion.
"You can't just do that with this. They are different types".

Typescript allows you to catch these little incongruencies with static types.

3 types of types:

* any - a little fairy gets hit by a moving car everytime this is written.
* Built-in - available types given by TypeScript that cover the basics
* User defined - types like enum, array, interface, class...

To assign a type to a variable:

```ts
  let foo: number = 2;
```

> Number values can be floats, octals, hexadecimals, binary.

```ts
  let parisAgreementGoalReached: boolean = false
```

> example of a variable declared as a boolean

```ts
let planets: Array<string>;
planets = ['Jupiter', 'Saturn', 'Mercury']; 
let notPlanets: string = 'Pluto';

let euromillionsWinningNumbers: Array<number>;
ids = [2, 14, 29, 31, 44]; 
```

> Examples of Typed Arrays

As a small challenge, let's discuss how can we use TypeScript to fix **shenanigans-01.ts** in order to get an expected results.

Now that this small intro is done, let's start doing this interactive book from Codemastery together.

[CodeMastery's Interactive Handbook of TypeScript](https://codemastery.dev/ts/interactive-handbook/intro/0)
