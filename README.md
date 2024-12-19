# Langchain Server and Client

This project demonstrates a simple integration of LangChain with FastAPI and Streamlit. It provides API routes to generate essays and poems using OpenAI's ChatGPT and Ollama's Llama2 models, and a Streamlit frontend for user interaction.

## Features

- **Essay Generator:** Generates a 100-word essay on a given topic using OpenAI's ChatGPT.
- **Poem Generator:** Generates a 100-word poem suitable for a 5-year-old on a given topic using Ollama's Llama2.
- **API Endpoints:** Accessible endpoints for essay and poem generation.
- **Streamlit UI:** A user-friendly interface for interacting with the API.

---

## Installation

### Prerequisites

- Python 3.8+
- FastAPI
- Streamlit
- LangChain
- Uvicorn
- Requests
- dotenv
- Other dependencies listed in `requirements.txt`

### Steps

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables:
   - Create a `.env` file in the root directory.
   - Add your OpenAI API key to the file:
     ```env
     OPENAI_API_KEY=your_openai_api_key_here
     ```

5. Run the server:
   ```bash
   python app.py
   ```

6. Run the Streamlit client:
   ```bash
   streamlit run client.py
   ```

---

## API Documentation

The FastAPI server exposes the following endpoints:

### Essay Endpoint
- **URL:** `/essay`
- **Method:** POST
- **Request Body:**
  ```json
  {
    "input": {"topic": "<your-topic>"}
  }
  ```
- **Response:**
  ```json
  {
    "output": {"content": "<generated-essay>"}
  }
  ```

### Poem Endpoint
- **URL:** `/poem`
- **Method:** POST
- **Request Body:**
  ```json
  {
    "input": {"topic": "<your-topic>"}
  }
  ```
- **Response:**
  ```json
  {
    "output": "<generated-poem>"
  }
  ```

---

## Usage

1. **Run the Server:**
   Ensure the FastAPI server is running on `localhost:8082`.

2. **Interact via Streamlit:**
   Open the Streamlit app in your browser at the URL shown in the terminal (usually `http://localhost:8501`).

3. **Generate Content:**
   - Enter a topic in the "Write an essay on" field for essays.
   - Enter a topic in the "Write a poem on" field for poems.

---

## File Structure

- `app.py`: FastAPI server implementation.
- `client.py`: Streamlit UI for interacting with the API.

---

## Notes

- Ensure that the OpenAI API key is valid and active.
- Customize prompt templates in `app.py` as needed.
- Adjust the host and port in `app.py` or `client.py` if necessary.

---

## Contributors

- [Rakesh Shetty](https://github.com/glitchrakesh)

