# Philosophers' Debate Simulator

This project uses AI to simulate philosophical debates between historical thinkers, such as Aristotle and Nietzsche, based on their original texts. By transforming philosophical works into a searchable knowledge base, the simulator allows users to ask abstract questions—like "What is justice?" or "What is the self?"—and receive AI-generated responses that reflect each philosopher's reasoning and style.

## Project Description

The goal of this project is to improve how philosophy is studied by moving away from rote memorization toward AI-powered dialogue simulations.  
We use classical philosophical texts (e.g., *Aristotle’s Physics*) to build a searchable vector database.  
When users input a philosophical question—such as *"What is justice?"* or *"What is love?"*—the system retrieves relevant text segments and simulates how each philosopher might respond, preserving their unique reasoning styles.

This project integrates:
- PDF preprocessing of classical texts
- OpenAI embeddings
- MongoDB Atlas vector search
- LangChain framework for retrieval
- Gradio for interactive UI

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Philosophers-Debate-Simulator.git
cd Philosophers-Debate-Simulator
```

### 2. Set Up Your Environment

Install dependencies:

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install openai pymongo langchain gradio
```

Create a `.env` file and add your credentials:

```bash
OPENAI_API_KEY=your-openai-key
MONGODB_URI=your-mongodb-uri
```

### 3. Run the Project

Open and run the notebook `Langchain_Mongo_Philosophy.ipynb` to step through the entire pipeline—from document processing to chatbot deployment.

## File Structure

```
Langchain_Mongo_Philosophy.ipynb    # Main notebook: data loading, embedding, simulation
data/                               # Folder containing sample philosophical texts
assets/                             # Project poster and visuals
README.md                           # Project documentation
requirements.txt                    # Python dependencies
.env                                # Environment variable config (excluded from repo)
```

## Analysis

- **Text Processing**: Used LangChain PDF loaders and recursive character splitters to divide texts into segments.
- **Embedding**: Applied OpenAI’s embedding model to convert segments into vector format.
- **Storage & Retrieval**: Stored vectors in MongoDB Atlas using the AtlasVectorSearch module for similarity-based search.
- **AI Simulation**: Retrieved relevant text segments and prompted OpenAI’s LLM to generate philosopher-style responses.

## Results

Our system successfully simulates dialogue between philosophers based on their texts.  
For instance, on the question **“What is love?”**, Aristotle emphasizes virtue and growth, while Nietzsche focuses on power and emotion.  
This comparative approach reveals how different traditions respond to the same core ideas.

### Future Improvements

- Add more philosophers (e.g., Plato, Kant, Confucius)  
- Support web-based chat interface  
- Expand document preprocessing for multilingual texts  

## Contributors

- 112ZU1017 曾秭翊  
- 112ZU1048 陳雨柔
- 113ZU1017 陳玟佑 
- 113ZU1055 盧家愛  
- **Professor**: 卞中佩  

## Acknowledgments

Special thanks to the **Introduction to AI** course at 國立政治大學 for guidance and support.  
We also appreciate the open-source tools provided by LangChain, OpenAI, MongoDB Atlas, and Gradio.

## References

- https://github.com/advapplab/ici_template  
- https://platform.openai.com/docs/guides/embeddings  
- https://www.mongodb.com/docs/atlas/vector-search/  
- https://www.langchain.com/  
- https://www.gradio.app/
