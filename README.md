# 🤖 LLM_Connect Plugin for Unreal Engine

**LLM_Connect** is a powerful yet lightweight Unreal Engine plugin designed to connect your Blueprints with top-tier Large Language Models (LLMs) like OpenAI's GPT, Google's Gemini, Claude, DeepSeek, and  Ollama models. It enables seamless communication using a single Blueprint node — no C++ required.

---

## ✨ Features

- 🔹 **Unified Blueprint Node** – Send prompts and receive responses easily.
- 🔹 **Multiple LLM Support**:
  - Google **Gemini**
  - OpenAI **GPT**
  - **Claude** by Anthropic
  - **DeepSeek**
  - **Ollama** models
- 🔹 **Dropdown Model Selection**
- 🔹 **API Key, Prompt, Model Name and Server Input**
- 🔹 **Streaming Parsing Support** (Ollama)
- 🔹 **Text-only Smart Extraction**

---

## 🎮 Use Cases

- AI-powered NPC conversations
- Dynamic quest generation
- Developer tools powered by LLMs
- Text-to-text generation, summarization, or scripting logic

---

## 📦 Installation

1. Place the plugin in your UE project’s `Plugins/` folder.
2. Regenerate project files and build.
3. Enable it from `Edit > Plugins > LLM_Connect`.

---

## 🧠 How It Works

### 🔷 Blueprint Node: `SendLLMRequest`

| Pin | Type | Description |
|-----|------|-------------|
| **LLM Type** | Enum | Select from GPT, Gemini, Claude, etc. |
| **API Key** | String | Your LLM API key (not required for Ollama) |
| **Prompt** | String | Input prompt/question for the model |
| **Model** | String | Model ID (e.g., `gpt-4`, `claude-opus`, etc.) |
| **Server IP:Port** | String | For Ollama – server endpoint |
| **Max Tokens** | Int | (Claude) Optional token cap |
| **OnSuccess** | Output | Event triggered on valid response |
| **Result** | String | Parsed AI response content |

---

## 🧩 Blueprint Example

> 📌 Below is an example of the `SendLLMRequest` node setup in Blueprint:

![LLM Node Blueprint Example](/node_example.png)


---

## 💼 Purchase

This plugin is available for purchase on **fab**.  
➡️ **[Buy Now on Fab](https://www.fab.com/sellers/rootrootQ)**

---


## 🙌 Created by

**rootrootQ**  
Youtube @rootrootQ
