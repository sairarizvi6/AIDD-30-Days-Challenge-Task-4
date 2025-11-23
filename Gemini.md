✨ **Gemini CLI Project Prompt** 

Project: PDF Summarizer & Quiz Generator Agent

Core Agent Name: PDF Learning Assistant

📌 **Initial Setup & Context Preservation**

1. Documentation File (GEMINI.md)
   
Create or overwrite a file named GEMINI.md in the project’s root directory.

This file must store the full project prompt (from “Project Goal” to “Final Action Step”).

This ensures long-term context for all future tasks and commands.

🎯 **Project Goal**

Build an intelligent, interactive system that can:

1.	Extract text from an uploaded PDF
   
2.	Generate a clean summary using the Gemini model
   
3.	Create quizzes (MCQs + mixed questions) based on the PDF’s original text
   
The system will serve as an automated study assistant for students.

🧠 **Technology Stack**

•	Model / Server: Gemini CLI (gemini-2.5-pro or higher)

•	MCP Server: Use Context7 as the required MCP server context

•	Agent Framework: OpenAI Agents SDK (Python)

•	Frontend: Streamlit

•	PDF Extraction: PyPDF / pypdf

🧩 **Agent Functionality (A): PDF Summarizer**

1. Input

User uploads a PDF through Streamlit (using st.file_uploader).

2. Extraction

•	Use PyPDF to extract text from all pages.

•	Handle extraction issues gracefully (corrupted PDF, empty pages, etc.).

3. Processing

•	Send the extracted text to the Gemini model.

•	The model must return a clear, concise, meaningful summary of the full document.

4. Output

•	Display the summary in Streamlit.

•	UI is flexible — summary may be shown in a card, container, block, expander, etc.

🧩 **Agent Functionality (B): Quiz Generator**

Trigger

A button labeled “Create Quiz” appears only after a summary has been generated.

Input Source

Use the complete original PDF text, NOT the summary.

Generation Requirements

1. MCQs

•	Minimum 10 high-quality MCQs

•	Each with 4 options (A, B, C, D)

•	Model must provide a hidden correct answer key

2. Mixed Question Types

Add 5–10 more items from formats like:

•	True/False

•	Fill-in-the-blank

•	Short descriptive prompts

Total questions: 15–20

Output

•	Display the quiz clearly in Streamlit

•	Include a “Check Answers” feature for user interaction

⚙️**Technical Requirements**

•	Structure the agent using the OpenAI Agents SDK

•	Use clean, well-organized Python code

•	Add requirements.txt for dependency control

•	Handle errors correctly (e.g., invalid file uploads, extraction failures)

•	App must run via:

streamlit run app.py

🚀 **Final Action Step**

Generate the full, self-contained code for the PDF Learning Assistant project, including:

•	app.py (Streamlit UI)

•	Agent logic using OpenAI Agents SDK

•	PDF extraction logic via PyPDF

•	Complete GEMINI.md file containing the entire project prompt




