# Advanced-RAG - This repository is consist of exploratory Notebooks of 2 cutting edge RAG pipelines.
## A) Evaluating a Multimodal Fusion RAG Pipeline with Structured Prompting and Image Intelligence

- The whole article can be found at

https://medium.com/@sourish.syntel/multimodal-fusion-rag-evaluating-a-multimodal-fusion-rag-pipeline-with-structured-prompting-and-a541ef922c12

## Implementation and Evaluation of a Multimodal Fusion RAG

__Fusion RAG__ : Combining Multimodal Vector-store and Keyword Search for more accurate retrieval.
A) _semantic vector search_ - Enhanced with multimodal context retrieval(retrieval based on both text and images)
leverages vector embeddings to represent text(and images), enabling efficient retrieval of relevant information based on semantic similarity
B) _keyword-based BM25_ retrieval.(https://en.wikipedia.org/wiki/Okapi_BM25)
BM25 is a traditional bag-of-words algorithm used for text matching. It ranks documents based on term frequency and inverse document frequency.

_See the readme file in the main branch for updated instructions and information._

## B) Evaluating a Graph based Hybrid RAG Pipeline with Structured Prompting

### Hybrid retrieval strategy on a corpus of RAG white papers and articles, combining:

- Semantic Vector Search
- Graph-Based Knowledge Traversal -enhances traditional RAG systems by organizing knowledge/concepts as a connected graph rather than a flat collection of documents

## Installing
Clone this repository into your local machine using the terminal (Mac), CMD (Windows), or a GUI tool like SourceTree by 

```bash
git clone https://github.com/nitsourish/Advanced-RAG.git
```

```bash
pip install -r requirements.txt
```

## Setting Up the OpenAI API Client
We initialize the OpenAI client to generate embeddings and responses with following models

- An important step is to get an OPENAI_API_KEY from https://platform.openai.com/

- Initialize the OpenAI client with the base URL and API key

```bash
client = OpenAI(
    base_url="https://api.openai.com/v1/",
    api_key=os.getenv("OPENAI_API_KEY")  # Retrieve the API key from environment variables
)
```
- text-embedding-3-large: Generates robust text embeddings for semantic similarity
- gpt-4o: The generation workhorse. It's OpenAI's most recent model capable of text and multimodal input processing.
