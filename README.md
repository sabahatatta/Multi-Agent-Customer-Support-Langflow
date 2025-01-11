# Multi-Agent-Customer-Support-Langflow

This project demonstrates a **multi-agent customer support system** built using Langflow (web-based), Astra DB, and OpenAI. It utilizes a RAG (Retrieval-Augmented Generation) approach for intelligent data retrieval and a user-friendly frontend powered by Streamlit. The system features three specialized agents—Manager Agent, Order Agent, and FAQ Agent—designed to provide efficient, contextual, and dynamic customer support.

---

## 🌟 Features

- **Langflow Web Integration**: The entire flow and agents are defined using Langflow's intuitive web-based interface.
- **Astra DB for Vectorization**: Embeds and vectorizes data for efficient retrieval using Astra DB.
- **RAG-Based Retrieval**: Retrieval-Augmented Generation enables contextual and accurate responses.
- **Multi-Agent System**:
  - **Manager Agent**: Coordinates interactions between the agents.
  - **Order Agent**: Handles order-related queries using interconnected orders and products data.
  - **FAQ Agent**: Provides answers to frequently asked questions using the uploaded FAQ PDF.
- **Streamlit Frontend**: Interactive and easy-to-use interface for customer queries and responses.

---

## 🛠️ Tech Stack

### Backend
- **Langflow (Web)**: For defining and managing the complete agent workflow.
- **Python**: Used to power the Streamlit frontend and manage API integrations.
- **Astra DB**: Enables data embedding and vectorization for retrieval.

### AI Integration
- **OpenAI**: Used as the primary LLM for generating intelligent responses.

### Frontend
- **Streamlit**: Provides an interactive web interface for customer interaction.

---

## 📂 Folder Structure

```
├── data/                       # Data resources for the project
│   ├── Company_FAQ.pdf         # FAQ document for the FAQ Agent
│   ├── sample_orders.csv       # Sample orders data for the Order Agent
│   ├── sample_products.csv     # Sample products data for cross-referencing
├── Langflow/                   # Langflow-related assets
│   ├── Customer Support.json   # JSON file exported from Langflow
├── prompts/                    # Prompts for individual agents
│   ├── FAQAgent.txt            # Prompt for the FAQ Agent
│   ├── ManagerAgent.txt        # Prompt for the Manager Agent
│   ├── OrderLookupAgent.txt    # Prompt for the Order Agent
├── .env                        # Environment variables
├── LICENSE                     # License for the project
├── main.py                     # Entry point for the Streamlit app
├── README.md                   # Project documentation
├── requirements.txt            # Python dependencies
```

---

## ⚙️ Application Workflow

### 1. Langflow Workflow Definition
- The entire multi-agent workflow is defined and managed in Langflow's **web-based interface**.
- Agents and flows are exported as JSON for integration with the Python-based backend.

### 2. Data Preparation
- **PDF Document**: FAQ data is provided via an uploaded PDF file.
- **CSV Files**: Sample orders and products data are provided in CSV format and interconnected for efficient lookups.

### 3. Multi-Agent System
- **FAQ Agent**: Handles queries related to FAQs using vectorized embeddings of the PDF.
- **Order Agent**: Processes order-related queries by cross-referencing orders and products data.
- **Manager Agent**: Directs queries to the appropriate agent and ensures smooth interaction.

### 4. Streamlit Frontend
- Users interact with the agents through a web-based frontend built using Streamlit.
- Queries are routed to the appropriate agent, and responses are dynamically generated using OpenAI.

---

## 🔧 Setup Instructions

### Prerequisites
- Python 3.9 or later
- OpenAI API key
- Astra DB account and API keys

### Steps

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/sabahatatta/Multi-Agent-Customer-Support-Langflow.git
   cd Multi-Agent-Customer-Support-Langflow
   ```

2. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Environment Variables**:
   Create a `.env` file with the following variables:

   ```
   OPENAI_API_KEY=your_openai_api_key
   ASTRA_DB_APPLICATION_TOKEN=your_astra_db_token
   ```

4. **Run the App**:

   ```bash
   streamlit run main.py
   ```

   Access the app at [http://localhost:8501](http://localhost:8501).

---

## 🚀 Future Enhancements

- Add conversational context for maintaining dialogue history.
- Expand the system to include additional agents for more functionalities.
- Integrate user authentication for secure access.
- Optimize response time by caching frequent queries.

---

## 🤝 Contributing

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`feature/your-feature-name`).
3. Commit your changes and push to the branch.
4. Open a pull request.

---

## 📜 License

This project is licensed under the MIT License.

---

Feel free to reach out for feedback or suggestions to make this project even better! 😊