# 🌟 Enhanced Event Document Parser Pro

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io)
![Version](https://img.shields.io/badge/version-2.0.0-green)
![Python](https://img.shields.io/badge/python-3.8+-blue)
![License](https://img.shields.io/badge/license-MIT-blue)

A powerful, AI-driven document parser specifically designed for event, hotel, and meeting documents. Built with Streamlit and powered by Groq's LLM API.

## 🎯 Live Demo

[View Live App on Streamlit Cloud](#) *(Link will be added after deployment)*

## ✨ Key Features

- **🤖 AI-Powered Extraction**: Leverages Groq's Llama 3.3 70B model for intelligent document parsing
- **🔒 Secure API Management**: Encrypted storage of API keys using system keyring
- **⚡ Performance Optimization**: Document caching and batch processing capabilities
- **📊 Advanced Analytics**: Cost breakdowns, occupancy analysis, and optimization recommendations
- **🔍 Document Comparison**: Side-by-side comparison of multiple event documents
- **✏️ Edit Mode**: Correct extraction errors with real-time recalculation
- **📈 Confidence Scoring**: Visual indicators for extraction accuracy
- **🎯 Template Learning**: Improves accuracy by learning from corrections
- **📥 Multiple Export Formats**: Excel (formatted), JSON (multiple formats), and integration-ready exports
- **⌨️ Keyboard Shortcuts**: Productivity shortcuts for power users

## 🚀 Quick Start

### Option 1: Use the Hosted Version
Visit [our Streamlit app](#) to use the parser without any installation.

### Option 2: Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/pkumv1/event-document-parser.git
   cd event-document-parser
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up your Groq API key**
   ```bash
   cp .env.template .env
   # Edit .env and add your API key
   ```

4. **Run the application**
   ```bash
   streamlit run main.py
   ```

## 📖 Usage Guide

### Single Document Processing

1. **Upload**: Drag and drop or click to upload a PDF/DOCX file
2. **Preview**: Review the document in the preview pane
3. **Analyze**: Click "Analyze Document" to start extraction
4. **Review**: Check extracted data across different tabs
5. **Edit**: Toggle edit mode to make corrections
6. **Export**: Download results as Excel or JSON

### Batch Processing

Process multiple documents simultaneously:
- Select "Batch Processing" mode from the sidebar
- Upload multiple documents
- Download all results as a ZIP file

### Document Comparison

Compare two event documents:
- Select "Document Comparison" mode
- Upload two documents
- Review side-by-side differences

## 🔧 Configuration

### API Key Setup

1. Get your API key from [Groq Console](https://console.groq.com)
2. Add it to your `.env` file or enter it in the app interface
3. The app will securely store it for future use

### Supported Document Types

- **PDF**: Text-based PDFs (not scanned images)
- **DOCX**: Microsoft Word documents
- **Content**: Event contracts, BEOs, proposals, invoices

## 📊 Understanding Confidence Scores

- ✅ **High (>80%)**: Reliable extraction
- ⚡ **Medium (60-80%)**: Review recommended
- ⚠️ **Low (<60%)**: Manual verification needed

## 🛠️ Project Structure

```
event-document-parser/
├── main.py                    # Main Streamlit application
├── requirements.txt           # Python dependencies
├── .env.template             # Environment variables template
├── LICENSE                   # MIT License
├── README.md                 # This file
├── .streamlit/              # Streamlit configuration
│   └── config.toml
├── core/                     # Core functionality
│   ├── parser.py            # Enhanced JSON parser
│   ├── extractor.py         # Document text extraction
│   └── validator.py         # Data validation
├── models/                   # Data models
│   ├── event.py             # Event data structures
│   └── financial.py         # Financial data structures
├── ui/                      # User interface
│   ├── components.py        # Reusable UI components
│   └── styles.py           # Custom CSS and theming
├── utils/                   # Utilities
│   ├── calculations.py      # Financial calculations
│   ├── formatters.py        # Data formatting
│   ├── security.py          # API key management
│   └── cache.py            # Document caching
├── prompts/                 # LLM prompts
│   └── extraction.py        # Prompt generation
└── exporters/               # Export functionality
    ├── excel.py             # Excel export
    └── json.py              # JSON export
```

## ⚠️ Important Setup Note

This repository is currently being set up. To complete the setup:

1. **Add Module Files**: Copy all the module code from the provided documentation into the respective `.py` files in each directory
2. **Update main.py**: Replace the placeholder main.py with the complete application code
3. **Configure Streamlit Secrets**: When deploying to Streamlit Cloud, add your GROQ_API_KEY in the secrets management

## 🔐 Security

- API keys are encrypted using system keyring
- No sensitive data is stored in plain text
- All processing happens locally
- Document cache can be cleared anytime

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For issues or questions:
- Check the [Issues](https://github.com/pkumv1/event-document-parser/issues) page
- Create a new issue with:
  - Error description
  - Steps to reproduce
  - Sample document (if possible)

## 🙏 Acknowledgments

- Built with [Streamlit](https://streamlit.io/)
- Powered by [Groq](https://groq.com/)
- UI design inspired by Groupize branding

---

Made with ❤️ for the events industry