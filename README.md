
# 🧠 AI Task Manager Assistant

## 📌 Problem Statement

In today’s fast-paced environment, individuals struggle to manage daily tasks effectively. Missed deadlines, forgotten activities, and decreased productivity are common due to the lack of an intuitive system that understands natural language and assists in task management seamlessly.

## ✅ Proposed Solution

An AI-powered desktop assistant that uses NLP and ML to:
- Understand user commands
- Classify task intents
- Manage, schedule, and remind users of tasks
- Provide voice feedback and GUI interaction

## 🧱 System Development Approach

### 📥 Data Collection & Preprocessing
- Collected 100–200 labeled user commands per intent (e.g., `add_task`, `delete_task`)
- Preprocessing: Lowercasing, stopword removal (via spaCy), datetime parsing (`dateparser`)

### 🤖 Machine Learning
- Model: TF-IDF + Logistic Regression pipeline
- Accuracy Goal: 85% on an 80/20 train-test split
- Persistence: Model saved using `joblib`

### 💻 Application Development
- Frontend: `Tkinter` GUI for command entry and task display
- Backend: 
  - NLP with `spaCy`
  - Date handling with `dateparser`
  - Reminders via background thread
  - Notifications using `plyer`
  - Voice feedback via `pyttsx3`
- Features:
  - Task metadata (time, priority, category, recurring)
  - Dual-mode output: GUI + voice
  - CLI version (optional)

## 🚀 Deployment
- Runs as a standalone Python desktop app (no server/cloud required)
- Optional data persistence using JSON or SQLite

## 🧪 Evaluation
- Manual testing
- Accuracy check for intent classification
- User feedback survey on ease of use and responsiveness

## ⚙️ System Architecture

- Modules:
  - User Input (GUI/CLI)
  - Intent Detection
  - Entity & Datetime Extraction
  - Task Processing
  - Reminders
- Output:
  - GUI updates
  - Voice feedback
  - Notifications

## 💻 System Requirements

- OS: Windows 10/11, macOS, or Linux
- Python: 3.8–3.11
- RAM: 4 GB+
- CPU: Intel i3 or better


## 📚 Libraries Used

- spaCy – For NLP tasks like tokenization and stop word removal
- dateparser – To parse natural language date/time expressions
- pyttsx3 – For offline text-to-speech voice output
- tkinter – For building the graphical user interface (GUI)
- plyer – To show desktop notifications across platforms
- threading – To run the reminder loop in the background without freezing the GUI
- scikit-learn – For the machine learning pipeline (TfidfVectorizer + LogisticRegression)
- joblib – To save and load the trained ML intent classifier

## 🔄 Algorithm Overview

- Input: Natural language command
- Processing:
  - Text → TF-IDF features
  - Predict intent (e.g., `add_task`)
  - Extract task details
- Output: GUI update, voice feedback, notification

## 🖼️ Result

- Accurately manages tasks via natural language
- Supports:
  - Task categorization
  - Prioritization
  - Recurring reminders
- Effective combination of NLP, ML, GUI, and TTS

## 🧾 Conclusion

This project showcases the power of Python and lightweight ML/NLP to create an intelligent, offline task assistant. It offers a practical, interactive solution to daily task management without relying on complex cloud infrastructure.

## 🔮 Future Scope

- Integrate voice input (speech-to-text)
- Cloud sync for multi-device access
- Mobile app versions (Android/iOS)
- Use advanced NLP models (e.g., BERT)
- Smart task suggestions
- Calendar integrations (Google/Outlook)
- Multi-user profile support
