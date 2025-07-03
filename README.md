# 🤖 LLM\_Connect Plugin for Unreal Engine

**LLM\_Connect** is a powerful Unreal Engine plugin that enables seamless integration with Large Language Models (LLMs) via Blueprints. It supports **OpenAI (GPT)**, **Google Gemini**, **Anthropic Claude**, **DeepSeek**, and **Ollama (local or remote)** — all through a unified Blueprint node. You can send prompts and receive streamed or full responses in real time. No C++ coding is required.

---

## ✨ Features

* 🔹 **Unified Blueprint Node**: Communicate with multiple LLMs using a single Blueprint node.
* 🔹 **Multi-LLM Support**: Easily connect to popular models:

  * OpenAI **GPT**
  * Google **Gemini**
  * **Claude** by Anthropic
  * **DeepSeek**
  * **Ollama** (local models)
* 🔹 **Dropdown Model Selection**: Choose from supported model names.
* 🔹 **Flexible Input**: Configure API Key, Prompt, Model Name, Server IP/Port, and more.
* 🔹 **Streaming Parsing**: Supports streamed output (Ollama).
* 🔹 **Text-only Smart Extraction**: Auto-extract meaningful responses from LLMs.

---

## 🏦 1. Installation (via Fab Marketplace)

1. Go to the **Fab Marketplace**.
2. Search for **LLM Connect**.
3. Purchase or add it to your Library.
4. Open the **Epic Games Launcher**, go to the **Library**, and install it to your Engine or Project.

---

## 📚 2. Adding to Your Unreal Project

1. Open your Unreal project.
2. Go to `Edit → Plugins`.
3. Find **LLM Connect** under Installed and enable it.
4. Restart the project when prompted.

---

## 🤖 3. Using the Plugin (Blueprint Only)

1. Open any Blueprint (e.g., Level Blueprint, Actor Blueprint).
2. Right-click in the Event Graph and search for `LLM Connect`.
3. Select the node: **LLM Connect – Unified LLM Request**.

---

## ⚛️ 4. Node Pin Reference

| Pin                      | Type    | Description                                                                                                                                                                                                                                                                      |
| ------------------------ | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Model Type**           | Enum    | Select the LLM service:<br>• GPT (OpenAI)<br>• Gemini (Google)<br>• Claude (Anthropic)<br>• DeepSeek<br>• Ollama (local)                                                                                                                                                         |
| **Model**                | String  | The model to use.<br>*Examples*:<br>• `gpt-4`, `gpt-3.5-turbo` (GPT)<br>• `gemini-pro`, `gemini-1.5-flash`, `gemini-1.5-pro` (Gemini)<br>• `claude-3-opus`, `claude-3-sonnet` (Claude)<br>• `deepseek-chat`, `deepseek-coder` (DeepSeek)<br>• `llama3`, `mistral`, etc. (Ollama) |
| **API Key**              | String  | API key required for GPT, Gemini, Claude, and DeepSeek.                                                                                                                                                                                                                          |
| **Prompt**               | String  | The question to send to the LLM.                                                                                                                                                                                                                                                 |
| **Server IP/Port**       | String  | For Ollama only. Example: `http://localhost:11434`.                                                                                                                                                                                                                              |
| **Max Tokens**           | Integer | Used with Claude to limit response length.                                                                                                                                                                                                                                       |
| **Temperature**          | Float   | (0.0 to 1.0) Controls randomness.                                                                                                                                                                                                                                                |
| **System Prompt**        | String  | Optional role description (e.g., "You are a helpful assistant.").                                                                                                                                                                                                                |
| **On Success**           | Exec    | Triggered when a response is received.                                                                                                                                                                                                                                           |
| **Response Text**        | String  | The LLM's returned message.                                                                                                                                                                                                                                                      |
| **Standard Exec Output** | Exec    | Normal flow output.                                                                                                                                                                                                                                                              |

---

## 📈 5. API Behavior Table

| Model    | Requires API Key | Needs Server | Notes                                      |
| -------- | ---------------- | ------------ | ------------------------------------------ |
| GPT      | ✅ Yes            | ❌ No         | e.g., `gpt-3.5-turbo`, `gpt-4`             |
| Gemini   | ✅ Yes            | ❌ No         | e.g., `gemini-1.5-flash`, `gemini-1.5-pro` |
| Claude   | ✅ Yes            | ❌ No         | Needs `Max Tokens`                         |
| DeepSeek | ✅ Yes            | ❌ No         | e.g., `deepseek-chat`                      |
| Ollama   | ❌ No             | ✅ Yes        | Server must be running locally.            |

---

## 📂 6. Blueprint Example

> **Blueprint Flow**
>
> `Begin Play` ➔ `LLM Connect Node`
>
> Configure:
>
> * **Model Type**: GPT
> * **Model**: `gpt-3.5-turbo`
> * **Prompt**: "What is the capital of France?"
> * **API Key**: \[Your API Key]
> * **On Success**: Connect to `Print String` using `Response Text`

---

## 💡 7. Additional Notes

* Ollama requires local installation and model setup.
* Ollama does **not** use API Keys.
* Other LLMs require **valid API Keys** for access.
* All config data is runtime-only – nothing is saved.
* Full source code is included.

---

## ⚖️ 8. Support & Documentation

* GitHub: [https://github.com/yigit-altun-rootrootq/LLM-Connect](https://github.com/yigit-altun-rootrootq/LLM-Connect)
* Contact: [https://www.youtube.com/@rootrootQ](https://www.youtube.com/@rootrootQ)

---

© LLM Connect Plugin - 2025. All Rights Reserved.
