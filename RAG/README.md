# RAG Tutorial
Let's say we have a chatbot that has been trained on a very large dataset. Now if you ask it a very specific question, it might not be able to answer it because it has not been trained on that specific data.

We can use Retrieval-Augmented Generation (RAG) to solve this problem. RAG is a technique that allows us to use a large language model to answer questions based on a specific dataset.

To understand RAG, we first need to understand what are embeddings.

## Embeddings
Embeddings are a way to represent data so that computers can understand it. We encode the data into a vector of numbers. These vectors are sorted in a way that similar data points are close to each other. 

These embeddings are stored in a vector database. In vector DB, we can query the database to find the most similar data points to the query on the basis of cosine similarity.

For example, the text embeddings for "Computer Terminal" will encodes properties like actions (typing commands), technology, user interaction and even cultural references.

**Note:** Embeddings are not just for words. We can also use embeddings for sentences,images, audio, video, etc. For sentences, we can create embeddings for each word and then average them to get a sentence embedding.

## Retrieval Augmented Generation
Retrieval Augmented Generation (RAG) is a technique that allows us to use a large language model to answer questions based on a specific context.

RAG is a two-step process:
1. Retrieval: We retrieve the most relevant data points from the vector database.
2. Generation: We use the large language model to answer the question based on the retrieved data points.

## RAG Pipeline
Let's say we have a large document that we want to use to answer questions. Now, there is an issue with this. The document is too large to be used as a context for the language model. So, we need to break down the document into smaller chunks. This is called chunking. 

We take that whole large document and split it into smaller chunks. Now, we can use the embeddings models to generate embeddings for each of these chunks and store them in a vector database. There are two proeprties of embeddings that we need to consider: 
- Chunk Size: The size of the chunk.
- Overlap: The amount of overlap between chunks.

Once we get the embeddings, we can store them in a vector database. Now, we can query the vector database to find the most relevant data points to the query.



