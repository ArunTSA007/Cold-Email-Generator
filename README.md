# 📧 Cold Mail Generator

An AI-powered cold email generator that helps software service companies create personalized outreach emails based on a company's job openings.

The application takes a company's careers-page URL, extracts relevant job listings, analyzes the job requirements, retrieves relevant portfolio projects using **ChromaDB**, and generates a personalized cold email using **LangChain and Groq**.

---

## 🚀 Features

* 🔗 Accept a company's careers-page URL
* 🔍 Extract job listings and job descriptions
* 🧠 Analyze job requirements using an LLM
* 🔎 Retrieve relevant portfolio projects using semantic search
* 🗄️ Store and search portfolio data using **ChromaDB**
* ✉️ Generate personalized cold emails
* 🔗 Include relevant portfolio links in generated emails
* 🌐 Simple and interactive **Streamlit** interface

---

## 💡 Imagine a Scenario

* **Nike** needs a Principal Software Engineer and is spending time and resources on hiring, onboarding, and training.
* **Atliq** is a software development company that can provide a dedicated software development engineer to Nike.
* The Business Development Executive (**Mohan**) from Atliq wants to reach out to Nike through a personalized cold email.

Instead of manually researching the job requirements and finding relevant previous work, the Cold Mail Generator can automate this process.

![Cold Mail Generator](imgs/img.png)

---

## 🏗️ Architecture Diagram

The application combines web scraping, LLM processing, vector search, and personalized email generation.

![Architecture Diagram](imgs/architecture.png)

---

## 🔄 How It Works

```text
Company Careers Page
        │
        ▼
   Web Scraping
        │
        ▼
  Job Listings
        │
        ▼
 Job Description
        │
        ▼
   LLM Analysis
        │
        ▼
Job Requirements / Skills
        │
        ▼
     ChromaDB
        │
        ▼
Relevant Portfolio Projects
        │
        ▼
  LangChain + Groq
        │
        ▼
Personalized Cold Email
```

### Step 1 — Enter Company Careers Page

The user provides the URL of a company's careers page.

### Step 2 — Extract Job Information

The application extracts relevant job listings and job descriptions from the provided page.

### Step 3 — Analyze Job Requirements

The extracted job description is processed to identify relevant skills, technologies, and requirements.

### Step 4 — Search Portfolio

The identified requirements are used to search the portfolio stored in **ChromaDB**.

ChromaDB performs vector-based retrieval to identify portfolio projects that are relevant to the specific job requirements.

### Step 5 — Generate Cold Email

The job information and relevant portfolio projects are provided as context to the LLM.

**LangChain + Groq** are then used to generate a personalized cold email.

### Step 6 — Review the Email

The generated email can be reviewed and customized before being sent to the potential client.

---

## 🛠️ Tech Stack

| Technology          | Purpose                                                   |
| ------------------- | --------------------------------------------------------- |
| 🐍 **Python**       | Core application development                              |
| 🦜 **LangChain**    | LLM application workflow and orchestration                |
| ⚡ **Groq**          | Fast LLM inference                                        |
| 🗄️ **ChromaDB**    | Vector database and semantic search                       |
| 🎨 **Streamlit**    | Web application interface                                 |
| 🌐 **Web Scraping** | Extracting job information                                |
| 🧠 **Embeddings**   | Representing portfolio information for semantic retrieval |

---

## 📂 Project Structure

```text
Cold-Email-Generator/
│
├── app/
│   ├── main.py
│   ├── chains.py
│   ├── portfolio.py
│   └── ...
│
├── imgs/
│   ├── img.png
│   └── architecture.png
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

## ⚙️ Setup

### 1. Clone the Repository

```bash
git clone https://github.com/ArunTSA007/Cold-Email-Generator.git
cd Cold-Email-Generator
```

### 2. Create a Virtual Environment

#### Windows

```bash
python -m venv venv
```

Activate the virtual environment:

```bash
venv\Scripts\activate
```

#### macOS / Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure the Groq API Key

Create a `.env` file inside the `app/` directory:

```env
GROQ_API_KEY=your_groq_api_key
```

Get your API key from the [Groq Console](https://console.groq.com/keys).

> ⚠️ **Important:** Never commit your `.env` file or API keys to GitHub.

### 5. Run the Application

From the project root directory:

```bash
streamlit run app/main.py
```

The Streamlit application will open in your browser.

---

## 🖥️ Application Preview

### Cold Mail Generator

![Cold Mail Generator](imgs/img.png)

### Architecture

![Architecture Diagram](imgs/architecture.png)

---

## 🧠 Key Concepts

This project provides hands-on experience with several Generative AI and LLM concepts:

* Large Language Models (LLMs)
* Generative AI
* LangChain
* Groq API
* ChromaDB
* Vector Databases
* Embeddings
* Semantic Search
* Information Retrieval
* Prompt Engineering
* Web Scraping
* Streamlit
* AI-powered application development

---

## 🎯 Project Goals

The main goal of this project is to demonstrate how **LLMs and vector databases can be combined with traditional web scraping to build a practical AI application**.

Instead of generating a generic email, the application retrieves relevant portfolio information based on the actual job requirements and uses that information to create a more personalized outreach email.

---

## 🔮 Future Improvements

* [ ] Support multiple job portals
* [ ] Improve job-description extraction
* [ ] Add multiple cold email templates
* [ ] Add different email tones
* [ ] Allow users to edit generated emails
* [ ] Add email export functionality
* [ ] Improve portfolio retrieval
* [ ] Add email quality evaluation
* [ ] Deploy the application for public use

---

## 👨‍💻 Author

**Arun Soundhara Pandian T**

GitHub:
https://github.com/ArunTSA007

---

## 📜 Attribution

This project is based on the **Cold Mail Generator** project by Codebasics and has been modified and extended for learning and development purposes.

Please refer to the original project's license and attribution requirements before redistributing or using the project commercially.

---

⭐ **If you find this project useful, consider giving the repository a star!**
