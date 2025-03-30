# 🛍️ ShopTheLook

**ShopTheLook** is an AI-powered fashion assistant that transforms your mood, vibe, or occasion into stylish outfit images—and helps you shop the look instantly. Powered by Google's Gemini multimodal API, Stable Diffusion, and real-time product search via SerpAPI, this project delivers a seamless "mood-to-outfit-to-shopping-cart" experience.

## ✨ Features

- 🎯 **Prompt Refinement**: Gemini refines vague user input (e.g., "cosmic streetwear") into detailed prompts for image generation.
- 🎨 **Outfit Generation**: Uses Stable Diffusion to generate high-quality, on-theme fashion visuals.
- 👁️ **Multimodal Image Analysis**: Gemini vision analyzes images and produces SEO-friendly shopping phrases.
- 🛍️ **Real-Time Shopping Integration**: Uses SerpAPI to fetch Google Shopping results for analyzed outfits.
- 🧠 **Vector Caching**: Pinecone stores prompt-image-search triplets for faster repeat queries.
- ☁️ **Cloud-Based Storage**: Google Cloud Storage hosts generated images and makes them instantly shareable.

## 🔧 Tech Stack

- **Gemini API (Text + Vision)** – Prompt refinement and image description
- **Stable Diffusion (HuggingFace)** – Fashion image generation
- **SerpAPI** – Real-time product search
- **OpenAI Embeddings + Pinecone** – Smart caching for performance
- **Google Cloud Storage** – Hosting generated images
- **LangChain** – Workflow orchestration
- **Python, Google Colab** – Development environment

## 🚀 How It Works

1. User enters a mood, occasion, or style prompt.
2. Gemini refines the input into a more detailed fashion concept.
3. Stable Diffusion generates outfit images based on the refined prompt.
4. Gemini vision analyzes images to generate search-optimized fashion phrases.
5. SerpAPI fetches real-world shopping results based on those phrases.
6. The output includes generated images and links to purchase similar styles.

## 📸 Sample Output

**Input Prompt**: `"Saturn vibes"`  
**Gender**: `Male`  
**Age**: `24`  

**Generated Images**:  
- Hosted on Google Cloud Storage

**Gemini Analysis**:  
- `"lace midi fit and flare wedding dress"`  
- `"lace midi dress puff sleeves"`

**Shopping Results**:  
- Grace Loves Lace Jones Crepe Dress – [$2,900](https://www.google.com/shopping/product/3662215624119381499)
- Lulus Lace Puff Sleeve Dress – [$69.00](https://www.google.com/shopping/product/13058217797976100699)

## 🛠️ Installation & Setup

> Project is currently built in Google Colab with access to external APIs.

1. Clone or open the notebook in Google Colab.
2. Install the required libraries:
```bash
pip install pillow torch diffusers google-cloud-storage langchain \
pinecone-client google-generativeai serpapi tiktoken
