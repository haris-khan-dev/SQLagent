[README.md](https://github.com/user-attachments/files/22439270/README.md)
# 🛡️ SQL Agent Security & Analytics

A hands-on educational repository demonstrating the evolution from basic SQL agents to secure, production-ready analytics systems using LangChain and OpenAI. Learn step-by-step how to build safe, effective SQL agents for business intelligence.

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- OpenAI API key (for scripts using LLMs)
- Basic knowledge of SQL and Python

### Setup Instructions
```bash
# 1. Create and activate a virtual environment (from project root)
python -m venv .venv && source .venv/bin/activate

# 2. Install dependencies
pip install -r requirements.txt

# 3. Navigate to the SQLAgent folder
cd SQLAgent

# 4. (Optional) Reset the database to its initial state
python scripts/reset_db.py

# 5. Run the tutorial scripts in order
python scripts/00_simple_llm.py         # Simple LLM usage (no agents/tools)
python scripts/01_simple_agent.py       # Basic SQL agent
python scripts/02_risky_delete_demo.py  # ⚠️ Dangerous patterns (educational)
python scripts/03_guardrailed_agent.py  # Secure implementation
python scripts/04_complex_queries.py    # Advanced analytics
```

## 📁 Project Structure
```
agent/
├── requirements.txt
├── README.md
└── SQLAgent/
    ├── sql_agent_class.db         # SQLite database with sample data
    ├── sql_agent_seed.sql         # Database schema and seed data
    └── scripts/
        ├── 00_simple_llm.py           # Simple LLM usage
        ├── 01_simple_agent.py         # Basic SQL agent
        ├── 02_risky_delete_demo.py    # Dangerous patterns (educational)
        ├── 03_guardrailed_agent.py    # Secure SQL agent
        ├── 04_complex_queries.py      # Advanced analytics
        └── reset_db.py                # Database reset utility
```

## 📚 Learning Progression
Each script demonstrates a new concept or security improvement:

1. **00_simple_llm.py** – Pure LLM usage, no database or agent
2. **01_simple_agent.py** – Basic SQL agent, unrestricted access
3. **02_risky_delete_demo.py** – Shows dangerous patterns and why security is needed
4. **03_guardrailed_agent.py** – Secure agent with input validation and guardrails
5. **04_complex_queries.py** – Advanced analytics and business intelligence

## 🔒 Security Concepts Demonstrated
- Input validation and SQL injection prevention
- Whitelist-based security (only allow SELECT statements)
- Result set limiting
- Multi-statement prevention
- Error handling and safe reporting

## 🗄️ Database Schema
The included SQLite database (`sql_agent_class.db`) contains realistic e-commerce data with tables for customers, orders, order_items, products, payments, and refunds. The schema and seed data are in `sql_agent_seed.sql`.

## ⚠️ Safety Guidelines
- Use the provided SQLite database for learning only
- Do NOT use dangerous patterns from `02_risky_delete_demo.py` in production
- Always validate and restrict agent capabilities in real-world applications

## 🤝 Contributing
Contributions to improve documentation, security, or analytics examples are welcome!

---

**Start with the basics, understand the risks, and build robust, secure SQL agents!**
