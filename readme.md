# Conversational RAG with PDF Uploads and Chat History

This project is a Streamlit application that leverages LangChain and Groq API to enable a conversational retrieval-augmented generation (RAG) system. The application allows users to upload PDF documents and interact with them using a conversational interface that maintains chat history. The project integrates multiple components, including Chroma for vector storage, and Hugging Face embeddings, to provide an efficient document querying experience.

![Screenshot of the Interface](Screenshot%202024-08-29%20123524.png)

## Project Structure
```
project-directory/
 │ ├── app.py 
 ├── requirements.txt 
 ├── .env 
 ├── README.md 
 ├── LICENSE 
 ├── .gitignore 
 ├── temp.pdf 
 ├── generative ai.pdf 
 ├── attention.pdf 
 └── Screenshot_2024-08-29_123524.png
 ````


## Getting Started

### Prerequisites

Ensure you have the following installed:
- Python 3.8 or higher
- Pip (Python package installer)

### Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/conversational-rag-pdf.git
cd conversational-rag-pdf
``` 

2. Install the required Python packages:

```bash
pip install -r requirements.txt
```

3. Set up your environment variables in the `.env` file:

```bash
HF_TOKEN=your_huggingface_api_token
```

Replace the placeholder with your actual Hugging Face API token.

## Running the Application

1. Ensure your `.env`file is properly configured with your Hugging Face API token.

2. Run the Streamlit application:

```bash
streamlit run app.py
```
Open your web browser and go to http://localhost:8501 to interact with the application.

## Example Usage

1. Upload a PDF document using the file uploader.
2. Enter your Groq API key to initialize the conversational model.
3. Ask questions about the content of the uploaded PDF. The system will retrieve relevant sections from the document and provide concise answers.

## Integration Details
- `LangChain Components`: Used for creating the retrieval-augmented generation (RAG) pipeline. LangChain’s modular design allows easy handling of various input formats, including PDF documents.

- `Hugging Face Embeddings`: The Hugging Face model is used to generate embeddings for the text, enabling effective document retrieval.
Groq API: Utilized for the conversational AI component, facilitating intelligent, context-aware interactions based on the uploaded document.

## Files
- `app.py`: The main Python script that handles the Streamlit interface, LangChain components, PDF loading, and conversational RAG system.
- `requirements.txt`: Lists all the Python dependencies needed to run the application.
- `.env`: Contains the Hugging Face API token. This file should not be included in version control.
- `README.md`: This file, providing an overview of the project.
- `LICENSE`: The project's license, specifying how others may use the code.
- `.gitignore`: Specifies files and directories that should be ignored by Git, such as the .env file and any other sensitive information.
- `temp.pdf`: A temporary file used for PDF processing.
- `generative ai.pdf`: An example PDF file that can be uploaded for querying.
- `attention.pdf`: Another example PDF file available for document retrieval tasks.
- `Screenshot_2024-08-29_123524.png`: A screenshot of the interface, included for reference.

## License
This project is licensed under the MIT License - see the `LICENSE` file for details.

## .gitignore
The following files are ignored in the version control:
```bash
.env
__pycache__/
*.pyc
*.pyo
*.pyd
temp.pdf
```

## Contributing
Feel free to fork this repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## Acknowledgments
- Thanks to the developers of LangChain for providing powerful tools for building language model applications.
- Thanks to Hugging Face for their APIs and models that make advanced NLP tasks accessible.
- Thanks to Groq for the API that supports advanced conversational AI capabilities.
