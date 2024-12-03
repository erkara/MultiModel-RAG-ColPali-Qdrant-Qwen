# MultiModel-RAG-ColPali-Qdrant-Qwen

This repository has two notebooks that demonstrate a vision-based Retrieval-Augmented Generation (RAG) pipeline built with ColPali, Qdrant, and Qwen models. The project focuses on efficient image-based retrieval and generating insightful answers to user queries.

![Vision-based RAG Pipeline](assets/similarity_map.png)

## Components

### [ColPali](https://github.com/illuin-tech/colpali)
A state-of-the-art Vision Language Model (VLM) for document retrieval. By treating each PDF page as an image, ColPali skips the need for complicated OCR and layout detection pipelines. It generates multi-vector embeddings for each page and has shown significant improvements over traditional approaches in several benchmarks.

### [Qdrant](https://qdrant.tech/)
A fast and scalable vector database. Qdrant supports multi-vector embeddings, making it a great fit for ColPali since embeddings are created for each image patch. It’s an open-source solution, with a free-tier option, that handles large-scale similarity searches efficiently.

### [Qwen2-VL](https://huggingface.co/Qwen/Qwen2-VL-7B-Instruct)
You probably know this one, pretty famous Vision Language Model by Alibaba, integrated to generate detailed and contextually rich answers from the retrieved images.

---

## What’s Included

- **`colpali_intro`**: This notebook demonstrates how to set up a retrieval pipeline using ColPali without requiring a vector store. It also includes interpretability features to visualize query-image similarities.

- **`colpali_qdrant`**: Here, I’ve extended the pipeline by integrating Qdrant to handle large-scale retrieval. The use of multi-vector embeddings ensures precise and efficient matching for more extensive datasets.

---

It would be hard to pull this notebook together without great resources. Check [ColPali cookbooks](https://github.com/tonywu71/colpali-cookbooks), [Qdrant tutorial](https://youtu.be/_A90A-grwIc?si=i9m2u_u06t9yNwbS), and [Vespa blog](https://blog.vespa.ai/retrieval-with-vision-language-models-colpali/) for more cool stuff. I hope you enjoy!

