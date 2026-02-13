# 🤖 AI Multi-Channel Marketing Agent

> **Automate your marketing pipeline from a single form submission.** 

The **AI Multi-Channel Marketing Agent** is a sophisticated automation system built with **n8n**, **LLMs**, and **Structured Output Parsing**. It transforms raw event data into polished, platform-specific marketing content and distributes it across multiple digital channels automatically.

---

## 🌟 Key Features

- **🧠 Agentic Orchestration**: Uses AI to handle complex decision-making and content generation logic.
- **🎨 Dynamic Poster Generation**: Automatically renders high-quality HTML/CSS posters and converts them to images.
- **📱 Multi-Channel Distribution**: Tailors content specifically for **LinkedIn**, **Email**, **Telegram**, and **WhatsApp**.
- **🔍 Structured Validation**: Employs JSON schema validation to ensure consistent and reliable AI outputs.
- **⚡ Conditional Routing**: Smart logic to publish only to the channels selected by the user.

---

## 🏗️ System Architecture

The workflow follows a linear yet intelligent progression:

1.  **Input Phase**: User submits event details (Topic, Venue, Date, Time) via an n8n Form.
2.  **AI Reasoning**: 
    - A central AI Agent (Groq/Ollama) generates structured core content.
    - Specialized sub-tasks generate platform-specific copy (LinkedIn Hooks, Email Invites, Telegram Posts).
3.  **Visualization**:
    - A JavaScript engine dynamically injects AI content into a pre-designed HTML/CSS template.
    - The `HTM-to-Image` API captures the rendered HTML as a shareable graphic.
4.  **Distribution**:
    - **LinkedIn**: Formats professional posts with hooks and hashtags.
    - **Email**: Sends styled HTML invitations via Gmail.
    - **Telegram**: Publishes the generated image alongside an energetic post.
    - **WhatsApp**: Routes content for instant messaging.

---

## 🛠️ Tech Stack

### Automated Core
- **[n8n](https://n8n.io/)**: The backbone of the entire workflow orchestration.
- **[LangChain](https://www.langchain.com/)**: powers the AI Agent and Structured Output Parsing.

### Artificial Intelligence
- **Groq / Ollama**: High-speed LLM inference for content generation.
- **Models**: `kimi-k2`, `qwen3-coder`, `cogito-2.1`.

### Design & Visuals
- **HTML5 / CSS3**: For responsive and modern poster templates.
- **HTML-CSS-to-Image API**: To bridge the gap between web code and social media graphics.

### Communication APIs
- **Gmail API**: For automated email outreach.
- **Telegram Bot API**: For instant channel publishing.

---

## ⚙️ Setup Instructions

### 1. Import Workflow
- Download the `Marketing Agent.json` file.
- Log in to your **n8n** instance.
- Click on **Workflows** > **Import from File...** and select the JSON.

### 2. Configure Credentials
You will need to set up the following credentials in n8n:
- **Groq API / Ollama**: For the brain of the agent.
- **Gmail OAuth2**: For sending emails.
- **Telegram Bot API**: For channel posts.
- **HTML/CSS to Image API**: For generating poster graphics.

### 3. Customize Branding
- Locate the **"Code in JavaScript"** node.
- Modify the `const html` template to match your brand colors, logos, and fonts.

### 4. Activate & Run
- Toggle the **Active** switch in n8n.
- Access the **Form Trigger** URL to start generating your first campaign!

---

## 🎯 Use Cases

Ideal for:
- 🎓 **Educational Institutions**: Promoting workshops and seminars.
- 🏢 **Corporate Teams**: Automating internal announcements.
- 📅 **Event Organizers**: Managing cross-platform event hype with zero manual effort.

---

## 📄 Repository Structure

```tree
.
├── Marketing Agent.json    # The core n8n workflow file
└── README.md               # Project documentation
```

---

*Built with ❤️ to simplify AI-driven marketing automation.*
