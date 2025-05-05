# ChunkWise_AI
ChunkWise AI is an intelligent chatbot system that transforms large documents into searchable, semantically meaningful chunks using LangChain, FAISS, and OpenAI. It finds and retrieves only the most relevant information, delivering fast, precise answers with minimal token usage — making knowledge more accessible, efficient, and scalable.

Day 1 of the project.

Tired of Copy-Pasting Articles into ChatGPT? So was I.

Ever found yourself copying long articles into ChatGPT just to get fragmented responses or hit token limits?
I’ve been there—it's tedious, inefficient, and not scalable.

🔍 The issues:

Manual copy-paste is painful.

Most models choke beyond ~3000 words.

We often need just the right chunk, not the whole article.

So I started building a solution:
An AI assistant that reads, understands, and responds based on semantically relevant chunks using Langchain, FAISS, and OpenAI.

Stay tuned. In this mini-series, I’ll walk you through the entire dev journey—from ingestion to chat UI.

#LLM #Langchain #VectorSearch #AIChatbot #SemanticSearch

![image](https://github.com/user-attachments/assets/c19e25a0-dd9c-4c59-93ae-95477bc6da1c)

Day2 of the project.

🚀 What Powers an Intelligent Chatbot? Let’s Break It Down.

When you ask an AI a smart question, there’s an entire hidden engine working behind the scenes.

For my project, I designed a simple but powerful AI knowledge engine made of these moving parts:

🔹 Load Documents → Bring in raw content
🔹 Chunk & Split → Break it into smaller, meaningful pieces
🔹 Embed → Turn those pieces into numbers (vectors!)
🔹 Vector Store (FAISS) → Save them smartly for lightning-fast search
🔹 Retriever → Grab only the relevant chunks for your question
🔹 LLM (OpenAI) → Generate a focused, clear answer
🔹 Chatbot UI (React/Streamlit) → Show you the final magic 💬

Every piece has a reason.
Without proper chunking, we overfeed the LLM.
Without semantic search, answers become random.

Tomorrow, I’ll dive deeper into how we split and embed documents like a pro.

👀 Here’s the roadmap visual for today—makes it way easier to understand 👇

#AI #LLM #Langchain #VectorSearch #OpenAI #ReactJS #Streamlit #DeveloperJourney

![image](https://github.com/user-attachments/assets/7b6a347b-5a36-464d-94e0-6153e75e7e91)

🧠 Turning Big Documents into Bite-Sized Intelligence

Imagine throwing a full 50-page article into a chatbot — without overwhelming it.
That’s where smart chunking comes in.

In this project, we don’t just cut text randomly.
We split it strategically to keep meaning intact.
⚙️ Here's how the process flows:
1. Load Content: Use LangChain’s TextLoader or UnstructuredURLLoader.
2. Naive Split? No thanks: Simple slicing cuts words awkwardly.
3. Recursive Splitting: Enter RecursiveCharacterTextSplitter!
 It tries to split by:
Paragraphs → Sentences → Words → Characters — keeping chunks balanced and readable.

✅ This ensures that:
Each chunk stays within token limits,
Context isn’t lost,
And we feed the LLM only what matters.

Tomorrow, I’ll show how these smart chunks are transformed into vectors and stored for lightning-fast semantic search.

Here’s a visual of today’s pipeline 👇
hashtag#SemanticSearch hashtag#LLM hashtag#LangChain hashtag#DocumentProcessing hashtag#ChunkWiseAI

![image](https://github.com/user-attachments/assets/dc1d29e8-775b-4f0d-b093-50b849c61871)

📦 Turning Text into Math: The Power of Embeddings

Now that we’ve split our documents into smart chunks… how does AI actually understand them?

Welcome to Embeddings — the secret sauce of semantic search.


🔍 Instead of comparing words literally, we transform them into vectors —number-based representations that capture meaning and context.

🧬 For example:

“iPhone review” and “Apple product feedback” may look different as text...

…but embeddings bring them closer in vector space 🌌

Here’s what I used: 

✅ Model: all-MiniLM-L6-v2 via SentenceTransformers

✅ Database: FAISS – a fast similarity search engine by Facebook

✅ Why FAISS? It indexes vectors to help us instantly retrieve the most relevant chunks when a question is asked.


Tomorrow, we go full circle: how LLMs use these vectors to craft responses — fast, smart, and cost-effective.

🎯 Visual breakdown of today’s concept 👇

#Embeddings #VectorSearch #FAISS #LLM #AIpipeline #LangChain #ChunkWiseAI
![image](https://github.com/user-attachments/assets/0e0d8210-9579-4e71-bea3-1aacc383d3d0)

💬 How I Built a Chatbot That Thinks Before It Speaks

We’ve chunked the docs.
Embedded their meaning.
Indexed them in a vector database.
Now what?

We bring it all together in an intelligent chatbot that can understand your questions and retrieve just the right knowledge.

⚙️ Here's how it works:

You ask a question.

The chatbot converts it into a vector using embeddings.

It searches the FAISS index for semantically similar chunks.

The LLM reads only those — and gives a smart, cost-efficient reply.

Bonus:
✅ We avoid token overload using Map-Reduce or Refine methods for long contexts.
✅ Memory lets the bot remember past queries to maintain conversation flow.

🚀 It’s like ChatGPT, but with your own data — deeply integrated, hyper-relevant, and blazing fast.

📦 Built with:

LangChain

FAISS

OpenAI

Streamlit (UI)

React frontend (coming soon)

Check out this final roadmap of the full pipeline 👇

#AIchatbot #LangChain #SemanticSearch #FAISS #LLM #Streamlit #ChatWithDocs #ChunkWiseAI

![image](https://github.com/user-attachments/assets/d0fad1c1-d578-4155-8586-12e8f5bb65d3)

🚀 From Idea to Execution: The AI Chatbot Project is LIVE!

6 days ago, this was just a wild idea:
“Can we make ChatGPT answer questions from our own docs?”

Today, it's a working, scalable chatbot powered by:
✅ LangChain
✅ FAISS
✅ OpenAI
✅ Streamlit
✅ React (coming soon)

🌟 What it can do:

Ingest and process lengthy documents/webpages

Convert them into smart chunks

Store their meanings in a vector DB

Let you ask anything, and get contextual, fast responses

🎯 Key Takeaway:
You don't need to be an AI researcher to build powerful tools — just the right architecture, creativity, and motivation.

👨‍💻 Full code is now on GitHub → (Link in comments)
This wraps up the “Chat With Docs” dev series — but new experiments are on the way.

🙌 Thanks for following along! Drop a 🔥 if you'd try building something similar!

#AI #Chatbot #LLM #LangChain #SemanticSearch #OpenAI #FAISS #Streamlit #DevJourney






# ChunkWise_AI: News Research Tool 

ChunkWise_AI is a user-friendly news research tool designed for effortless information retrieval. Users can input article URLs and ask questions to receive relevant insights from the stock market and financial domain.


## Features

- Load URLs or upload text files containing URLs to fetch article content.
- Process article content through LangChain's UnstructuredURL Loader
- Construct an embedding vector using OpenAI's embeddings and leverage FAISS, a powerful similarity search library, to enable swift and effective retrieval of relevant information
- Interact with the LLM's (Chatgpt) by inputting queries and receiving answers along with source URLs.


## Installation

1.Clone this repository to your local machine using:

```bash
  git clone https://github.com/Poorna-Chandra-D/ChunkWise_AI.git
```
2. Install the required dependencies using pip:

```bash
  pip install -r requirements.txt
```
3.Set up your OpenAI API key by creating a .env file in the project root and adding your API

```bash
  OPENAI_API_KEY=your_api_key_here
```
## Usage/Examples

1. Run the Streamlit app by executing:
```bash
streamlit run main.py

```

2.The web app will open in your browser.

- On the sidebar, you can input URLs directly.

- Initiate the data loading and processing by clicking "Process URLs."

- Observe the system as it performs text splitting, generates embedding vectors, and efficiently indexes them using FAISS.

- The embeddings will be stored and indexed using FAISS, enhancing retrieval speed.

- The FAISS index will be saved in a local file path in pickle format for future use.
- One can now ask a question and get the answer based on those news articles

## Project Structure

- main.py: The main Streamlit application script.
- requirements.txt: A list of required Python packages for the project.
- faiss_store_openai.pkl: A pickle file to store the FAISS index.
- .env: Configuration file for storing your OpenAI API key.


