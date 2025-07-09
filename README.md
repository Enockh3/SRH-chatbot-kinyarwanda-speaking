# 🤖 Kinyarwanda-Speaking Chatbot for Sexual and Reproductive Health (SRH)

This is a prototype **RAG-based chatbot** designed to provide accurate, culturally relevant information on **Sexual and Reproductive Health (SRH)** in **Kinyarwanda**, integrated with **WhatsApp via Twilio**.

Built using **LangChain**, **OpenAI's GPT-4o-mini**, and **FAISS vectorstore**, this project demonstrates how Retrieval-Augmented Generation can be applied to real-world public health challenges in low-resource languages.

---

## 🌍 Project Goals

- 📲 Improve access to reliable SRH information in Kinyarwanda
- 💬 Support WhatsApp-based queries via conversational AI
- 🧠 Recommend family planning options based on user context (via prediction model)
- 🌐 Demonstrate use of RAG in a low-resource language and testing environment

---

## ⚙️ Tech Stack

- **Flask** – Web framework for the chatbot API  
- **LangChain** – For RAG pipeline and conversation memory  
- **OpenAI GPT-4o-mini** – LLM for generation  
- **FAISS** – Vector store for document retrieval  
- **Twilio API** – For WhatsApp message integration  
- **PyMuPDF, PowerPoint & Text Loaders** – For loading SRH content  
- **Ngrok** – To expose local Flask server for Twilio testing  
- **dotenv** – For API key management

---

## 📦 Features

- ✅ Chatbot supports **Kinyarwanda SRH content**
- ✅ Uses **RAG** to respond with domain-specific answers  
- ✅ Runs in **Twilio Sandbox** (test environment)  
- ✅ Handles multiple user sessions with conversation history  
- ✅ Real-time chat through WhatsApp interface  
- ✅ Flask-based server runs with background thread & ngrok tunneling  

---

## 🛠️ How It Works

1. **Load SRH documents** (PDF, PPTX, TXT) from local directory  
2. **Split content** into chunks and store embeddings in **FAISS vectorstore**  
3. Create **retriever** for document search  
4. Initialize **ChatOpenAI** model (GPT-4o-mini) and conversation memory  
5. User sends a message on WhatsApp → handled via Flask route `/bot`  
6. Twilio webhook receives the message, sends it to the LangChain chain  
7. Bot returns a generated response based on retrieval + LLM output  
8. Response is sent back to the user via Twilio's WhatsApp Sandbox

---

## 🧪 Current Limitations

- 🔒 Only tested via **Twilio Sandbox** (not deployed for production use)  
- 🧠 LLM is not fine-tuned; responses depend on the quality of retrieval  
- 💾 Local-only; not yet deployed to cloud (e.g., AWS, GCP, etc.)  
- 📊 Prediction model for contraceptive preference not yet integrated into chatbot flow  

---

## 📍 Example Use Cases

- "Ni ubuhe buryo bwo kuboneza urubyaro bushobora kunyobora?"  
- "Ese ibinini byo kuboneza urubyaro bifite ingaruka?"  
- "Ni ryari umugore ashobora gusama nyuma yo kubyara?"

---

## 🧑‍💻 Author

**Enock Habimana**  
Medical Student | Data Science Enthusiast  
📍 Kigali, Rwanda  
📧 habimanaenock15@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/enockh)





