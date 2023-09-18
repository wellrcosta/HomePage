---
title: Creating a TypeScript Node.js API
date: 2023/3/19
description: Learn how to create a TypeScript-based Node.js API for building robust and maintainable web services.
tag: nodejs, typescript, express
author: Reis
---

In this guide, we'll walk through the process of creating a TypeScript-based Node.js API. TypeScript brings static typing and enhanced tooling to Node.js development, making it a popular choice for building robust and maintainable APIs.

## Prerequisites

Before we begin, ensure you have the following installed:

- Node.js and npm (Node Package Manager)
- TypeScript (install it globally using `npm install -g typescript`)
- Your favorite code editor (e.g., Visual Studio Code)

## Step 1: Initialize a New Project

1. Create a new project directory:

   ```bash
   mkdir my-ts-api
   cd my-ts-api
   ```

2. Initialize a new Node.js project and create a `package.json` file:

   ```bash
   npm init -y
   ```

3. Install TypeScript and TypeScript Node for development:

   ```bash
   npm install --save-dev typescript ts-node
   ```

4. Initialize a TypeScript configuration file:

   ```bash
   npx tsc --init
   ```

## Step 2: Create Your API

1. Create a `src` directory and a TypeScript file for your API called `app.ts`.

2. Install Express.js:

   ```bash
   npm install express
   npm install --save-dev @types/express
   ```

3. Write a simple API using Express.js as an example:

   ```typescript
   import express from 'express';

   const app = express();
   const port = 3000;

   app.get('/', (req, res) => {
     res.send('Hello, TypeScript API!');
   });

   app.listen(port, () => {
     console.log(`Server is running on port ${port}`);
   });
   ```

## Step 3: Configure TypeScript

1. Open `tsconfig.json` and configure your TypeScript settings. Here's a basic example:

   ```json
   {
     "compilerOptions": {
       "target": "ESNext",
       "module": "CommonJS",
       "rootDir": "./src",
       "strict": true
     }
   }
   ```

2. Add a `"start"` script to your `package.json` to run your TypeScript code using `ts-node`:

   ```json
   "scripts": {
     "start": "ts-node src/app.ts"
   }
   ```

## Step 4: Build and Run Your API

1. Start your API:

   ```bash
   npm start
   ```

## Step 5: Test Your API

Open your web browser or a tool like [curl](https://curl.se/) and visit `http://localhost:3000` to see your API in action.

## Conclusion

You've successfully created a TypeScript-based Node.js API using Express.js. You can expand upon this foundation by adding routes, controllers, middleware, and database integration as needed for your project.

Happy coding!
