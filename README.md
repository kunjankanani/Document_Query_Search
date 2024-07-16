# Document_Query_Search (RAG)

Document Query Search also know as ```Retrieval-Augmented Generation```, or RAG, is an innovative approach that enhances the capabilities of pre-trained large language models (LLMs) by integrating them with external data sources. This technique leverages the generative power of LLMs (Large Language Model), and combines it with the precision of specialized data search mechanisms. The result is a system capable of providing nuanced, contextually relevant responses that go beyond the model's initial training data.

### Why RAG?

- **Up-to-Date Information**: Traditional LLMs are limited by their training data, which has a cutoff date. RAG allows the model to access the latest information, ensuring responses are current and relevant.
- **Reduced Hallucinations**: LLMs can sometimes generate confident but inaccurate or "hallucinated" responses. RAG mitigates this by retrieving accurate data from authoritative sources.
- **Contextual Relevance**: By fetching specific information related to the query, RAG ensures that the responses are tailored to the user's context, providing a more personalized experience.

### Applications of RAG

RAG can be particularly useful in scenarios where up-to-date or specialized knowledge is required. For example, it can power a customer support chatbot that provides precise answers to queries about product specifications, troubleshooting, or warranty information by accessing a company's product database and user manuals.


# How It Works


![image](https://github.com/kunjankanani/Document_Query_Search/assets/115248453/b3c39351-f7d9-4882-92dd-5bb4af76d6a6)

1. **Input: Documents**
   - The process begins with a set of documents. These documents can be any type of text, such as articles, reports, or web pages.
   - The goal is to extract relevant information from these documents to answer questions.

2. **Generate Document Chunks**
   - The documents are split into smaller chunks. These chunks could be paragraphs, sentences, or other meaningful segments.
   - By breaking down the documents, we create more manageable units for further processing.

3. **LLM Embedding**
   - Each document chunk is transformed into a numerical representation using a language model (such as an LLM - Large Language Model).
   - This embedding captures the semantic meaning of the text and encodes it as a vector.

4. **Vector Database**
   - The embeddings of document chunks are stored in a vector database.
   - Each embedding is associated with a unique chunk ID, allowing efficient retrieval.

5. **Input: Question**
   - A user submits a question. This question also undergoes LLM embedding to create a vector representation.

6. **Retrieve Relevant Document Chunks**
   - The question's embedding is used to search the vector database.
   - The database returns relevant document chunk IDs based on similarity to the question's embedding.

7. **Combine Chunks and Question**
   - The retrieved document chunks are combined with the original question.
   - This combined text serves as a prompt for another LLM Text model.

8. **LLM Text Model (Answer Generation)**
   - The LLM Text model generates an answer based on the combined prompt.
   - It leverages the context from both the question and the relevant document chunks.

9. **Final Answer**
   - The output of the LLM Text model provides the final answer to the user's question.


****

# How To Run Application

1. **Run in Google Colab** *Recommend*
   - Uploade Document_Query_Search.ipynb file in your google colab and Change runtime type to **```GPU```** for fast execution. Run all cell in your colab.

2. **Run in your local machin**
   - **```Run on CPU```**
        - in ex.env file chenge ```DIVICE_TYPE``` to **CPU**
   - **```Run on GPU```**
        - in ex.env file chenge ```DIVICE_TYPE``` to **GPU**
    
```
You also chenge LLM model

chenge MODEL_PATH
```

```
✨  Your document is placed inside the source_documents folder.
✨  It is also possible to insert multiple documents at time.
```

****

# Demo

I ask query ```all boys are allow in team ?``` so application provide humanize answer using Guidelines.pdf document.

### Ask query in Application snapshot

![image](https://github.com/kunjankanani/Document_Query_Search/assets/115248453/5dda3555-63fd-496b-b84d-6a9ee4f27c65)

### Guidelines.pdf Document snapshot

![image](https://github.com/kunjankanani/Document_Query_Search/assets/115248453/bdcb14ce-edff-4338-8c45-4f8514e7e115)



