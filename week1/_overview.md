# Week 1

## Disclaimer
Oneirocom is not responsible for any radical shifts in thinking or behavior that may occur as a result of this course.
- Also, since everyone is coming from different backgrounds and skill levels, we are going to start from the very beginning.
- But don't worry, things will get much more interesting very quickly!

## How to get these files

Posted on Github at https://github.com/Oneirocom/Academy

1. git clone OR
2. press the green "Download" button

## Setting up

1. Log into Magick Academy
2. Get an OpenAI account and API key

## Core Concepts

Core concepts are here: https://magick-docs.vercel.app/docs/core-concepts/Overview

### Subgroup of concepts we'll be starting with

- Tokens and Prompts
- Nodes
- Connections
- Graphs (Spells)
- Agents

# Part 1

## Tokens and Prompts

- What is a token? Let's find out!
https://platform.openai.com/tokenizer

-> OpenAI Sandbox- https://platform.openai.com/playground

### Text Completions vs Chat Completions
--> The quick brown fox

--> Chat format and system directives

### Temperate? Top P? WTF?

--> Let's ask ChatGPT!

--> Chat transcript here: [parameters.md](./parameters.md)

--> DALL-E 2
- https://labs.openai.com/

### How to make a great prompt?

 - Single shot vs multishot
 - Get it to work first, then get it to work with less tokens

 --> https://learnprompting.org/

# Part 2
## Introduction to Magick

### Nodes

- Nodes are the basic building blocks of Magick

### Connections

- Connections are the relationships between nodes

### Graphs

- Graphs are a collection of nodes and connections

### Let's make a graph!
--> Hello World example
--> Basic interface overview

## Project - Simple Chatbot

### Input Node
- What is an input?

### Destructure and Event Destructure
- What is destructuring?

{
    type: "apple",
    color: "red",
}

- How do we get the color?

Input looks like:
{
    content: "Hello World",
    ... some other stuff
}

### Text Variable
- What is a variable?
- Strings vs text

### Generate Text

### Output
 - default vs named output

### Adding comments

### Putting it all together and testing

### View the run cost in the Request Window

### Memory
 - We can add short term *and* long term memory, will be covered next week

# Part three

## Set the bot up with Discord

- Register for Discord

- Create a test server

- Discord Developer Portal
https://discord.com/login?redirect_to=%2Fdevelopers%2Fapplications

- Create a new application
https://discordjs.guide/preparations/setting-up-a-bot-application.html#creating-your-bot

https://discordjs.guide/preparations/adding-your-bot-to-servers.html#bot-invite-links
https://discord.com/api/oauth2/authorize?client_id=123456789&permissions=0&scope=bot%20applications.commands

## Creating an agent

- Add API keys
- Enable
