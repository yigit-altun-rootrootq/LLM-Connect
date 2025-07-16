🤖 LLM_Connect Plugin for Unreal Engine
LLM_Connect is a powerful Unreal Engine plugin that enables seamless integration with Large Language Models (LLMs) via Blueprints. It supports OpenAI (GPT), Google Gemini, Anthropic Claude, DeepSeek, Ollama (local or remote), and LM Studio — all through a unified Blueprint node. You can send prompts and receive streamed or full responses in real time. No C++ coding is required.

✨ Features
🔹 Unified Blueprint Node: Communicate with multiple LLMs using a single Blueprint node.

🔹 Multi-LLM Support: Easily connect to popular models:

OpenAI GPT

Google Gemini

Claude by Anthropic

DeepSeek

Ollama (local models)

LM Studio (local or remote models)

🔹 Dropdown Model Selection: Choose from supported model names.

🔹 Flexible Input: Configure API Key, Prompt, Model Name, Server IP/Port, and more.

🔹 Streaming Parsing: Supports streamed output (Ollama).

🔹 Text-only Smart Extraction: Auto-extract meaningful responses from LLMs.

🏦 1. Installation (via Fab Marketplace)
Go to the Fab Marketplace.

Search for LLM Connect.

Purchase or add it to your Library.

Open the Epic Games Launcher, go to the Library, and install it to your Engine or Project.

📚 2. Adding to Your Unreal Project
Open your Unreal project.

Go to Edit → Plugins.

Find LLM Connect under Installed and enable it.

Restart the project when prompted.

🤖 3. Using the Plugin (Blueprint Only)
Open any Blueprint (e.g., Level Blueprint, Actor Blueprint).

Right-click in the Event Graph and search for LLM Connect.

Select the node: LLM Connect – Unified LLM Request.

⚛️ 4. Node Pin Reference
Pin	Type	Description
Model Type	Enum	Select the LLM service:
• GPT (OpenAI)
• Gemini (Google)
• Claude (Anthropic)
• DeepSeek
• Ollama (local)
• LM Studio
Model	String	The model to use.
Examples:
• gpt-4, gpt-3.5-turbo (GPT)
• gemini-pro, gemini-1.5-flash, gemini-1.5-pro (Gemini)
• claude-3-opus, claude-3-sonnet (Claude)
• deepseek-chat, deepseek-coder (DeepSeek)
• llama3, mistral, etc. (Ollama)
• lmstudio-chat (LM Studio)
API Key	String	API key required for GPT, Gemini, Claude, and DeepSeek.
Prompt	String	The question to send to the LLM.
Server IP/Port	String	For Ollama and LM Studio only. Example: http://localhost:11434.
Max Tokens	Integer	Used with Claude to limit response length.
Temperature	Float	(0.0 to 1.0) Controls randomness.
System Prompt	String	Optional role description (e.g., "You are a helpful assistant.").
On Success	Exec	Triggered when a response is received.
Response Text	String	The LLM's returned message.
Standard Exec Output	Exec	Normal flow output.

📈 5. API Behavior Table
Model	Requires API Key	Needs Server	Notes
GPT	✅ Yes	❌ No	e.g., gpt-3.5-turbo, gpt-4
Gemini	✅ Yes	❌ No	e.g., gemini-1.5-flash, gemini-1.5-pro
Claude	✅ Yes	❌ No	Needs Max Tokens
DeepSeek	✅ Yes	❌ No	e.g., deepseek-chat
Ollama	❌ No	✅ Yes	Server must be running locally.
LM Studio	❌ No	✅ Yes	Server must be running locally.

📂 6. Blueprint Example
Blueprint Flow

Begin Play ➔ LLM Connect Node

Configure:

Model Type: GPT

Model: gpt-3.5-turbo

Prompt: "What is the capital of France?"

API Key: [Your API Key]

On Success: Connect to Print String using Response Text

💡 7. Additional Notes
Ollama requires local installation and model setup.

LM Studio requires local installation and model setup.

Ollama and LM Studio do not use API Keys.

Other LLMs require valid API Keys for access.

All config data is runtime-only – nothing is saved.

Full source code is included.

⚖️ 8. Support & Documentation
GitHub: https://github.com/yigit-altun-rootrootq/LLM-Connect

Contact: https://www.youtube.com/@rootrootQ

© LLM Connect Plugin - 2025. All Rights Reserved.
