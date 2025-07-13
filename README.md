# GenAI-Doc-Assistant
# GenAI Document Comprehension Assistant
A local AI-powered assistant that reads your research papers, legal files, or technical manuals — and helps you deeply understand them through contextual Q&A and logic challenges.

# Features
* Upload PDFs or TXT files
* Auto-generates a concise summary (≤ 150 words)
* Ask Anything Mode: ask free-form questions, get answers directly grounded in the document with references.
* Challenge Me Mode: the assistant generates 3 logic/comprehension questions — you answer, it evaluates, and justifies the feedback with exact text evidence.
* No hallucination: all answers are contextually linked to the uploaded content.
* Clean local web interface (built with Streamlit)

# Tech Tools
*	Frontend: Streamlit
*	Backend: Python, LangChain
*	LLM: OpenAI GPT (via API)
*	Vector Store: FAISS (for fast chunk retrieval)

# Setup & Run Locally
* Clone this repo
* Install dependencies
* Set your OpenAI API key
* Run the app

# How It Avoids Hallucination
*	Uses Retrieval Augmented Generation (RAG): document is split into chunks → embedded → stored in a vector DB (FAISS) → relevant chunks are retrieved for every query.
*	LLM answers only from the retrieved context — and every answer includes the supporting text or its location.
