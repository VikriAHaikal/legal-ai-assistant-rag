# 🤖 Legal AI Assistant: Fine-Tuning Llama 3 & RAG System

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Llama 3](https://img.shields.io/badge/Model-Llama--3--8B-orange)
![Unsloth](https://img.shields.io/badge/Fine--Tuning-Unsloth%20%2F%20QLoRA-brightgreen)
![LangChain](https://img.shields.io/badge/RAG-LangChain%20%2B%20ChromaDB-purple)
![Dicoding Grade](https://img.shields.io/badge/Dicoding-4%2F5%20Stars-gold)

Sistem asisten hukum berbasis kecerdasan buatan (*Large Language Model*) yang dirancang khusus untuk menjawab pertanyaan seputar **Regulasi & Undang-Undang Ketenagakerjaan Indonesia**. Proyek ini mengombinasikan teknik **Instruction Fine-Tuning (QLoRA)** dan **Retrieval-Augmented Generation (RAG)** untuk menghasilkan jawaban hukum yang akurat, terstruktur, dan minim halusinasi.

---

## 📸 Demo Preview

<video src="./demo.mp4" controls width="100%"></video>

> *Sistem mampu melakukan pencarian berbasis vektor ke dokumen hukum aktual dan memberikan jawaban beserta sitasi sumbernya.*

---

## 🌟 Fitur Utama

- **Fine-Tuned LLM (Llama 3 8B):** Dilatih menggunakan metode QLoRA (4-bit quantization) untuk memahami konteks instruksi dan gaya bahasa hukum Indonesia.
- **RAG System (Zero-Hallucination Focus):** Memanfaatkan vector database ChromaDB untuk mengambil konteks dari 4 dokumen UU/PP Ketenagakerjaan secara *real-time*.
- **Sitasi Otomatis:** Menyertakan nama dokumen beserta nomor halaman tempat dasar hukum ditemukan.
- **Optimasi Memori Tinggi:** Menggunakan Unsloth sehingga dapat dijalankan dan dilatih pada lingkungan dengan VRAM terbatas (misal: Kaggle GPU T4).

---

## 🛠️ Tech Stack & Library

- **Base Model:** Meta Llama 3
- **Fine-Tuning Framework:** Unsloth, PEFT (LoRA), BitsAndBytes, Hugging Face `TRL` (`SFTTrainer`)
- **RAG Architecture:** LangChain, ChromaDB, `HuggingFaceEmbeddings` (`sentence-transformers`), PyPDFLoader
- **Deployment & Model Hub:** [Hugging Face (vikriahaikal/llama3-legal-bot)](https://huggingface.co/vikriahaikal/llama3-legal-bot)
- **Environment:** Kaggle Notebook (GPU T4)

---

## 📂 Basis Dokumen Hukum (Knowledge Base)

Sistem RAG ini menggunakan dokumen resmi Ketenagakerjaan Indonesia:
1. **UU Nomor 6 Tahun 2023** (Cipta Kerja)
2. **PP Nomor 35 Tahun 2021** (PKWT, Alih Daya, Waktu Kerja, dan PHK)
3. **PP Nomor 5 Tahun 2021** (Perizinan Berusaha Berbasis Risiko)
4. **PP Nomor 51 Tahun 2023** (Pengupahan)

---

## 🚀 Cara Menjalankan (Quick Start)

### 1. Clone Repositori
```bash
git clone [https://github.com/VikriAHaikal/legal-ai-assistant-rag.git](https://github.com/VikriAHaikal/legal-ai-assistant-rag.git)
cd legal-ai-assistant-rag
