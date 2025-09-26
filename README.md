# Prompt Compression and Query Optimization

*A course by **DeepLearning.AI** in collaboration with **MongoDB***

## About This Course

This course explores how to integrate **traditional database features** with **vector search** to optimize the **efficiency, security, and cost** of large-scale **Retrieval-Augmented Generation (RAG)** applications.

You’ll gain practical skills in building intelligent retrieval pipelines that reduce query costs, improve response times, and increase relevance for end users.

---

## Course Topics & Explanations

### 1. Vanilla Vector Search

Vector search lies at the core of modern RAG systems. Instead of relying on keyword matches, documents and queries are converted into **dense embeddings** (numerical vectors). These vectors capture semantic meaning, enabling the system to find results based on **conceptual similarity** rather than exact word overlap.

In this course, you’ll:

* Learn how **cosine similarity** or **Euclidean distance** is used to measure closeness between embeddings.
* Implement a basic **vector index** in MongoDB for efficient retrieval.
* Understand the trade-offs between brute-force similarity search and optimized indexes.

---

### 2. Filtering with Metadata

Not all semantically relevant results are equally useful. For example, if you’re searching a product catalog, you might only want results available in your region or within a certain price range.

Filtering ensures results match both the **semantic meaning** and **practical conditions**:

* **Prefiltering** – Applied **before** the vector search using metadata stored in indexes (e.g., filtering by document type, category, or date). This reduces the search space and speeds up queries.
* **Postfiltering** – Applied **after** the vector search to refine retrieved results further. Useful when filtering conditions depend on computed fields or non-indexed attributes.

You’ll learn how to combine semantic search with **structured database queries**, ensuring retrieval is not just relevant, but also **context-aware**.

---

### 3. Projection

Projection is the process of **selecting only the fields you need** from query results instead of retrieving entire documents.

Why it matters:

* Reduces **bandwidth and latency** by minimizing response size.
* Improves **memory usage** when handling large datasets.
* Increases **security** by hiding sensitive fields that don’t need to be exposed.

For example, instead of retrieving an entire user profile, you may only need the user’s name and email for a query response. This practice keeps pipelines lean and efficient.

---

### 4. Boosting & Reranking

After performing a vector search, you may still want to **adjust the order of results** to prioritize what’s most useful.

* **Boosting** assigns higher importance to certain fields (e.g., favoring recent content, verified sources, or premium products).
* **Reranking** reorders results based on additional signals, such as popularity, click-through rate, or metadata values.

This ensures that the **most valuable documents rise to the top**, even if several results are equally semantically relevant. You’ll learn how to apply reranking strategies using MongoDB’s aggregation framework to fine-tune retrieval.

---

### 5. Prompt Compression

Large prompts are expensive — every token sent to an LLM consumes resources and impacts latency.

**Prompt Compression** is about making inputs shorter while retaining the necessary context. Techniques include:

* Summarizing retrieved documents before including them in prompts.
* Extracting only the most relevant sentences or fields.
* Using projection to reduce unnecessary data before it reaches the LLM.

By applying prompt compression, you can:

* Reduce **inference costs** for LLMs.
* Improve **response speed**.
* Scale your application to handle larger workloads without exponential cost growth.

---

## Hands-On Skills You’ll Gain

* Implement vector search for **RAG pipelines** using MongoDB.
* Build **multi-stage aggregation pipelines** to filter, project, and rerank efficiently.
* Use **metadata** to refine and restrict search results.
* Apply **projection** for performance and security optimization.
* **Rerank and boost** documents to maximize retrieval relevance.
* Implement **prompt compression** to cut down costs in LLM-powered systems.

---

## Why This Course Matters

Modern AI applications face challenges of **cost, latency, and scalability**. This course equips you to:

* Optimize RAG pipelines for **faster, cheaper queries**.
* Improve **retrieval accuracy and relevance**.
* Secure data by controlling query outputs.
* Build **production-ready AI systems** that scale efficiently.

---

## Acknowledgment

This course is proudly offered by:

* **[DeepLearning.AI](https://www.deeplearning.ai/)** – advancing world-class AI education.
* **[MongoDB](https://www.mongodb.com/)** – the developer data platform powering modern applications.

Special thanks to the instructors and engineers who combined expertise in **LLMs** and **databases** to create this impactful learning experience.
