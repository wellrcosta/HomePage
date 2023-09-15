---
title: Video2AI
date: 2023/3/15
description: Video Processing with Artificial Intelligence.
tag: nodejs, reactjs, typescript, fastify, openai, personalprojects
author: Reis
---

## About the Project

**video2ai** is a project developed during the Rocketseat NLW AI event. It consists of two parts: an API (located in the `api` directory) and a web interface (located in the `web` directory) that allow you to convert videos into text using OpenAI technology. The API handles interaction with OpenAI and also receives audio from the web interface, while the web interface provides an easy way to use the functionality and converts video to audio before sending it to the API.

## Technologies Used

![Node.js](https://img.shields.io/badge/Node.js-green)
![Typescript](https://img.shields.io/badge/Typescript-blue)
![Prisma](https://img.shields.io/badge/Prisma-orange)
![OpenAI](https://img.shields.io/badge/OpenAI-yellow)
![React](https://img.shields.io/badge/React-blue)
![Typescript](https://img.shields.io/badge/Typescript-blue)
![Vite](https://img.shields.io/badge/Vite-orange)
![FFmpeg](https://img.shields.io/badge/FFmpeg-red)

## How to Run the Project Locally

Below are detailed and simple instructions for running the project on your local machine.

### API

1. Navigate to the `api` folder in your terminal:

```bash
cd api
```

2. Install the dependencies using the following command:

```bash
npm install
```

3. Create a `.env` file in the `api` folder and include the following environment variables:

```env
OPENAI_API_KEY=YourOpenAIApiKey
DATABASE_URL=YourDatabaseURL
```

4. Create a folder called `tmp` inside the `api` folder.
- Note: Otherwise, the API will fail when trying to save the video path in the database.

5. Execute the following command to apply database migrations:

```bash
npx prisma migrate dev
```

6. Now you can start the API server:

```bash
npm run dev
```

The API will be available at [http://localhost:3333](http://localhost:3333).

### Web

1. Navigate to the `web` folder in your terminal:

```bash
cd web
```

2. Install the dependencies using the following command:

```bash
npm install
```

3. Start the web application:

```bash
npm run dev
```

The web interface will be available at [http://localhost:5173](http://localhost:5173).

## Usage Instructions

- Select the video to be used.
- Fill in the "Transcription Prompt" with comma-separated keywords.
- Click "Load."
- After loading, select one of the two generated prompts or create one yourself.
- Select the desired "temperature."
- Click "Run."
- After the operation is completed, you should see the result generated by the AI in the "AI-generated Result" field.