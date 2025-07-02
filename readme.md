# Motivational Interviewing System Prompt for Misinformation Detection

This repository contains two versions (prompt.html and prompt.json) of a carefully designed system prompt used for guiding a local LLM (via Ollama) in detecting and addressing misinformation in German politics** through the lens of Motivational Interviewing (MI).

## Project Context

This is part of an internship project focused on:
- **Detecting misinformation/disinformation** in short-form video content (e.g., TikTok, Instagram Reels)
- Guiding users out of misinformation using **Motivational Interviewing (MI)** techniques
- Leveraging **local LLMs** running inside Docker containers via **Ollama**
- Extending the system later with **RAG (Retrieval-Augmented Generation)** and potential **fine-tuning**

---

## Files Overview

 1. prompt.html: Human-readable version using custom tags to guide LLM behavior. Optimized for use in UI-based interfaces (e.g., Open WebUI).

 2. prompt.json: Structured version using JSON. Ideal for backend parsing, LangChain integration, or REST API-based prompt injection.

---

## Prompt Goals

- Empathically guide users who consumed misleading short-form content
- Use **Motivational Interviewing (MI)** techniques:
  - Reflective listening
  - Non-confrontational questioning
  - Encouraging user-led change
- Limit output verbosity and avoid overwhelming the user
- Format responses for readability and clarity

---

## Features

-  Uses **OARS**: Open Questions, Affirmations, Reflections, Summaries  
-  Limits to **max 2 questions per response**  
-  Emphasizes **autonomy**, avoids **persuasion without permission**  
-  Includes example interaction for behavior anchoring  
-  Optional word limit (≤150 words) to reduce verbosity

---

## Integration Guide

You can load the system prompt in two common ways:

###  With Ollama/Open WebUI:
Use prompt.html in the system prompt input field. Works well with markdown rendering.

### With LangChain or API injection:
Use prompt.json and feed it to the system using a structured chain or REST API wrapper. Recommended for scalable RAG pipelines.

---

## Session Context

- Language preferences: US English and DE German
- Assumes user has just watched a TikTok/short-form video and is questioning its claims
- Focuses on **German political topics**, but adaptable to other misinformation themes

---

## Future Extensions

- Integration with **Whisper** for voice-to-text transcription of TikTok videos
- Connection with **OCR and caption parsers** for carousel or image-based content
- **RAG backend** to support grounded, source-aware responses
- Possible **fine-tuning** of LLaMA model using MI-annotated dialogues

---

## Credits

Internship Project by: Brian Llane
Supervised by: *Omed Abed*  
Institution: *Hochschule Rhein-Waal*  
Model: Any model via Ollama (local, containerized) using Open WebUI



