# Intelligent PDF Summarizer using Azure Durable Functions (Mocked Version)

## Overview
This project is a serverless solution built using **Azure Durable Functions**, **Blob Trigger**, **Form Recognizer**, and a **mocked OpenAI summarizer**. It simulates the extraction and summarization of text from uploaded PDF files in a scalable and event-driven manner.

> **Note:** Azure OpenAI quota was not available for student accounts. The summarization step uses a **mock summary** as per professor instructions.

---

## Features
-  Automatically triggered when a PDF is uploaded to Azure Blob Storage
-  Uses Azure Form Recognizer to extract text from PDFs
-  Mocks summarization using a sample response
-  Writes summary to the `output` Blob container as a `.txt` file

---

## Technologies Used
- Azure Functions (Python)
- Azure Durable Functions (Orchestrator + Activities)
- Azure Blob Storage
- Azure AI Form Recognizer
- Azure OpenAI (Mocked)
- GitHub, VS Code

---

## Project Structure

```bash
Intelligent-PDF-Summarizer/
├── function_app.py         # Main Durable Function App
├── local.settings.json     # Local config with env variables
├── requirements.txt        # Python dependencies
├── host.json
├── .venv/                  # Virtual environment
```

---

## How It Works (Step-by-Step)

1. **Upload** a PDF to the `input` container
2. **Durable Functions Orchestrator** starts:
   - `analyze_pdf`: Extracts text via Azure Form Recognizer
   - `summarize_text`: Mocks OpenAI response
   - `write_doc`: Writes `.txt` summary to `output` container
3. Summary file is ready for download in Blob Storage

---

## Mocked Output Example

```txt
This is a mock summary of the uploaded PDF document. Replace this with actual output once your Azure OpenAI quota is approved.
```

---

## Demo Video
https://www.youtube.com/watch?v=NUdGRoZW7ks
**Watch the video demo here:**  


---

## Author

**Parth Bodana**  
GitHub: [@boda0004](https://github.com/boda0004)

---


