# 🗣️ Context Bot (Boribot)

> **"Translating geek speak... into human speak"** 
> An intelligent AI assistant on LINE OA that explains jargon or technical terms from various industries into easy-to-understand language, while recommending appropriate solutions and services.

---

## 🌟 Key Features

1. **AI Jargon Translator:** Translates difficult technical terms (e.g., *Thread tapping*, *API*, *Wireframe*) into everyday language that anyone can instantly understand.
2. **Conversation Memory:** The bot features a context memory system (remembering the last 10 messages), allowing you to ask follow-up questions seamlessly, just like talking to a real person without losing the context.
3. **Smart Quick Replies (Next Steps):** Once the AI answers a question, a smart system predicts and generates **"Next step questions"** as quick reply buttons. This keeps the conversation flowing and provides users with deeper insights effortlessly.
4. **Lead Generation & Affiliate (Business Model):** If a problem requires assistance from an expert or professional, the AI will recommend relevant services and attach sponsor or partner links (URLs) via a separate message block.

---

## 🛠️ Tech Stack

*   **Runtime:** Node.js
*   **Framework:** Express.js
*   **Messaging Platform:** LINE Messaging API (`@line/bot-sdk` v10.x.x)
*   **AI Engine:** DeepSeek API (`deepseek-chat`) via the `openai` package

---

## 🚀 Getting Started

### 1. Prerequisites
*   Install **Node.js** (version 16 or higher)
*   A **LINE Developers** account with a created Provider / Channel (Messaging API)
*   A **DeepSeek API** account with an API Key ready
*   Install **ngrok** for port forwarding your local machine to a Public URL (for local development)

### 2. Installation
1. Clone or create the project folder and navigate into it, then run:
   ```bash
   npm install
   ```
2. Create a `.env` file in the root folder using the format below:
   ```env
   PORT=3000
   LINE_CHANNEL_ACCESS_TOKEN=your_LINE_TOKEN_here
   LINE_CHANNEL_SECRET=your_LINE_SECRET_here
   DEEPSEEK_API_KEY=your_DEEPSEEK_API_KEY_here
   ```

### 3. Running the Server
Open your terminal and run the following command:
```bash
node server.js
```
*(If successful, you will see the message: `🚀 บอทบริบท (พลัง DeepSeek) กำลังรันอยู่ที่ http://localhost:3000`)*

### 4. Connecting with LINE (Webhook)
1. Open a new terminal tab (leave the first one running) and execute:
   ```bash
   ngrok http 3000
   ```
2. Copy the destination URL (e.g., `https://...ngrok-free.app`) and paste it into the **LINE Developers > Messaging API > Webhook URL** field. 
   *(Don't forget to append `/webhook` at the end of the link, e.g., `https://xxxx.ngrok-free.app/webhook`)*
3. Click `Verify` and toggle on `Use webhook`.

---
*Created as a Hackathon / Startup Pitch Idea MVP.*
