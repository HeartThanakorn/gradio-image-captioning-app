# Image Captioning App with Gradio and Hugging Face

This project is a web application that automatically generates descriptive captions for any uploaded image. It utilizes the powerful **BLIP (Bootstrapping Language-Image Pre-training)** model from Hugging Face's Transformers library and provides a simple, interactive user interface built with **Gradio**.

This application is based on the "Implement image captioning app with Gradio" exercise.

## ✨ Features

-   **Upload & Caption**: Easily upload an image and receive an AI-generated caption.
-   **User-Friendly Interface**: A clean and intuitive web interface powered by Gradio.
-   **State-of-the-Art Model**: Leverages the pre-trained BLIP model for high-quality image descriptions.
-   **Easy to Set Up**: A straightforward setup process with minimal dependencies.

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

Make sure you have Python 3 installed on your system. You will also need `pip` to install the required libraries.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/gradio-image-captioning-app.git](https://github.com/YOUR_USERNAME/gradio-image-captioning-app.git)
    cd gradio-image-captioning-app
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate

    # For Windows
    python -m venv venv
    .\venv\Scripts\activate
    ```

3.  **Install the required libraries:**
    [cite_start]Based on the project's requirements, install Gradio, Transformers, and Pillow[cite: 187].
    ```bash
    pip install gradio transformers Pillow torch
    ```

### Running the Application

1.  Place your Python script (e.g., `image_captioning_app.py`) in the root directory.

2.  [cite_start]Run the application from your terminal[cite: 222]:
    ```bash
    python3 image_captioning_app.py
    ```

3.  [cite_start]Open your web browser and navigate to the URL provided in the terminal (usually `http://127.0.0.1:7860`) to start using the app[cite: 237].

## 🛠️ How It Works

The application follows these steps:

1.  [cite_start]**Load the Pre-trained Model**: It loads the `BlipForConditionalGeneration` model and its corresponding `AutoProcessor` from the Hugging Face library[cite: 193, 195].
2.  [cite_start]**Define the Captioning Function**: A function `caption_image` takes an uploaded image, converts it to the correct format (RGB), and processes it[cite: 199, 201].
3.  [cite_start]**Generate Caption**: The processed image is passed to the BLIP model, which generates a sequence of tokens representing the caption[cite: 203].
4.  [cite_start]**Decode Output**: The tokens are decoded into a human-readable text string[cite: 204].
5.  [cite_start]**Create Gradio Interface**: A `gradio.Interface` is created to wrap the `caption_image` function, providing an "Image" upload component for input and a "Text" box for the output caption [cite: 208, 211-214].
6.  [cite_start]**Launch the App**: The `launch()` method starts a local web server to host the interactive interface[cite: 218].

Enjoy generating captions for your images!
