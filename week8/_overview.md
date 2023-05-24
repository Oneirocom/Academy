# Week 5

## Subspell Node
You can load spells into spells. You can do this in a fixed way with the Spell node, or in a dynamic way with the "Get Spell By Name" node

A limitation of dynamic spells is no public variables or data inputs. Public variales working now, subspells coming soon. We pass data by adding it to the event object we pass in.

## Skill Node
Skills are a type of subspell, but they take in task data instead of an input event

## Intents
The first thing we need to know is what the user or agent wants to do. This is called an "intent", and usually describes the query that calls the intent as well as how the response is handled by the agent. In a traditional NLP system like Amazon Echo, the Alexa determines the intent from the user's utterance and calls the relevant skill.

## Tool
"Tool" is an abstraction to create a common interface for the language model to interact with. A tool is a node that has a set of inputs and outputs, along with some parameters. A good example of a tool is "Google Search". The inputs are the search terms, the outputs are the search results, and the parameters are the search engine and the number of results to return.

Magick describes tools as nodes which can be used inside graphs

## Skill
"Skill" is a similar abstraction to tool, but it describes a process of how a tool can be used. Skills tend to be more complex and handle conditional logic-- i.e. if the user says "yes" then do this, if the user says "no" then do that. An example skill could also be "Google Search". The skill takes the search terms as input, and then calls the Google Search tool. The skill then takes the results and displays them to the user. The difference between the tool and skill is that the prompting, error handling, and other logic is handled by the skill.

In a system like AutoGPT or most chain-of-thought systems, the reasoning is generalized and only tools are used. In Magick we emphasize skills so we can have more control and a better testing flow, leading to better likelihood of success.

## Tasks
A task is something that an agent does to accomplish a goal.

An example task would be "search the web for everything about elephants and return the result".

Tasks have an objective and are completed in steps.

## Steps
Tasks are completed in steps. Each step starts with reasoning over the previous task steps, then selection of skill for the next step, then execution of the skill, then reflection on the execution.

## OODA
Observe, Orient, Decide Act
https://en.wikipedia.org/wiki/OODA_loop

## Task flow
1. Identify the task objective
2. Create the task with the objective
3. Reason about the first step (probably planning)
4. Find the relevant skill
5. Execute the skill
6. Reflection on if the execution was successful or not
7. Repeat steps 3-6 until the task is complete

## Some example skills
1. Plan
2. Complete task
3. Cancel task
4. Search long-term memory
5. Search web
6. Get user input