# 📚 LLM-Powered Flashcard Generator

A lightweight yet robust flashcard generation tool that uses **Large Language Models (LLMs)** to convert educational content (e.g., textbook chapters, lecture notes) into effective **Question-Answer flashcards**.

Built with **Python**, powered by **Groq/OpenAI**, and deployed using **Streamlit** on **Render**.

---

## ✨ Features

- 🧠 Automatically generates flashcards from `.txt` or `.pdf` content
- 🤖 Supports Groq (e.g., Mixtral) or OpenAI (e.g., GPT-3.5-Turbo)
- 📄 Paste text or upload files directly
- ✅ Each flashcard includes:
  - Question (clear & concise)
  - Answer (factual & self-contained)
- 🧪 Assign difficulty levels
- 🌐 Export flashcards to `.csv` and `.json`
- 🖼️ Clean and simple UI with **Streamlit**

---
![image](https://github.com/user-attachments/assets/f331b51b-c000-4732-b250-8ee83fb092d4)


## 🚀 Getting Started

### 🔧 Installation (Locally)

```bash
git clone https://github.com/chaudharynaveen377/question_flashcard_generator.git
cd question_flashcard_generator

# Create virtual environment (optional)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
```



## 🧾 Requirements
Python-3.12.0

Your `requirements.txt` should include:

```txt
streamlit==1.23.1
pandas==1.5.3
numpy==1.23.5
scikit-learn==1.1.3
openai==0.28.0
groq==0.28.0
```
```txt
question_flashcard_generator/
├── app.py
├── requirements.txt
├── .runtime.txt
└── README.md
```
### 🌐 Translation Support
```text
The app supports automatic translation of the educational content before generating flashcards, allowing users to learn in their preferred language.
```
✅ How it works:
```text
In the sidebar, enable the "Translate content before generating questions" checkbox.

Select your target language from the dropdown (e.g., Hindi, Spanish, French, German, Japanese).

The original input is translated using an LLM (e.g., Mixtral via Groq).

Flashcards are then generated based on the translated version of your content.

🗣️ Supported Languages (currently):
Hindi

Spanish

French

German

Japanese

✨ This feature helps in multi-lingual learning environments, enabling students to study in their native language.
```
![image](https://github.com/user-attachments/assets/6ffe670b-d4b3-4123-bb98-b22fc8a63dca)

### 📋 Review Output Section
```text
After flashcards are generated, users can review the raw output in a structured format for validation or preview before exporting.
```

#### ✅ Key Features:
- Displays all generated flashcards in **plain text**
- Preserves formatting for both **MCQ** and **Short Answer** types
- Includes **explanations** if enabled
- Helps users **verify content** before download

#### 💡 Where It Appears:
- Shown as an expandable section titled **"📋 Review Output"**
- Located just below the flashcard generation area


## ☁️ Deployment Instructions

### 🚀 Deploy on **Render**

1. Push your project to a GitHub repository.
2. Go to [Render](https://render.com) and create a new **Web Service**.
3. Connect your GitHub repo and configure the settings:

   - **Build Command:**  
     ```bash
     pip install -r requirements.txt
     ```

   - **Start Command:**  
     ```bash
     streamlit run app.py
     ```

4. Save and deploy. Your app will be available at the Render-generated URL.

---

### 🌐 Deploy on **Streamlit Cloud**

1. Push your project to a GitHub repository.
2. Go to [Streamlit Cloud](https://streamlit.io/cloud) and sign in.
3. Click on **"New app"** and connect your GitHub repository.
4. Select the branch and the `app.py` file as the main entry point.
5. Click **Deploy**.

> 🔁 Streamlit will automatically handle environment setup based on your `requirements.txt`.

---

### ✅ Deployment Links

- 🌐 **Streamlit Cloud App:** [Live Demo on Streamlit](https://questionanswerflashcard-nq9plrcs2x8acwk5mleqqr.streamlit.app/)
- 🚀 **Render App:** [Live Demo on Render](https://question-flashcard-generator.onrender.com)

#### 🔍 Example Preview:

```text
Q: What is the Internet?
A) A computer
B) A global office
C) A global network of interconnected computers
D) A messaging app
Answer: C
Explanation: The Internet is a global network used to connect computers and share data.
```
---
![image](https://github.com/user-attachments/assets/ea60f917-2269-4473-8270-2ad9a116137f)

### 📤 Export Section
```text
Once flashcards are generated and reviewed, users can export them in multiple formats for study or integration with popular tools like **Anki** or **Quizlet**.
```

#### ✅ Supported Export Formats:

| Format         | Description                                               |
|----------------|-----------------------------------------------------------|
| `.csv`         | Tabular data of all flashcards (including MCQ options)    |
| `.json`        | Structured data for programmatic use or APIs              |
| Anki `.csv`    | Front/Back format for flashcard import into Anki decks    |
| Quizlet `.csv` | Front/Back format compatible with Quizlet import tools    |

#### 💡 How to Use:
- After generating flashcards, scroll to the **📤 Export Flashcards** section.
- Click to download your preferred format:
  - ⬇️ Download CSV  
  - ⬇️ Download JSON  
  - ⬇️ Download Anki CSV  
  - ⬇️ Download Quizlet CSV


![image](https://github.com/user-attachments/assets/28d2d59c-a40d-4e2e-9efb-08e5cd9a2d61)

### 🧾 Example
```text
The Internet is a global network of interconnected computers that communicate using standardized protocols. 
It allows users to access and share information across the world. The World Wide Web is a system that operates 
on the Internet and enables users to access web pages using browsers and URLs.
```

### output
```text
[
  {
    "question": What is the primary function of the Internet?,      
    "answer": " The primary function of the Internet is to allow users to access and share information across the world."
  },
  {
    "question": What is the role of URLs in accessing information on the Internet?
    "answer": "URLs (Uniform Resource Locators) enable users to access web pages on the Internet by providing a unique address for each webpage."
  },
  {
    "question": " What is the relationship between the Internet and the World Wide Web?",
    "answer": "The World Wide Web is a system that operates on the Internet, enabling users to access web pages using browsers and URLs."
  }
]
```
![image](https://github.com/user-attachments/assets/1d183d05-1679-46e6-bd11-f311e30bffe3)

![image](https://github.com/user-attachments/assets/f77a8fd1-18c0-4a52-879d-478fcc80ed16)

### 🎥 Demo Video

📽️ [Click here to watch the demo](https://drive.google.com/file/d/1UxJhg5cs07yvt6dmVxRHohQFh2Kac50g/view?usp=sharing)

