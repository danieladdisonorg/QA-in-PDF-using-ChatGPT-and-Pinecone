# QA in PDF using ChatGPT and Pinecone

A powerful Question-Answering application that enables users to query PDF documents using advanced AI technologies. This project combines OpenAI's ChatGPT for natural language processing with Pinecone's vector database for efficient document retrieval, creating an intelligent document search and Q&A system.

## 🚀 Features

- **PDF Document Processing**: Automatically loads and processes PDF files from a specified directory
- **Intelligent Text Chunking**: Splits documents into manageable chunks for optimal retrieval
- **Vector Embeddings**: Uses OpenAI embeddings to create semantic representations of document content
- **Semantic Search**: Leverages Pinecone vector database for fast and accurate document retrieval
- **Natural Language Q&A**: Powered by ChatGPT for human-like responses
- **Interactive Web Interface**: Built with Streamlit for easy user interaction
- **Caching Optimization**: Implements Streamlit caching for improved performance

## 🛠️ Technology Stack

- **LangChain**: Framework for building LLM applications
- **OpenAI GPT**: Large language model for generating responses
- **Pinecone**: Vector database for similarity search
- **Streamlit**: Web application framework
- **Python**: Core programming language

## 📋 Prerequisites

- Python 3.7+
- OpenAI API key
- Pinecone API key and environment

## 🔧 Installation

1. **Clone the repository**
```bash
git clone https://github.com/danieladdisonorg/QA-in-PDF-using-ChatGPT-and-Pinecone.git
cd QA-in-PDF-using-ChatGPT-and-Pinecone
```

2. **Install required dependencies**
```bash
pip install -r requirements.txt
```

3. **Set up environment variables**
   
   Create a `.env` file in the root directory and add your API keys:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   PINECONE_API_KEY=your_pinecone_api_key_here
   PINECONE_ENV=your_pinecone_environment_here
   ```

4. **Create data directory**
```bash
mkdir data
```

5. **Add your PDF files**
   
   Place your PDF documents in the `data/` directory.

## 🚀 Usage

1. **Start the application**
```bash
streamlit run app.py
```

2. **Access the web interface**
   
   Open your browser and navigate to `http://localhost:8501`

3. **Ask questions**
   
   Enter your questions in the text input field and click "Ask Query" to get AI-powered answers based on your PDF documents.

## 📁 Project Structure

```
QA-in-PDF-using-ChatGPT-and-Pinecone/
├── app.py                 # Main application file
├── data/                  # Directory for PDF files
├── .env                   # Environment variables (create this)
├── requirements.txt       # Python dependencies (create this)
└── README.md             # Project documentation
```

## ⚙️ Configuration

### Pinecone Setup
- Create a Pinecone account and get your API key
- Set up an index named `langchain-demo-indexes`
- Note your environment (e.g., `us-west1-gcp`)

### OpenAI Setup
- Create an OpenAI account and generate an API key
- Ensure you have sufficient credits for API usage

## 🔍 How It Works

1. **Document Loading**: The application scans the `data/` directory for PDF files
2. **Text Processing**: Documents are split into chunks of 1000 characters
3. **Embedding Generation**: OpenAI creates vector embeddings for each text chunk
4. **Vector Storage**: Embeddings are stored in Pinecone for fast retrieval
5. **Query Processing**: User questions are converted to embeddings and matched against stored vectors
6. **Answer Generation**: Relevant document chunks are retrieved and passed to ChatGPT for answer generation

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [LangChain](https://langchain.com/) for the excellent framework
- [OpenAI](https://openai.com/) for the powerful language models
- [Pinecone](https://pinecone.io/) for the vector database
- [Streamlit](https://streamlit.io/) for the web framework

## 📞 Support

If you encounter any issues or have questions, please open an issue on GitHub or contact the maintainer.

---

**Note**: Make sure to keep your API keys secure and never commit them to version control.
