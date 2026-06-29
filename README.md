# AI-Powered-Fashion-Product-Intelligence-System

An AI-powered fashion product intelligence system that uses **BLIP, CLIP, and FAISS** to understand products from images, generate embeddings, perform similarity search, recommend complementary products, detect duplicate products, and enable natural language product search.(smart product recommendations, duplicate product detection, and reverse product search)

## Project Overview

Modern e-commerce platforms contain thousands of products, making it difficult for customers to discover relevant items and for businesses to maintain a clean catalog. This project extends a multimodal product intelligence pipeline by combining image understanding, vector embeddings, and similarity search to solve common e-commerce challenges.

The system is built on top of:

* **BLIP** for product image understanding and caption generation
* **CLIP** for generating multimodal image and text embeddings
* **FAISS** for efficient vector similarity search

Using a single CLIP embedding pipeline, the system supports multiple downstream applications including recommendations, catalog cleaning, and reverse product search.

---

## Objectives

The project implements the following advanced product intelligence tasks:

### Task 1: Smart Product Recommendation Engine

Traditional recommendation systems often suggest visually similar products. This project recommends **complementary products** that can complete an outfit.

**Example**

Input Product:

* Running Shoes

Recommended Products:

* Sports Socks
* Fitness Watch
* Water Bottle

**Features**

* CLIP-based visual similarity
* Outfit Affinity Score
* Complementary product recommendations
* Recommendation visualization

---

### Task 2: Unique Product Catalog Creation

Large marketplaces frequently contain duplicate or near-duplicate products uploaded by different sellers. This task automatically identifies and groups similar products.

**Example**

Input:

* Blue Shirt A
* Blue Shirt B
* Blue Shirt C
* Running Shoe A
* Running Shoe B

Output:

* Blue Shirt
* Running Shoe

**Features**

* Duplicate product detection
* Agglomerative clustering
* Similar product grouping
* Unique catalog generation

---

### Task 3: Reverse Product Search

Allows users to search products using natural language descriptions instead of images.

**Example Query**

"blue casual shirt"

Output:

1. Men's Blue Casual Shirt
2. Blue Checked Shirt
3. Slim Fit Blue Shirt

**Features**

* Text-to-product retrieval
* CLIP text embeddings
* Semantic search
* Synonym expansion

---

## Dataset

**Dataset Used:** Fashion Product Images (Small)

The dataset contains:

* Product Images
* Product Names
* Category Information
* Subcategory Information
* Gender Information
* Color Information

For experimentation and evaluation, 700 products were processed using the CLIP embedding pipeline.

---

## System Architecture

Product Images
↓
BLIP Caption Generation
↓
CLIP Embedding Generation
↓
FAISS Vector Index
↓
Advanced Features
├── Smart Product Recommendation Engine
├── Unique Product Catalog Creation
└── Reverse Product Search

---

## Technologies Used

| Technology    | Purpose                                  |
| ------------- | ---------------------------------------- |
| Python        | Core Development                         |
| BLIP          | Image Understanding & Caption Generation |
| CLIP ViT-B/32 | Image and Text Embeddings                |
| FAISS         | Vector Similarity Search                 |
| Scikit-Learn  | Clustering & Evaluation                  |
| NumPy         | Numerical Computation                    |
| Pandas        | Data Processing                          |
| Matplotlib    | Visualizations                           |
| Kaggle        | Development Environment                  |

---

## Implementation Details

### BLIP Caption Generation

BLIP is used to generate descriptive captions from product images. These captions help the system understand product content and serve as the foundation for further analysis.

### CLIP Embeddings

CLIP converts both images and text into a shared embedding space. This enables:

* Image-to-image similarity search
* Text-to-image retrieval
* Recommendation generation
* Duplicate detection

### FAISS Indexing

FAISS is used to store and search embeddings efficiently, allowing fast retrieval of similar products even in larger catalogs.

---

## Results

### Embedding Generation

* Products Processed: 700
* Embedding Dimension: 512
* Model: CLIP ViT-B/32

### Task 1 Results

Successfully generated complementary product recommendations using visual similarity and category compatibility.

### Task 2 Results

Successfully grouped similar products and identified duplicate entries using clustering techniques.

### Task 3 Results

Successfully retrieved relevant products from natural language queries using CLIP text-image matching.

---

## Business Impact

This system provides practical value for e-commerce platforms:

* Automated product understanding
* Improved recommendation quality
* Better product discovery
* Duplicate catalog detection
* Reduced manual effort
* Enhanced customer experience

---

## Future Enhancements

* Personalized recommendations using user purchase history
* Voice-based product search
* Multi-image search support
* Real-time catalog updates
* LLM-enhanced product descriptions
* Price-aware recommendation ranking

---

## Repository Structure

```text
AI-Powered-Fashion-Product-Intelligence-System/
│
├── Fashion_Product_Intelligence.ipynb
├── README.md
└── report.pdf
        └──screenshots/
            ├── recommendation_results.png
            ├── duplicate_detection.png
            └── reverse_search.png
```

## Author

**A N Prajwal**


## References

* OpenAI CLIP
* BLIP Image Captioning
* FAISS Similarity Search
* Hugging Face Transformers
* Fashion Product Images Dataset
