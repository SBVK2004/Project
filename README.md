# Text-to-Image Generator
This repository contains a Python script that leverages Hugging Face's Diffusers library to generate images from text prompts using the Stable Diffusion v1.5 model.

## *Features*

Image Generation: Create images directly from your text descriptions.
GPU Acceleration: Automatically uses CUDA (NVIDIA GPUs) for faster generation if available, otherwise falls back to CPU.
User Input: Simple command-line interface to enter your desired text prompt.
Safe Filenames: Automatically sanitizes prompts to create valid filenames for saved images.
Live Preview: Displays the generated image using Matplotlib after saving.

## *Installation*
Before running the script, you'll need to set up your Python environment.

Prerequisites
Python 3.8+
pip (Python package installer)
For GPU acceleration (recommended): An NVIDIA GPU and CUDA Toolkit installed.

## *Steps*
1. Clone the repository:
Bash

git clone https://github.com/your-username/your-text-to-image-repo.git
cd your-text-to-image-repo
(Replace your-username/your-text-to-image-repo with your actual GitHub details.)

2.Create a virtual environment (recommended):
Bash

python -m venv venv
source venv/bin/activate # On Windows: .\venv\Scripts\activate

3.Install dependencies:
Bash

pip install torch diffusers transformers accelerate matplotlib
pip install xformers # Optional: For faster Stable Diffusion performance on GPU

## *Configuration*
The script uses the runwayml/stable-diffusion-v1-5 model. Key parameters for image generation are set as follows:

negative_prompt: "low quality, blurry, ugly, deformed, distorted, bad anatomy, bad eyes, disfigured, poor quality, cartoon, anime, 3d render" (helps avoid undesirable artifacts).
num_inference_steps: 30 (a good balance between quality and generation speed).
guidance_scale: 7.5 (controls how strongly the image adheres to the prompt).
You can modify these values directly within the generate_image.py file to experiment with different outputs.

## *Requirements*
Hugging Face Diffusers library
RunwayML for the Stable Diffusion model


# Text-to-Video Generator
This repository features a Python script that leverages Hugging Face's Diffusers library to generate short videos from text prompts using the Damo-Vilab Text-to-Video model.

## *Features*
Video Generation: Create short videos directly from your text descriptions.
GPU Acceleration: Automatically uses CUDA (NVIDIA GPUs) for faster generation if available, otherwise falls back to CPU.
User Input: Simple command-line interface to enter your desired text prompt.
Safe Filenames: Automatically sanitizes prompts to create valid filenames for saved videos.

## *Installation*
Before running the script, you'll need to set up your Python environment.

Prerequisites
Python 3.8+
pip (Python package installer)
For GPU acceleration (recommended): An NVIDIA GPU and CUDA Toolkit installed.
## *Steps*
1.Clone the repository:
Bash

git clone https://github.com/your-username/your-text-to-video-repo.git
cd your-text-to-video-repo
(Replace your-username/your-text-to-video-repo with your actual GitHub details.)

2.Create a virtual environment (recommended):
Bash

python -m venv venv
source venv/bin/activate # On Windows: .\venv\Scripts\activate
3.Install dependencies:
Bash

pip install torch diffusers transformers accelerate
Important: The text-to-video model (damo-vilab/text-to-video-ms-1.7b) might be a gated model on Hugging Face. You might need to log in via the Hugging Face CLI before running the script to download the weights:
Bash
huggingface-cli login

## *Configuration*
The script uses the damo-vilab/text-to-video-ms-1.7b model. Key parameters for video generation are:

fps: Frames per second, set to 8.
n_seconds: Duration of the video in seconds, set to 4.
num_frames: Automatically calculated as fps * n_seconds.
You can modify fps and n_seconds directly within the generate_video.py file to control the video's speed and length.







