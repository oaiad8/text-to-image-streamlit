# 🎨 Text-to-Image Generator (Streamlit + Hugging Face Diffusers)

This is a simple **Streamlit app** that generates images from text prompts using the [OpenJourney](https://huggingface.co/prompthero/openjourney) model.

## 🚀 Features
- Enter any text prompt and generate an image.
- Runs with Hugging Face `diffusers` pipeline.
- CPU-only safe setup (works even without GPU).

## 🛠️ Installation

1. Clone this repo:
   ```bash
   git clone https://github.com/YOUR-USERNAME/text-to-image-streamlit.git
   cd text-to-image-streamlit
pip install -r requirements.txt
streamlit run image_generator.py
