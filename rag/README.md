# Simple RAG Demo

This project is a small Retrieval-Augmented Generation (RAG) example built in
Python. The notebook:

1. Splits `doc.md` into text chunks.
2. Creates Chinese text embeddings with Sentence Transformers.
3. Stores and retrieves chunks with ChromaDB.
4. Reranks the retrieved results with a cross-encoder.
5. Uses Google Gemini to generate an answer from the most relevant context.

## Run locally

The project requires Python 3.12+, [uv](https://docs.astral.sh/uv/), and
Jupyter. Create a `.env` file in this directory containing your Gemini API key:

```env
GEMINI_API_KEY=your_api_key
```

Then install the locked dependencies and start JupyterLab:

```bash
uv sync
uv run --with jupyter jupyter lab
```

Open `main.ipynb` and run the cells in order. The `.env` file contains a secret
and must not be committed to Git.

## Attribution

This learning project is based on MarkTechStation's
[Python RAG example](https://github.com/MarkTechStation/VideoCode/tree/main/%E4%BD%BF%E7%94%A8Python%E6%9E%84%E5%BB%BARAG%E7%B3%BB%E7%BB%9F/rag)
from the `VideoCode` repository.
