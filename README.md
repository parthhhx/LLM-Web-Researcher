# Getting Started

## ⚙️ Installation

### Prerequisites
- Install **Python 3.11** or later. [Guide](https://www.python.org/downloads/).

### Steps

1. **Clone the Project**
   ```bash
   git clone https://github.com/parthhhx/LLM-Web-Researcher.git
   cd gpt-researcher
   ```

2. **Set Up API Keys**
   Export your API keys by running the following commands:
   ```bash
   export OPENAI_API_KEY={Your OpenAI API Key here}
   export TAVILY_API_KEY={Your Tavily API Key here}
   ```
   Alternatively, store them in a `.env` file for convenience.

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Start the Server**
   ```bash
   python -m uvicorn main:app --reload
   ```

5. **Access the Application**
   Open your browser and visit [http://localhost:8000](http://localhost:8000) to start using the application.

### Other Setups
For alternative setups (e.g., using Poetry or virtual environments), refer to the [Getting Started page](#).

---

## 📄 Research on Local Documents

You can instruct the Researcher to run research tasks based on your local documents. Currently supported file formats are: **PDF, plain text, CSV, Excel, Markdown, PowerPoint, and Word documents**.

### Steps

1. **Add the `DOC_PATH` Environment Variable**
   Point the `DOC_PATH` variable to the folder containing your documents:
   ```bash
   export DOC_PATH="./my-docs"
   ```

2. **Run GPT Researcher**
   - **If Running the Frontend App**: 
     Navigate to [http://localhost:8000](http://localhost:8000) and select **"My Documents"** from the **"Report Source"** dropdown options.
   
   - **If Using the PIP Package**:
     Pass the `report_source` argument as `"local"` when instantiating the `GPTResearcher` class. Example code snippet:
     ```python
     from gpt_researcher import GPTResearcher
     
     researcher = GPTResearcher(report_source="local")
     researcher.run_research()
     ```

