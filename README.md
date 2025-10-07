LangChain: Chat with SQL Database

This project is a Streamlit-based web app that lets you chat with your SQL database (either SQLite or MySQL) using natural language.
It uses LangChain, Groq LLMs (Llama3), and SQLDatabaseToolkit to convert your questions into SQL commands and display results instantly.

Features

Natural Language to SQL: Ask questions like "How many students are above 20?" and get results without writing SQL.

Multiple Database Support:

SQLite (student.db)

MySQL (via user credentials)

LLM-powered: Uses ChatGroq with Llama3-8b for fast and accurate query generation.

Interactive UI: Built with Streamlit
 for a seamless chat experience.

Agent-Based Query Execution: Uses LangChain’s SQLDatabaseToolkit and create_sql_agent to execute queries securely.

Project Structure
Chat-with-SQL/
│
├── app.py              # Main Streamlit app
├── requirements.txt    # Python dependencies
├── student.db          # SQLite database (sample)
└── README.md           # Project documentation

Installation
1. Clone the repository


2. Create and activate a virtual environment
conda create -n myenv python=3.8
conda activate myenv


or using venv:

python -m venv myenv
source myenv/bin/activate  # (Linux/Mac)
myenv\Scripts\activate     # (Windows)

3. Install dependencies
pip install -r requirements.txt

Environment Setup

You’ll need a Groq API key to use the LLM. Get one from https://groq.com
.

In the Streamlit sidebar, enter:

Groq API Key

MySQL credentials (if connecting to MySQL)

Run the App
streamlit run app.py


Once running, open the URL shown in the terminal (usually http://localhost:8501).

Usage

Choose the database:

SQLite: uses student.db provided in the project folder.

MySQL: enter host, username, password, and database name.

Enter your Groq API Key.

Start chatting! Example queries:

"How many students are there?"

"List the top 5 students by marks."

"What is the average age of students?"

Tech Stack
Component	Technology
Frontend	Streamlit
LLM	Groq (Llama3-8b)
Backend	LangChain, SQLAlchemy
Databases	SQLite, MySQL
