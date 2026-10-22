إليك محتوى ملف **`README.md`** كاملاً ومحدثاً بـ **البرومبت الكامل** والصورة التي صممناها، لتنسخه وتلصقه مباشرة في ملف الـ README الخاص بك على GitHub:

```markdown
# 🤖 NewsAI: Automated AI News Curator & Audio Digest

An advanced automation workflow built with **n8n** that collects the latest Artificial Intelligence news, filters recent updates, processes and summarizes them intelligently using **Google Gemini AI**, and sends both a formatted text digest and a natural **Voice/Audio summary** directly to your **Telegram** channel or chat.

---

## 🖼️ Workflow Banner

![NewsAI Architecture Banner](./banner.jpg)

> **Banner Generation Prompt:**
> *A professional dark-themed high-tech landscape banner for a GitHub repository titled "NewsAI: Automated AI News Curator & Audio Digest". The image clearly illustrates a modern automation workflow diagram from left to right. On the far left, show input node boxes representing RSS Feeds with tech logos (like TechCrunch and OpenAI). A glowing connecting wire leads into a Filter node labeled "Filter (24h)", then into an Aggregate node, which connects to a central glowing AI brain node labeled "Basic LLM Chain" featuring the Google Gemini logo. From the Gemini node, two output branches emerge: one branch goes upwards to a Telegram icon labeled "Telegram (Text)" showing a clean Markdown chat window preview; the other branch goes downwards through a sound wave node labeled "OpenAI TTS" with vibrant audio waves leading into a headphones/audio icon labeled "Telegram (Audio)". In the bottom right corner, include a sleek avatar tag that says "Developed by salman-dev-ai". Modern neon lighting, glowing circuitry background, ultra-sharp detail, cinematic tech aesthetics, 16:9 aspect ratio.*

---

## 🚀 Key Features

* **Automated Scheduling:** Runs automatically at specified times using Schedule Triggers.
* **RSS Aggregation:** Collects real-time tech news from top sources like TechCrunch and OpenAI.
* **Smart Filtering:** Automatically filters articles published within the last 24 hours.
* **AI-Powered Curation:** Leverages **Google Gemini** to extract key insights, write engaging headlines, and translate/format content into fluent Arabic.
* **Dual Output (Text & Audio):** 
  * Sends a clean Markdown text summary to Telegram.
  * Converts the summary into an audio file (TTS) for on-the-go listening.
* **No-Code Architecture:** Fully visual automation pipeline built entirely within n8n.

---

## 🛠️ Workflow Architecture

```text
[Schedule Trigger] 
       ↓
   [RSS Read] ──► [Filter (24h)] ──► [Aggregate Items]
                                           ↓
                                  [Basic LLM Chain] ──► [Google Gemini Model]
                                           ↓
                        ┌──────────────────┴──────────────────┐
                        ▼                                     ▼
             [Telegram: Send Text]                 [OpenAI: Text-to-Speech]
                                                              ↓
                                                   [Telegram: Send Audio]

```

---

## 📋 Prerequisites & Requirements

Before importing the workflow, make sure you have:

1. An active **n8n** instance (Cloud or Self-Hosted).
2. A **Telegram Bot Token** (created via [@BotFather](https://t.me/BotFather)) and your **Chat ID**.
3. A **Google Gemini API Key** for the LLM chain.
4. An **OpenAI API Key** (for text-to-speech audio generation).

---

## ⚙️ Installation & Setup

1. Clone this repository or download the workflow JSON file:
```bash
git clone [https://github.com/salman-dev-ai/n8n-ai-news-summarizer-telegram.git](https://github.com/salman-dev-ai/n8n-ai-news-summarizer-telegram.git)

```


2. Open your **n8n** dashboard.
3. Create a new workflow, click on the options menu (`...`), and select **Import from File**.
4. Upload the provided JSON workflow file.
5. Configure your credentials:
* Connect your Telegram account/bot credentials.
* Add your Google Gemini API credentials.
* Add your OpenAI credentials for audio generation.


6. Update the **Chat ID** inside the Telegram nodes with your personal ID.
7. Click **Save** and test the workflow!

---

## 👤 Author

* **Salman Al-Ansi**
* **Portfolio:** [salman-al-ansi.vercel.app](https://portfolio-en-salman-32c9.vercel.app/)
* **GitHub Repository:** [salman-dev-ai/n8n-ai-news-summarizer-telegram](https://github.com/salman-dev-ai/n8n-ai-news-summarizer-telegram)

*Let's connect and build amazing automations!*

