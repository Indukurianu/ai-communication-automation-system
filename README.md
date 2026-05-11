# ai-communication-automation-system
AI-powered n8n workflow using webhook, Google Gemini, and conditional routing for Gmail and WhatsApp communication automation.

## ⚙️ Architecture

Webhook Trigger → Basic LLM Chain → Google Gemini Chat Model → IF Node → Gmail / WhatsApp (HTTP Request)

---

## 🧠 How It Works

1. **Webhook Trigger**
   - Receives incoming API requests

2. **AI Processing**
   - Uses Basic LLM Chain + Google Gemini Chat Model
   - Generates structured JSON output

3. **Routing Logic**
   - IF Node decides destination

4. **Communication Layer**
   - Gmail sends email
   - WhatsApp sends message via HTTP Request

---

## 🔗 Webhook Example

POST `/webhook/ai-communication`

```json
{
  "message": "Send interview confirmation email",
  "channel": "gmail"
}
