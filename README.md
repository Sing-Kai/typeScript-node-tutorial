## Tutorial On Setting Up And Configuring TypeScript in Node

Simple tutorial on how to set up and configure Typescript in Node 

## Prerequistes

Basic understaind of Node.js and TypeScript

## Installing TypeScript

Create and initialise a Node.js project with `package.json`

`npm init`

Install TypeScript with below command:

`npm install typescript --save-dev`

Check the version you have using below:

`npx tsc --version`

It's advisable to install TypeScript as a project-specific dependency. The same version of the language will then be used, regardless of the machine running the code.

Global installation can be done with below command: 

`npm install typescript --global`

version check

`tsc --version`

## Install tsconfig.json

use the below commandline to install and create a `tsconfig.json` file

`npx tsconfig.json`

## Complie TypeScript to JavaScript

Use the below command 

`npx tsc`

## Folder and File Structure

At the moment there is nothing to compile so lets create something to allow for this.

Create a `src` at the root directory, inside `src` create a `main.ts` folder

In `main.ts` add the following lines

```
const sayHello = (name: string):void => {
  console.log(`Hello ${name}`)
}
 
sayHello("TypeScript");
```

if you look at the tsconfig.json file you'll see a this configuration

` "outDir": "./dist"`

This is where the compile `js` files will created, there fore we need to create a `dist` folder

You should end up with a structure looking like this

```
├── dist
│   └── main.js
├── package.json
├── package-lock.json
├── src
│   └── main.ts
└── tsconfig.json
```

NOTE if you are pushing this into gitHub don't forget to add the `.gitignore` file with `node_modules` and `dist` folder to be ignored

## How to Execute TypeScript Files

Install `ts-node` with the below command line

`npm install ts-node --save-dev`

Using `ts-node` will compile TypeScript and run the JavaScript code

use the below command line now to execute TypeScript file:

`npx ts-node src/main.ts`

Terminal should output 

`Hello TypeScript`

## TLDR

| Command                              | What it does   
| ------------------------------------ |-------------------------------------------------|
| `npm install typescript --save-dev`  | Install TypeScript as dependency                | 
| `npm install typescript --global`    | Install TypeScript as globally                  | 
| `npx tsconfig.json`                  | create tsconfig.json file                       | 
| `npx tsc`                            | compiles TypeScript files                       | 
| `npm install ts-node --save-dev`     | package that compiles ts files and runs js files|  
| `npx ts-node src/main.ts`            | excute ts files with ts-node                    |  


