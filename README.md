# RAG (Retrieval-Augmented Generation) Implementation

## Quick Introduction to RAG

 The idea behind RAG is to leverage both retrieval and generation mechanisms to improve the quality of generated responses.

1. **Document Embedding**: First, documents or pieces of information are embedded into high-dimensional vectors using a pre-trained encoder model. These embeddings represent the semantic content of the documents.

2. **Vector Store Creation**: These document embeddings are stored in a vector database or store

3. **Query Embedding**: When a user inputs a query, it is also embedded into an high-dimensional vector using the same encoder model.

4. **Retrieval**: The query embedding is then used to search the vector store for the most relevant document embeddings. This retrieval step returns a set of documents/chunks or passages that are most semantically similar to the query.

5. **Context Construction**: The retrieved documents are combined to form a context, which can be used to provide additional information to the generative model.

6. **Generation with LLM**: The context, along with the query, is fed into an LLM. When used, the system prompt can set the initial context or provide specific instructions to the model.

7. **Response Generation**: The LLM analyzes the provided context and query, generating a coherent and contextually relevant response based on the retrieved information.


## Models Compatibility with System Prompts

### Gemma Models
Gemma models have been identified as not supporting system prompts. This limitation can affect their flexibility and performance in scenarios where initial context-setting or guidance is crucial for generating appropriate responses.

### Mistral Models
Mistral models support system prompts. This feature allows users to define an initial prompt that sets the context or provides specific instructions for the model

### Camel Models
Similar to Mistral, Camel models also support system prompts.

## Useful Resources

- [Prompting Guide](https://www.promptingguide.ai/models)
- [LlamaIndex Documentation](https://docs.llamaindex.ai/en/stable/understanding/)
