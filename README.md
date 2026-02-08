# 🤖 Customer Support Agent using Multi-Agent Handoffs (LangChain)

This project demonstrates how to build an **AI-powered Customer Support Agent** using **LangChain’s multi-agent handoff pattern**.  
The system intelligently routes customer queries between specialized agents (Billing, Technical Support, General Support) to provide accurate and contextual responses.

The implementation follows LangChain’s official handoff architecture:
https://docs.langchain.com/oss/python/langchain/multi-agent/handoffs-customer-support

<img width="711" height="721" alt="image" src="https://github.com/user-attachments/assets/9c857299-cbb8-4e30-b3db-88b8d5ee3794" />

---

## 🧠 Key Concept: Agent Handoffs

Instead of using a single monolithic agent, this system:
- Starts with a **Primary (Router) Agent**
- Analyzes the user query
- **Hands off** the conversation to a specialized agent best suited to answer it

This mirrors **real-world customer support workflows**, where queries move between teams.

---

## 🏗️ Architecture Overview

User Query
│
▼
Primary Support Agent (Router)
│
├──► Billing Agent
│
├──► Technical Support Agent
│
└──► General Support Agent


Each agent:
- Has its **own system prompt**
- Focuses on a **specific domain**
- Can seamlessly take over the conversation

---

## 🚀 Features

- ✅ Multi-agent orchestration using LangChain
- ✅ Dynamic agent handoff based on intent
- ✅ Clear separation of responsibilities
- ✅ Realistic customer support simulation
- ✅ Extensible design (easy to add new agents)

---

## 🧩 Agents Used

### 1️⃣ Primary Support Agent
- Acts as a **router**
- Determines which agent should handle the query
- Never answers directly unless necessary

### 2️⃣ Billing Support Agent
Handles:
- Payments
- Refunds
- Invoices
- Subscription issues

### 3️⃣ Technical Support Agent
Handles:
- Bugs
- Errors
- Login issues
- System failures

### 4️⃣ General Support Agent
Handles:
- Account questions
- Product information
- General inquiries

---

## 🛠️ Tech Stack

- **Python**
- **LangChain**
- **LangChain Core**
- **OpenAI / Compatible LLMs**
- **Jupyter Notebook**

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
2️⃣ Create Virtual Environment (Recommended)
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
3️⃣ Install Dependencies
pip install -r requirements.txt
4️⃣ Set Environment Variables
export OPENAI_API_KEY="your_api_key_here"
(On Windows)

setx OPENAI_API_KEY "your_api_key_here"
▶️ Running the Project
Open the Jupyter Notebook:

jupyter notebook Customer-Support-Agent-with-Handoffs.ipynb
Run the cells sequentially and start interacting with the customer support agent.

📌 Example Queries
“I was charged twice for my subscription” → Billing Agent

“My app crashes when I log in” → Technical Support Agent

“How do I update my profile?” → General Support Agent

🔮 Future Improvements
Add memory for long-term conversations

Integrate with ticketing systems (Zendesk / Freshdesk)

Add human-in-the-loop escalation

Deploy as an API or web app

Add analytics for agent performance

📚 References
LangChain Multi-Agent Handoffs
https://docs.langchain.com/oss/python/langchain/multi-agent/handoffs-customer-support
