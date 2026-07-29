
# ✅ WhatsApp Task Management System

A WhatsApp Task Management System that allows task assignment, tracking, and completion via WhatsApp messages using a simple UI. Users can assign tasks, mark them as done, and view/manage tasks from a clean dashboard UI.

---

## 📦 Project Structure

/backend  
├── app.py → Flask webhook backend for WhatsApp  
├── db.py → SQLite DB logic (create, save, fetch, update)  
├── task_handler.py → WhatsApp task parsing and response logic  
├── scheduler.py → For scheduled reminders (if extended)  
├── tasks.db → SQLite DB file  
└── .env → Stores API key and WhatsApp base URL  

/dashboard  
├── app.py → Dashboard Flask app  
├── templates/index.html → Frontend UI  
├── static/ → (Optional) CSS/JS/Icons  
└── requirements.txt → Dashboard dependencies  

---

## 🔧 Getting Started

### 1️⃣ Clone & Navigate  
git clone https://github.com/yourusername/whatsapp-task-manager.git  
cd whatsapp-task-manager  

### 2️⃣ Create & Activate Virtual Environment  
cd backend  
python -m venv venv  
.\venv\Scripts\Activate.ps1 (for Windows PowerShell)  

### 3️⃣ Install Dependencies  
pip install -r requirements.txt  

### 4️⃣ Setup .env (in /backend)  
WHATSAPP_API_KEY=your_whapi_cloud_api_key  
WHATSAPP_BASE_URL=https://gate.whapi.cloud  

📝 Use https://whapi.cloud to create an account and get your API key.

---

## 📲 WhatsApp Interaction

Once your backend is running, send structured messages like:

### 🆕 Assign Task  
TASK: Finish dashboard, ASSIGNEE: Riya, TIME: 6PM, NOTES: Include status color coding  

✅ Response:  
✅ Task saved successfully ✅  
👤 Assignee: Riya  
🆔 Task ID: 1  
📝 Task: Finish dashboard  
⏰ Time: 6PM  
🧾 Notes: Include status color coding  

---

### ✅ Mark as Done  
DONE: 1  

✅ Response:  
✅ Task #1 marked as completed.

---

### 📋 View Tasks (via WhatsApp)  
LIST  
LIST Riya  

---

## 🖥️ Dashboard UI (HTML + Flask)

### ▶️ Run Dashboard UI  
cd dashboard  
python app.py  

Visit http://localhost:5500

---

### ✅ Features

- View all ongoing tasks (with filters by assignee)  
- Mark any task as done  
- Update notes for any task  
- Auto-send confirmation on WhatsApp to both user & assignee  

---

## 🔐 Environment Variables

The .env file is critical for secure and dynamic API usage. Do not hardcode your API keys.

WHATSAPP_API_KEY=your_actual_key  
WHATSAPP_BASE_URL=https://gate.whapi.cloud  

---

## 🔍 Proof of Concept (POC)

📸 screenshots here for:  
- WhatsApp task flow  
![Screenshot 2025-04-15 211551](https://github.com/user-attachments/assets/8e9743ae-e07a-4321-a590-9f70ccff64fe)
![Screenshot 2025-04-15 211647](https://github.com/user-attachments/assets/0ef90e32-666f-4d0e-b617-86a5398cd804)


- Dashboard interface
![Screenshot (219)](https://github.com/user-attachments/assets/cb6aa4c0-7f4b-4c08-ba45-48900bd7b32e)
![Screenshot (220)](https://github.com/user-attachments/assets/abba9610-4fd7-4d57-ac04-374a17d6d4d3)
![Screenshot (221)](https://github.com/user-attachments/assets/f405e811-e1f0-4f39-a54b-05c6cc199b9d)

  
Directory should be in this form 



![Screenshot 2025-04-15 211820](https://github.com/user-attachments/assets/e4d2dbdc-bea0-456b-8979-da552ddc450f)


---

## ✅ Features

- [x] WhatsApp webhook listener  
- [x] Task parsing and validation  
- [x] DONE task confirmation  
- [x] UI with task list & update actions  
- [x] Confirmation via WhatsApp for every update  

---






