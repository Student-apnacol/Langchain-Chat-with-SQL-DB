# LangChain: Chat with SQL Database

This project is a Streamlit-based web application that allows you to chat with your SQL database (either SQLite or MySQL) using natural language.
It uses LangChain, Groq LLMs (Llama3), and SQLDatabaseToolkit to convert your natural language queries into SQL commands and display the results instantly.

---

## Features

* Natural Language to SQL: Ask questions like "How many students are above 20?" and get results without writing SQL.
* Multiple Database Support:

  * SQLite (`student.db`)
  * MySQL (via user credentials)
* LLM-powered: Uses `ChatGroq` with `Llama3-8b` for fast and accurate query generation.
* Interactive UI: Built with [Streamlit](https://streamlit.io/) for an easy-to-use interface.
* Agent-Based Query Execution: Uses LangChain’s `SQLDatabaseToolkit` and `create_sql_agent` to run queries securely.

---

## Project Structure

```
Chat-with-SQL/
│
├── app.py              # Main Streamlit application
├── requirements.txt    # Python dependencies
├── student.db          # Sample SQLite database
└── README.md           # Project documentation
```

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/chat-with-sql.git
cd chat-with-sql
```

### 2. Create and activate a virtual environment

Using Conda:

```bash
conda create -n myenv python=3.8
conda activate myenv
```

Or using venv:

```bash
python -m venv myenv
source myenv/bin/activate    # For Linux/Mac
myenv\Scripts\activate       # For Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Environment Setup

You will need a **Groq API key** to use the LLM. You can get one from [https://groq.com](https://groq.com).

In the Streamlit sidebar, enter:

* Groq API Key
* MySQL credentials (if connecting to MySQL)

---

## Run the App

```bash
streamlit run app.py
```

Once the server starts, open the URL shown in the terminal (usually `http://localhost:8501`).

---

## Usage

1. Choose the database:

   * SQLite: Uses the `student.db` provided in the project folder.
   * MySQL: Enter host, username, password, and database name.
2. Enter your Groq API Key.
3. Start chatting with your database using natural language queries.

Example queries:

* "How many students are there?"
* "List the top 5 students by marks."
* "What is the average age of students?"

---

## Tech Stack

| Component | Technology            |
| --------- | --------------------- |
| Frontend  | Streamlit             |
| LLM       | Groq (Llama3-8b)      |
| Backend   | LangChain, SQLAlchemy |
| Database  | SQLite, MySQL         |

---

## Future Improvements

* Add support for PostgreSQL and MSSQL
* Enable query visualization with charts and graphs
* Add authentication for secure access

---

## Contributing

Contributions are welcome.
Fork the repository, create a new branch, make your changes, and open a pull request.

---

## License

This project is licensed under the MIT License.


