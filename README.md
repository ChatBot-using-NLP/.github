# 🛒 Supermarket Assistant Chatbot using NLP  

An intelligent chatbot system for supermarkets that helps customers quickly locate goods by shelf number.  
The system combines **ASP.NET Core 9**, **React**, and **Python NLP** with **MongoDB** to provide an interactive, voice-enabled shopping assistant.  

---

## 🚀 Features
- 🗣 **Voice & Text Input** (React frontend with Web Speech API).  
- 🤖 **NLP Processing** (Python + spaCy) to extract product names from customer requests.  
- 📦 **MongoDB Integration** for managing products and shelf numbers.  
- ⚙️ **ASP.NET Core 9 Backend** for goods management and chatbot orchestration.  
- 🛠 **Admin Interface** (React) for adding/editing/deleting products dynamically.  
- 🖨 **Printable Shelf Summary** for customers.  

---

## 🏗️ Tech Stack
- **Frontend:** React (JavaScript, Web Speech API)  
- **Backend:** ASP.NET Core 9 Web API  
- **Database:** MongoDB (Products → Shelf mapping)  
- **NLP Service:** Python (FastAPI + spaCy)  

---

## 📂 System Architecture  

```text
                  ┌─────────────────────────┐
                  │       React Frontend     │
                  │  - Chatbot UI            │
                  │  - Voice/Text Input      │
                  │  - Admin Panel           │
                  └───────────▲─────────────┘
                              │  (REST API calls)
                              │
                  ┌───────────┴─────────────┐
                  │   ASP.NET Core 9 API     │
                  │  - Goods Management      │
                  │  - Orchestrates requests │
                  │  - Connects NLP + DB     │
                  └───────▲───────────▲─────┘
                          │           │
            ┌─────────────┘           └─────────────┐
            │                                       │
 ┌──────────┴──────────────┐           ┌────────────┴───────────┐
 │  Python NLP Service     │           │      MongoDB           │
 │  (FastAPI + spaCy)      │           │  Products Collection   │
 │  - Tokenization         │           │  { name, shelf }       │
 │  - Entity Extraction    │           │                       │
 └─────────────────────────┘           └───────────────────────┘
