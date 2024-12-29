## 🌐 Chat with Webpage using Llama3 and RAG
- This project provides an interactive Streamlit app that enables users to query and interact with the content of a webpage using a Retrieval-Augmented Generation (RAG) setup and the local llama3.2 model.

### ✨ Features
- 🛠️ Webpage Loader: Extracts content from a user-provided webpage.
- 🔍 Text Splitter: Divides webpage content into manageable chunks for embedding and retrieval.
- 📦 Vector Store: Utilizes Chroma for storing and retrieving embeddings.
- 🤖 Language Model Integration: Uses Ollama's llama3.2 model to answer user queries based on retrieved webpage content.

### 🗂️ Project Structure

#### 🔑 Core Components
- 🎛️ Streamlit Interface: Provides a user-friendly interface for loading a webpage and asking questions.
- 🌐 WebBaseLoader: Loads content from a webpage.
- ✂️ Text Splitter: Splits the webpage content into smaller chunks for effective retrieval.
- 📚 Vector Store: Stores and retrieves content embeddings.
- 🤝 Ollama Integration: Leverages the llama3.2 model for generating responses.

### 🧑‍💻 Usage

- Provide Webpage URL: 🌐 Enter the URL of the webpage you want to analyze in the input field.
- Load Webpage Content: 📥 The app will load the content of the webpage and preprocess it.
- Ask Questions: ❓ Input any question related to the webpage’s content in the provided text field.
- View Responses: ✨ The app will generate a response using the llama3.2 model, augmented by the retrieved context.

### 🧩 Components in Detail

##### 🌐 Webpage Loading
- Module: WebBaseLoader
- Description: Fetches the HTML content of the provided webpage URL.

##### ✂️ Text Splitting
- Module: RecursiveCharacterTextSplitter
- Description: Splits the webpage content into chunks of 500 characters with a 10-character overlap for better embedding and retrieval.

##### 📚 Embeddings and Vector Store
- Embeddings: Generated using OllamaEmbeddings with the llama3.2 model.
- Vector Store: Content embeddings are stored and queried using Chroma.

##### 🤖 Llama3 Integration
- Model: llama3.2
- Integration: Uses ollama.chat() to interact with the language model.
- Context: Combines retrieved content chunks to provide context for generating responses.

##### 🔄 RAG Setup
- Retriever: Queries the vector store to retrieve the most relevant content.
- Chain: Combines retrieved content into a formatted context and queries the language model.

##### 🛠️ Example Workflow
- 🌐 Enter the URL: https://example.com
- ❓ Ask a Question: "What is this webpage about?"
- ✨ View Response: The app fetches content, retrieves relevant context, and provides an intelligent answer.

