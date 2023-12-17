## Create a virtual environment and run install the packages from requirements.txt:
- pip install -r requirements.txt

## Use a HuggingFace API Token, create .env file in the folder:
- HUGGINGFACEHUB_API_TOKEN='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'

## Running the python file:
- streamlit run block.py

## Models used:

1 - For Vector Embeddings:
- hkunlp/instructor-xl, link - https://huggingface.co/hkunlp/instructor-xl

2 - For Context Generation based on embeddings and text information:
- google/flan-t5-xxl, link - https://huggingface.co/google/flan-t5-xxl

## Code Flow:
- As per the main function.
- Loading environment variables -> Streamlit page generated -> Can do conversation with LLM -> Upload document -> After processing, query with LLM and get responses.

- How the processing is done?
- Doc uploaded via Streamlit is processed with help of PDFReader library and texts are generated.
- The raw texts are then broken into multiple chunks based on the parameters provided. (Overlapping, etc.)
- Processing of the text chunks to generate vectors based on context, each chuck context gets a vector value, which can be stored locally in a database or in vectordb.
- Once the processing stage is completed, one can query the documents, based on the similarity score of vectors and the query, the LLM generates response from the documents.

- DO some editing in HTML page and also the code flow.
- For better results, use or try other huggingface models.

## - While doing presentation, talk about LangChain, LLM, Vectors, Embeddings, HuggingFace.
