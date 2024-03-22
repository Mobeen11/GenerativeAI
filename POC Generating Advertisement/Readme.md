## Introduction

This repository contains Python code for two different functionalities:

### 1. RAG-based Advertisement Generation

The first part of the code demonstrates the use of RAG (Retrieval Augmented Generations) for generating advertisements targeted at travelers. It utilizes Pinecone for similarity search, Sentence Transformers for generating embeddings, and Replicate for fine-tuning and generating text based on the provided context.
![RAG](https://github.com/Mobeen11/GenerativeAI/blob/main/POC%20Generating%20Advertisement/Untitled%20Diagram.drawio(5).png)

### 2. Tourist Destination Dataset Indexing and Querying

The second part of the code showcases indexing and querying a dataset of tourist destinations using Pinecone, a vector database service. It includes functionalities for preparing the dataset, indexing it into Pinecone, and performing similarity search based on textual descriptions of tourist destinations.

## Requirements

Before running the code, ensure you have the following dependencies installed:

- Python 3.x
- pandas
- sentence-transformers
- tqdm
- Pinecone
- Replicate (for RAG-based Advertisement Generation)

## Usage

### RAG-based Advertisement Generation

1. Set up Pinecone: Obtain an API key from Pinecone and replace the empty string in the code with your API key:

    ```python
    pc = Pinecone(api_key="YOUR_API_KEY_HERE")
    index = pc.Index("tourist-index")
    ```

2. Set up Replicate: Set your Replicate API token as an environment variable:

    ```bash
    export REPLICATE_API_TOKEN="YOUR_API_TOKEN_HERE"
    ```

3. Run the code: Execute the Python script or Jupyter Notebook containing the provided code snippets.

### Tourist Destination Dataset Indexing and Querying

1. Set up Pinecone: Obtain an API key from Pinecone and replace the placeholder in the code with your API key:

    ```python
    pc = Pinecone(api_key="YOUR_API_KEY_HERE")
    index = pc.Index("tourist-index")
    ```

2. Prepare the dataset: Modify the `dataset` variable to include the desired tourist destinations, categories, and descriptions.

3. Run the indexing code: Execute the Python script or Jupyter Notebook containing the provided code snippets to index the dataset into Pinecone.

4. Perform queries: Use the `run_query` function to search for destinations based on a query.

## Functionality

### RAG-based Advertisement Generation

1. **Similarity Search**: The code performs a similarity search using Pinecone, allowing you to find relevant context based on a given query.

2. **Text Embedding**: Sentence Transformers are used to generate embeddings for the input text.

3. **Text Generation**: Replicate is utilized for generating engaging advertisements targeted at travelers based on the context retrieved from the similarity search.

### Tourist Destination Dataset Indexing and Querying

1. **Dataset Indexing**: The code indexes a dataset of tourist destinations into Pinecone, associating each destination with its respective metadata and embedding.

2. **Text Embedding**: Sentence Transformers are utilized to generate embeddings for the textual descriptions of tourist destinations.

3. **Similarity Search**: Pinecone allows for efficient similarity search based on embeddings, enabling the retrieval of destinations similar to a given query.

## License

This code is provided under the [MIT License](LICENSE). Feel free to modify and distribute it according to your needs.
