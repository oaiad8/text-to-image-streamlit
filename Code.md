from diffusers import StableDiffusionPipeline
import torch
import streamlit as st

# Load the pipeline in float32
pipe = StableDiffusionPipeline.from_pretrained(
    "prompthero/openjourney",
    torch_dtype=torch.float32
)

# Force CPU
pipe = pipe.to("cpu")

def generate_image(prompt):
    image = pipe(prompt).images[0]
    return image

st.title("Text-to-Image Generator")

prompt = st.text_input("Enter your image description")

if st.button("Generate Image"):
    if prompt:
        st.image(generate_image(prompt), caption="Generated Image")
