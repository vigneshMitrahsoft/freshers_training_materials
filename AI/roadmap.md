The order I would follow

Week 1:

1. Embeddings
2. Vector
3. Similarity Search

Week 2:

4. Vector Databases
5. Top-K
6. Chunking

Week 3:

7. RAG

Week 4:

8. Prompt Engineering
9. Tool Calling
10. Structured Outputs

Week 5:

11. Evaluation (Evals)
12. LLM-as-a-Judge

Week 6:

13. Agents
14. LangGraph
15. MCP



If I were mentoring a Python backend developer, the exact order I'd recommend is:
1. Embeddings
2. Context Window
3. Attention
4. Transformer Architecture
5. Inference
6. Temperature / Top-K / Top-P
7. Prompt Engineering
8. LLM APIs
9. Tool Calling
10. RAG
11. Evaluation
12. Agents

At your current stage, Embeddings and Context Window will give you the biggest
return. Once those two click, many Al terms that currently feel like random jargon
start fitting into a coherent picture.









Final List:

Phase 1 — Understand How LLMs Work (Week 1):
Context Window
Inference
Temperature
Top-K
Top-P

Phase 2 — Embeddings & Retrieval (Week 2):
Vector
Embeddings
Similarity Search
Cosine Similarity
Top-K Retrieval

Input Text
↓
Tokenization
↓
Context
↓
Prediction
↓
Output

Phase 3 — Vector Databases (Week 3)

Now learn:

Why normal SQL search isn't enough
Vector Database
Indexing
Nearest Neighbor Search

Examples:

Pinecone
Weaviate
Qdrant
Chroma

Don't install anything yet.

Just understand the purpose.

Goal:

Answer:

Why does a vector database exist?


Phase 4 — Chunking & RAG (Week 4)

Now combine everything.

Learn:

Chunking
Retrieval
Augmentation
Generation

Mental model:

Documents
↓
Chunking
↓
Embeddings
↓
Vector DB
↓
Top-K Search
↓
LLM
↓
Answer

This is the first point where RAG will feel natural.


Phase 5 — Prompt Engineering (Week 5)

Now learn:

System Prompt
User Prompt
Few-Shot Prompting
Structured Prompting

Build:

Prompt
↓
LLM
↓
Output

Experiment:

Change prompts	
Compare outputs

Goal:

See how instructions affect behavior.


Phase 6 — APIs & Structured Outputs (Week 6)

This is where your backend experience becomes valuable.

Learn:

LLM APIs
JSON Mode
Structured Outputs
Function Calling

Mental model:

User
↓
Backend
↓
LLM API
↓
JSON
↓
Backend

Very similar to external API integrations.


Phase 7 — Tool Calling (Week 7)

Learn:

User
↓
LLM
↓
Tool Request
↓
Weather API
↓
LLM
↓
Answer

Build:

Calculator tool
Weather tool
Database lookup tool

Goal:

Understand that an agent is basically an LLM that can use tools.

Phase 8 — Evaluation (Week 8)

Most beginners skip this.

Learn:

Ground Truth
Precision
Recall
Relevance
Faithfulness
LLM-as-a-Judge

Think:

Unit Test

for AI systems.

Goal:

Learn how companies determine whether an AI app is actually working.


Phase 9 — Agents (Week 9)

Now agents will finally make sense.

Learn:

Memory
Planning
Tool Selection
Agent Loops

Mental model:

Reason
↓
Choose Tool
↓
Observe Result
↓
Reason Again


Phase 10 — LangGraph & MCP (Week 10)

Only now.

LangGraph

Think:

Workflow Engine

for agents.

MCP

Think:

Standard API Contract

between AI and tools.

As a backend developer, MCP is often easier to understand than many AI concepts because it resembles integration architecture.


Phase 11 — Speech (Optional Modality)

After you can build text pipelines (RAG / agents), add voice.

Learn:

Automatic Speech Recognition (ASR / STT)
Batch vs Streaming
WER
Whisper (API + local)
Text-to-Speech (TTS) briefly

Mental model:

Audio
↓
ASR → text
↓
LLM / RAG / Agent   (Phases 4–10, unchanged)
↓
(optional) TTS → spoken reply

Notebook: `13.automatic_speech_recognition.ipynb`