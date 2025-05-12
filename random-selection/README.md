# 🔍 Random Code Snippet Selection

This repository contains code snippets randomly selected from various open-source projects. These snippets were either generated or modified using AI tools.  
The goal is to explore the **security vulnerabilities** and **efficiency trade-offs** present in AI-assisted development.

Selection criteria and methodology are included as part of the project documentation.

---

## 📦 Repositories Analyzed

1. [Simple Chat App](https://github.com/100x-Engineers/simple-chat-app)  
2. [GPT Chatbot](https://github.com/nadvolod/gpt-chatbot)  
3. [Flask Twitter](https://github.com/Jmete/flask-twitter)  
4. [Weather App](https://github.com/DalpatRathore/weather-app)  
5. [Pop Frenzy Game](https://github.com/AndrewSink/Pop-Frenzy)  
6. [AI Image Generator](https://github.com/yusuftomilola/ai-images-generator)  

---

### 🧪 [Simple Chat App](https://github.com/100x-Engineers/simple-chat-app)

**Risks Identified:**
- 🚫 Insecure input handling: `io.emit('chat message', msg)` broadcasts raw messages — vulnerable to XSS.
- 🧠 Unvalidated usernames: risks spoofing and DoS through crafted input.
- ⚠️ Shared mutable state (`onlineUsers`) can cause race conditions under load.

---

### 🧠 [GPT Chatbot](https://github.com/nadvolod/gpt-chatbot)

**Risks Identified:**
- 🔑 API key (`OPENAI_API_KEY`) exposed in server logic with no rate-limiting or proxying.
- ❗ Raw user input sent to OpenAI API without sanitization — prone to injection or abuse.

---

### 🐦 [Flask Twitter](https://github.com/Jmete/flask-twitter)

**Risks Identified:**
- 🔁 Unvalidated query input (`screen_name`) passed to external API — risk of enumeration or abuse.
- ❌ Blanket `except:` hides errors, reducing auditability.
- 🔓 No input validation or rate-limiting.

---

### 🌦️ [Weather App](https://github.com/DalpatRathore/weather-app)

**Risks Identified:**
- 🔐 API key in frontend (`VITE_WEATHER_API_KEY`) exposed to browser clients.
- 🚫 Hardcoded city (`Jaipur`) restricts flexibility and misleads testing assumptions.

---

### 🎮 [Pop Frenzy](https://github.com/AndrewSink/Pop-Frenzy)

**Risks Identified:**
- 🕳️ Obfuscated/minified JavaScript logic — lacks transparency or auditability.
- ❗ WebGL canvas rendering could trigger performance or sandboxing issues.
- 🔍 No source validation possible without original, unbundled files.

---

### 🖼️ [AI Image Generator](https://github.com/yusuftomilola/ai-images-generator)

**Risks Identified:**
- ✏️ User prompts sent to `/dalle` endpoint without sanitization — risks prompt injection or offensive content.
- 🧾 Image returned as base64 with no validation or upload constraints — unsafe content risks.
- 🔁 Fetch requests are unauthenticated — vulnerable to misuse or abuse of endpoints.

---

## 📘 License

This repository is part of a research project on secure AI-assisted development. All included code snippets are used for educational and academic analysis under fair use.

