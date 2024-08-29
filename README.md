# LLM-Custom-Langchain

This project is built using the LangChain framework to process and query documents. The primary focus is to load documents, split them into manageable chunks, and store them in a vector database using OpenAI embeddings. The project is designed to retrieve relevant document chunks based on user queries and generate responses using the Mistral model via the Ollama interface.

Features
Document Loading: Load PDF documents from a specified directory.
Text Splitting: Split documents into smaller chunks to ensure efficient processing and querying.
Vector Store: Store document chunks as embeddings in a Chroma vector database.
Query Processing: Retrieve relevant document chunks based on a user's query using similarity search.
Response Generation: Generate answers from retrieved chunks using the Mistral model.
Project Structure
app.py: The main script to load, split, and store documents in the Chroma vector database. It includes an option to reset the database before adding new data.
query_data.py: The script to handle user queries. It retrieves the most relevant document chunks from the vector database and generates a response using the Mistral model.
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/langchain-llm-project.git
cd langchain-llm-project
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Set up environment variables:

Create a .env file in the project root.
Add your OpenAI API key and other necessary environment variables.
makefile
Copy code
OPENAI_API_KEY=your_openai_api_key
Run the document ingestion process:

bash
Copy code
python app.py --reset
This will load the documents from the data/ directory, split them into chunks, and store them in the Chroma vector database.

Usage
Query the database:

bash
Copy code
python query_data.py "Your query here"
The script will retrieve relevant document chunks and generate a response.

Next Steps: Integrating with Streamlit
The next step for this project is to integrate it with Streamlit to create a clean and user-friendly front end. This will allow users to input their queries directly through a web interface and view responses without needing to run scripts from the command line.
