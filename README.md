# LLM-Web-Researcher
LangGraph agents to research any topic on the web and generate wikipedia like articles. 


# Getting Started

## ⚙️ Installation

### Prerequisites
- Install **Python 3.11** or later. [Guide](https://www.python.org/downloads/).

### Steps

1. **Clone the Project**
   ```bash
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

