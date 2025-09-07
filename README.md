🚀 FastAPI Mistral Quantization & Ngrok Deployment

This project demonstrates how to quantize a Mistral model for efficient inference and serve it through a FastAPI backend. It also includes Ngrok integration to expose the API endpoint for external access during local development.

📂 Project Structure

quantization-fast-api-mistral.ipynb → Handles model quantization (reducing size & improving inference speed) and sets up a FastAPI server to serve the quantized model.

ngrok local.ipynb → Connects the FastAPI server to Ngrok, making the local API accessible via a public URL.

⚡ Features

Quantization of Mistral LLM for optimized performance.

FastAPI REST API for text generation.

Ngrok integration for quick testing & sharing.

Easy-to-run Jupyter notebooks for step-by-step execution.

🛠️ Installation

Make sure you have Python 3.9+ installed. Then install dependencies:

pip install fastapi uvicorn transformers accelerate torch ngrok


If using Jupyter, also install:

pip install jupyter notebook

▶️ Usage

Run quantization & API setup
Open and run all cells in quantization-fast-api-mistral.ipynb.
This will start a FastAPI server locally.

Expose API via Ngrok
Open ngrok local.ipynb and run all cells.
You’ll get a public Ngrok URL like:

https://xxxx-xx-xx-xxx.ngrok-free.app


Use this to send API requests externally.

Test API
Example request with curl:

curl -X POST "http://127.0.0.1:8000/generate" \
-H "Content-Type: application/json" \
-d '{"prompt": "Hello, world!"}'


Or via Ngrok:

curl -X POST "https://xxxx-xx-xx-xxx.ngrok-free.app/generate" \
-H "Content-Type: application/json" \
-d '{"prompt": "Write a poem about AI"}'

📌 Notes

Ngrok is intended for temporary testing; for production, consider deploying on a proper cloud platform.

Adjust quantization parameters in the notebook for different trade-offs between performance and accuracy.

📜 License

This project is for educational purposes. Feel free to adapt and extend it.
