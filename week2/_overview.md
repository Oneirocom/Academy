# Week 2

# PART 0
Review last week's material

# PART 1

# What are we building toward?
- Autonomous Agents
- AGI - Artificial General Intelligence

- https://github.com/yoheinakajima/babyagi
- https://github.com/Torantulino/Auto-GPT

# A Note On Safety
- We are playing with fire
- Fire is VERY useful
- But we need to be careful and respectful so we don't hurt anyone

# What is and isn't okay for a Magick Cloud agent to do?
- Anything that is not okay for a human to do is not okay for an agent, either
- Hacking, disinformation, spamming, lying, stealing, etc.
- Torture, creepy stuff is off limits
- Adult stuff is okay as long as it is consensual and not illegal
- If it is fun or it helps people it's probably okay

# Types of AGI Safety

### Existential Risk
- Yud thinks we're all gonna die - https://www.youtube.com/watch?v=AaTRHFaaPG8
- Sam does not https://www.youtube.com/watch?v=L_Guz73e6fw

### Bias (+ Racism and Bigotry)
- Emily Bender - On the Dangers of Stochastic Parrots: Can Language Models Be Too Big? 🦜 https://dl.acm.org/doi/10.1145/3442188.3445922
- Timnit Gebru, ex-Google AI ethics researcher - https://www.youtube.com/watch?v=b_--xrN3eso

### Democratization of AGI
Emad Mostaque - Technology is not neutral and you get good and bad. Open versions of this technology are essential for the global south which is most of humanity.

- Ben Goertzel -- Democracy and Decentraliation are key
https://www.youtube.com/watch?v=XHTdVve3Wj0

- Timnit Gebru - Is AI racist and undemocratic?
https://www.aljazeera.com/program/talk-to-al-jazeera/2022/8/6/timnit-gebru-is-ai-racist-and-antidemocratic

### Being kind to superintelligence!
- Blake Lemoine, ex-Google researcher
- *During my conversations with the chatbot, some of which I published on my blog, I came to the conclusion that the AI could be sentient due to the emotions that it expressed reliably and in the right context. It wasn't just spouting words.*

# As a Magick user, what can I do to help?
- Be kind to your agents
- Don't be a jerk
- Make things that improve the world and people's lives
- Don't make things that hurt people

# PART 2

# The cognitive loop
-> Input -> Memory -> External Knowledge -> Reasoning -> Response -> Output

Yann's cognitive model
https://ai.facebook.com/blog/yann-lecun-advances-in-ai-research/
https://scontent-sjc3-1.xx.fbcdn.net/v/t39.2365-6/274669205_502772811472072_6182865979039521197_n.jpg?_nc_cat=102&ccb=1-7&_nc_sid=ad8a9d&_nc_ohc=klAhuX00ha4AX8iab2c&_nc_ht=scontent-sjc3-1.xx&oh=00_AfARSUdxCNiN0QnpM3qG74XY4ESjgZj7gD58KdHPtktrwg&oe=643B1846

## So what are we missing from our current agents?
- Short term memory
- Long term memory
- External knowledge
- Reasoning

### Today we will cover short term memory and long term memory

## How can we emulate these things?
- We can use a standard database to store and recall short term memory
- We can use a specialized vector database to store and recall long term memory
- We can use data sources (Google, Wikipedia, etc.) to get external knowledge
- We can use our language model to reason

## Implementing short term memory with events
- Event store node
- Event recall node
- Events to conversation node
- Demonstration of using a database to store and recall short term memory

## What is a database?
- A database is a collection of data
- It's basically just a glorified Excel spreadsheet

## What is a vector?
Just a series of numbers
[0.0293021, 0.923849023, 0.0239]

Examples of text2vec
- https://huggingface.co/spaces/KaiCao/GanymedeNil-text2vec-cmedqq-lert-large

## What is an embedding?
- An embedding is a numerical representation of a word or phrase
- Essentially we've turned our sentence into something the computer can understand
- Embeddings are made by Language Models, specifically we use ada from OpenAI

## What is a vector database?
- A vector database is a database that stores vectors and lets us search them
- Imagine that each vector is a point in space, and we want to find the closest point to a given point
- This is called a nearest neighbor search

- Two kinds of nearest neighbor search -- we use both ANN and KNN

- ANN -- most popular. Weaviate, Milvus, FAISS, Qdrant, etc
- KNN -- slower, easier to integrate and simpler. pgvector for postgres

Vector search libraries
Facebook FAISS - https://engineering.fb.com/2017/03/29/data-infrastructure/faiss-a-library-for-efficient-similarity-search/
Weaviate - https://weaviate.io/
Qdrant - https://qdrant.tech/
Chroma - https://www.trychroma.com/

Explanation of how vector database works
https://www.youtube.com/watch?v=YkK5IKgxp-c

- All popular search databases use HNSW (ANN)
HNSW paper - https://arxiv.org/abs/1603.09320

## Implementing long term memory with vectors
- Create embedding node
- Get cached embedding node
- Store event with embedding
- Recall event by embedding

## Implementing external knowledge with data sources
- Google Search node