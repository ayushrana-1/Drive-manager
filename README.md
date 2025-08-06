## 📂 Drive Manager — WhatsApp Based Google Drive Automation

This workflow allows you to control your Google Drive directly via WhatsApp using simple text instructions (no commands like `/delete`). It supports listing files, deleting, moving, and summarizing files using Gemini AI.

---

### 🧠 Features

* 🔍 Search and list Google Drive folders/files
* 🗑️ Confirm and delete files
* 📁 Move files to another folder
* 📝 Summarize document content via Gemini AI
* ✅ WhatsApp-based interaction (No Telegram used)
* ⚙️ AI-based confirmation and natural language understanding

---

### ⚙️ Nodes Used

| Node Type            | Purpose                                          |
| -------------------- | ------------------------------------------------ |
| `Webhook`            | Trigger WhatsApp input                           |
| `Function`           | Split & extract text from user input             |
| `Switch`             | Determine what action to take                    |
| `GoogleDriveTool`    | Perform actions (search, delete, move, download) |
| `HTTP Request`       | Call Gemini API for summaries                    |
| `Respond to Webhook` | Send result back to user via WhatsApp            |

---

### 💬 Example Messages

* `Show my design folder files`
* `Delete image hello.png from project folder`
* `Move final.pdf to archive folder`
* `Summarize notes.txt`

The assistant will ask for confirmation when it detects a delete request.

---

### 🤖 AI Prompt Logic

All responses are handled by an AI Agent with context memory. If a file deletion is requested, the bot confirms before proceeding. For summaries, the content of files is passed to Gemini API.

---

### 🔒 Note

Make sure:

* Google Drive credentials are correctly authorized
* Gemini API Key is set
* WhatsApp Webhook is active and receiving messages

---

🚀 That’s it! You now have a full WhatsApp-based Drive Manager using AI + automation.
