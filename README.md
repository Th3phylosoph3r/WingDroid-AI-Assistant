WingDroid AI
Your intelligent copilot for everyday computing
WingDroid AI is a versatile desktop application that uses artificial intelligence to assist you with various computing tasks. It's designed to analyze and interpret content from different applications on your computer, providing insights and suggestions to enhance your productivity.
Features

Real-time analysis of active windows
OCR (Optical Character Recognition) for text extraction from images
Folder content analysis
Custom instructions for specific applications
Intelligent context-aware responses
Integration with Ollama for local LLM processing

Installation
Prerequisites

Python 3.7 or higher
Tesseract OCR engine
Ollama

Steps

Clone this repository:
Copygit clone https://github.com/yourusername/wingdroid-ai.git
cd wingdroid-ai

Install Tesseract OCR:

Windows: Download and install from Tesseract GitHub
macOS: brew install tesseract
Linux: sudo apt-get install tesseract-ocr


Add Tesseract to your system PATH.
Install Ollama by following the instructions on the official Ollama website.
Install required Python packages:
Copypip install -r requirements.txt

Run WingDroid AI:
Copypython wingdroid.py
Or on Windows, you can use the provided batch file:
Copywingdroid_run.bat


Ollama and Local LLM Integration
WingDroid AI leverages Ollama to run large language models (LLMs) locally on your machine. This ensures privacy, faster processing, and customization options.

After installing Ollama, pull the LLM model you want to use. For example:
Copyollama pull llama2

In the wingdroid.py file, locate the following line in the __init__ method of the ModernCmdAssistant class:
pythonCopyself.model_name = "llama3:8b"  # Adjust as needed
Replace "llama3:8b" with the name of the model you pulled, for example:
pythonCopyself.model_name = "llama2"


Benefits of using local LLMs with WingDroid AI:

Enhanced privacy: Your data doesn't leave your device.
Faster processing: No need to wait for remote API calls.
Customization: You can use different models based on your needs.

Choose a model that balances performance with your system's capabilities.
Usage

Launch WingDroid AI.
Select a window or use OCR to capture text.
Use the various analysis buttons to process the content.
Review the AI-generated insights and suggestions.

Disclaimer
WingDroid AI is a personal project created with the assistance of AI. It's intended for educational and experimental purposes. While efforts have been made to ensure its functionality, it may contain errors or limitations. The use of local LLMs through Ollama provides enhanced privacy, but users should still be mindful of the data they process.
Contributing
Contributions, ideas, and feedback are welcome! Feel free to open an issue or submit a pull request.
License
This project is licensed under the MIT License - see the LICENSE file for details.
