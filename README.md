🤖 Gemini AI Chatbot with Persistent Chat History

A Python-based conversational AI chatbot powered by Google's Gemini API, featuring persistent conversation history, environment-based API key management, and an interactive command-line interface.

📌 Project Overview

The Gemini AI Chatbot is a command-line application developed in Python that allows users to interact with Google's Gemini generative AI model.

The chatbot accepts questions and messages through the terminal and displays AI-generated responses. Its main feature is persistent conversation history: messages are saved in a local JSON file and restored when the application starts again.

This project demonstrates practical skills in Python programming, AI API integration, JSON file handling, environment variables, and exception handling.

✨ Features

- 🤖 AI-Powered Conversations: Interact with the configured Google Gemini model.
- 💬 Interactive Terminal Interface: Enter multiple messages without restarting the program.
- 💾 Persistent Chat History: Save conversation history in "chat_history.json".
- 🔄 History Restoration: Load previously saved messages when the chatbot starts.
- 🔐 Environment-Based API Key: Read the Gemini API key from a ".env" file.
- 🛡️ Error Handling: Handle API errors and problems reading or saving chat history.
- 📂 Organized File Management: Keep configuration and history files beside the Python script.
- 📝 JSON Data Storage: Store conversation messages in a structured JSON format.
- 🚪 Simple Exit Command: Type "exit" to stop the chatbot.

🛠️ Technologies Used

- Python — Core programming language.
- Google Gen AI SDK — Connects the application to Google's Gemini API.
- Google Gemini API — Generates AI responses.
- python-dotenv — Loads environment variables from a ".env" file.
- JSON — Stores conversation history.
- Pathlib — Manages file paths.
- OS Module — Reads environment variables.
- Exception Handling — Manages API and file-related errors.

📁 Project Structure

Gemini-Chat-Board/
│
├── chartboard.py       # Main chatbot application
├── .env                # Gemini API key (keep private)
├── chat_history.json   # Saved conversation history
├── .gitignore          # Files excluded from Git
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation

Note: "chat_history.json" is created when the application successfully saves a conversation. The other supporting files should be created as needed.

⚙️ Installation and Setup

1. Install Python

Install a compatible version of Python on your computer.

Check your Python installation:

python --version

2. Clone the Repository

Clone this repository to your local computer:

git clone https://github.com/YOUR-USERNAME/Gemini-Chat-Board.git

Move into the project directory:

cd Gemini-Chat-Board

Replace "YOUR-USERNAME" with your GitHub username.

3. Install Dependencies

Install the required Python packages:

pip install google-genai python-dotenv

4. Configure the Gemini API Key

Create a file named ".env" in the same directory as "chartboard.py".

Add the following line:

GEMINI_API_KEY=your_gemini_api_key_here

Replace "your_gemini_api_key_here" with your own valid Gemini API key.

Obtain and manage your API key through Google AI Studio:

https://aistudio.google.com/

Security Note: Never publish your real API key or share it in screenshots, source code, or public repositories.

▶️ How to Run

Run the following command from the project directory:

python chartboard.py

When the application starts, it displays a welcome message and the number of previous messages loaded.

Example:

Gemini Chatbot Started!
Loaded 0 previous messages.
Type 'exit' to stop.

You: What is Python?
Gemini: Python is a high-level programming language...

You: exit
Chatbot stopped!

The AI response and loaded message count will vary depending on your conversation history and API configuration.

💾 How Persistent Chat History Works

The chatbot uses a JSON file named "chat_history.json" to preserve conversation history.

1. Startup: The application checks whether a history file exists.
2. Loading: If saved messages exist, they are loaded and converted into Gemini content objects.
3. Conversation: User messages are sent to the Gemini chat session.
4. Saving: After a successful response, the conversation history is written to a temporary file.
5. File Replacement: The temporary file replaces the previous history file.
6. Next Session: When the application starts again, the saved conversation is restored.

This allows the chatbot to maintain context between program sessions, provided the saved history remains available.

🔐 Security and Privacy

- Store the Gemini API key in the ".env" file.
- Add ".env" to ".gitignore" to prevent accidentally publishing credentials.
- Do not commit private API keys or sensitive conversation history.
- Remember that "chat_history.json" contains saved messages and may include personal information.

Recommended ".gitignore" file:

.env
chat_history.json
__pycache__/
*.py[cod]
.venv/
venv/

🧠 Learning Outcomes

This project demonstrates the practical application of:

- Python functions and modules.
- Third-party library integration.
- Generative AI and API communication.
- Environment variables and configuration management.
- JSON serialization and deserialization.
- File handling using "pathlib".
- Exception handling with "try" and "except".
- Persistent data storage.
- Interactive command-line application development.

🚀 Future Improvements

Possible enhancements include:

- Add a graphical user interface.
- Support multiple separate conversations.
- Add commands to clear or export chat history.
- Improve logging and diagnostic messages.
- Add configurable model selection.
- Add automated tests.
- Support additional input types if the selected model and SDK support them.

👨‍💻 Author

Hamid Ali

BSCS Student | Python Developer | AI & Machine Learning Enthusiast

GitHub: https://github.com/Hamid8200

LinkedIn: https://www.linkedin.com/in/hamid-ali-182ba2434

📄 License

This project is intended for educational and learning purposes. If you plan to distribute or reuse it, consider adding an appropriate open-source license.

⭐ Acknowledgment

Built with Python and Google's Gemini API to explore conversational AI, API integration, and persistent chat applications.

If you find this project useful, consider giving the repository a star!
