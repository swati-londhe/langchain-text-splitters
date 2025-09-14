LangChain Text Splitting Examples
This repository contains Python scripts demonstrating various text splitting techniques using the LangChain library. These examples showcase how to split text based on language-specific syntax, semantic meaning, character length, and text structure, with applications for processing code, markdown, and natural language documents.
Prerequisites

Python 3.8+
Install required dependencies:pip install langchain langchain-community langchain-experimental langchain-openai python-dotenv


For scripts using OpenAIEmbeddings (e.g., semantic_meaning_based.py), set up an OpenAI API key in a .env file:OPENAI_API_KEY=your_api_key_here


Ensure the dl-curriculum.pdf file is available in the working directory for length_based.py.

Files and Descriptions

python_code_splitting.py

Uses RecursiveCharacterTextSplitter with Language.PYTHON to split a Python class definition into chunks.
Configured with a chunk size of 300 characters and no overlap.
Prints the number of chunks and an example chunk.


markdown_splitting.py

Applies RecursiveCharacterTextSplitter with Language.MARKDOWN to split a markdown document describing a project.
Set to a chunk size of 200 characters with no overlap.
Outputs the number of chunks and the first chunk.


semantic_meaning_based.py

Uses SemanticChunker with OpenAIEmbeddings to split text based on semantic meaning, using a standard deviation threshold of 3.
Processes a mixed-content sample about farming, cricket, and terrorism.
Prints the number of documents and their content.


length_based.py

Employs CharacterTextSplitter to split a PDF ('dl-curriculum.pdf') into chunks of 200 characters each with no overlap.
Loads the PDF using PyPDFLoader and prints the content of the second chunk.


text_structure_based.py

Uses RecursiveCharacterTextSplitter to split a paragraph about space exploration into chunks of 500 characters with no overlap.
Prints the number of chunks and their content.



How to Run

Ensure the .env file is configured with your OpenAI API key (for semantic_meaning_based.py).
Place the dl-curriculum.pdf file in the same folder as length_based.py.
Run any script using Python:python <script_name


