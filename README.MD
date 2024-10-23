---

# Data Crawling and Processing Pipeline

This repository contains a set of Jupyter notebooks for crawling product data, downloading images, and processing the data to convert it into vectors that can be used for machine learning models. The purpose of this pipeline is to collect and prepare product data for use in recommendation systems.

## Project Structure

- **crawl_data_by_id.ipynb**: Crawls product data based on product IDs.
- **crawl_id_product.ipynb**: Extracts product IDs for subsequent data crawling processes.
- **download_images.ipynb**: Downloads product images using URLs obtained from the crawled data.
- **image_to_vec.ipynb**: Converts product images into feature vectors using a pre-trained model (e.g., VGG16) for content-based filtering.
- **process_data_crawl.ipynb**: Cleans and processes the raw data collected from the crawling step, making it ready for machine learning tasks.
- **text_to_vec.ipynb**: Converts product descriptions or other text data into feature vectors using a text-based model (e.g., PhoBERT).

---

## Notebooks

### 1. **Crawling Data by Product ID**
   - **File**: `crawl_data_by_id.ipynb`
   - **Purpose**: This notebook crawls detailed product information based on product IDs. It uses a specified API to pull product details such as name, description, price, and other metadata.
   - **Usage**: After obtaining the product IDs, use this notebook to crawl the full product information for further analysis and processing.

### 2. **Crawling Product IDs**
   - **File**: `crawl_id_product.ipynb`
   - **Purpose**: This notebook is responsible for extracting product IDs from the e-commerce platform (e.g., Tiki). These IDs will be used in the `crawl_data_by_id.ipynb` notebook to pull detailed product data.
   - **Usage**: Run this notebook to generate a list of product IDs that can be used in subsequent crawling steps.

### 3. **Downloading Images by URL**
   - **File**: `download_images.ipynb`
   - **Purpose**: This notebook downloads product images from URLs that are extracted during the data crawling step. It fetches and saves the images locally for feature extraction.
   - **Usage**: Use this notebook after crawling data to obtain images associated with products.

### 4. **Processing Crawled Data**
   - **File**: `process_data_crawl.ipynb`
   - **Purpose**: This notebook handles cleaning and preprocessing the raw data obtained from the crawl. It normalizes data, handles missing values, and prepares the dataset for feature extraction and machine learning.
   - **Usage**: Run this notebook to clean the crawled data and prepare it for further processing.

### 5. **Converting Images to Vectors**
   - **File**: `image_to_vec.ipynb`
   - **Purpose**: Converts product images into feature vectors using a deep learning model like VGG16. These vectors will be used in the recommendation system for content-based filtering.
   - **Usage**: Use this notebook to transform product images into numerical representations (feature vectors) for similarity search and recommendation tasks.

### 6. **Converting Text to Vectors**
   - **File**: `text_to_vec.ipynb`
   - **Purpose**: This notebook converts text data such as product descriptions into feature vectors using a text-based model (e.g., PhoBERT). The vectors are used for text-based content filtering.
   - **Usage**: Run this notebook to convert product descriptions into numerical vectors for use in the recommendation system.

---
