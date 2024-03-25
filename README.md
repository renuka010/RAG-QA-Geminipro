# Generative QA - RAG(Gemini-pro)
This repository implements a **Generative Question Answering (QA)** using the **Retrieval-Augmented Generation** (RAG) approach. It leverages Haystack, an open-source AI framework, and Google's powerful **Gemini-Pro** generative model. The Pipeline is designed to generate answers to questions based on custom data extracted from two books.

## Overview

The pipeline follows these main steps:

1. **Preprocessing:** The input documents are preprocessed to extract relevant information.
2. **Embedding:** The preprocessed documents are converted into embeddings, which are then stored in a **vector database**. In this project, we utilize **Chroma**, an open-source embedding database.
3. **RAG Pipeline:** A Retriever-Augmented-Generation (RAG) pipeline is created to generate answers to questions. For the answer generation step, we leverage Google's **gemini-pro** model as the generator.

## Prerequisites

- Hugging Face Token
- Gemini API Key

## Limitations

It has been observed that splitting documents into very small chunks can sometimes lead to the model generating incomplete or inaccurate answers. To potentially improve answer quality, consider increasing the `split_length` parameter when splitting documents. Additionally, introducing `split_overlap` when splitting documents might help the model retain context across splits, leading to more comprehensive answers.

## Future Enhancements:

- **Interactive Interface:** Develop a user-friendly interface for more convenient questioning and exploration of generated answers.
- **Performance Optimization:** Consider optimizations for better quality of answer generation.
