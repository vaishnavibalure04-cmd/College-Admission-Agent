# College-Admission-Agent
# 🎓 College Admission Agent – RAG-Based AI (IBM Cloud)

This project implements a **Retrieval-Augmented Generation (RAG)-based AI assistant** to simplify the **college admission process** using IBM Watsonx, Object Storage, and vector databases.

---

## 📘 Project Summary

Navigating college admissions can be overwhelming due to scattered and unclear information. This AI assistant helps students retrieve reliable admission-related details — such as eligibility criteria, fee structures, application dates, and procedures — using natural language queries, powered by IBM Watsonx.

---

## 🚀 Technologies Used

- **🧠 Generative AI**: IBM Watsonx.ai (Agent Lab + Prompt Lab)
- **🗂 Document Storage**: IBM Cloud Object Storage
- **📊 Vector Database Options**:
  - In-memory (default)
  - Milvus
  - Elasticsearch
- **🐍 Data Preprocessing**: Python (Jupyter Notebook)
- **📚 RAG (Retrieval-Augmented Generation)**: For document-grounded question answering

---

## 🧾 Steps to Run the Agent on IBM Cloud

### 🔹 1. Set up IBM Cloud

- Log into [IBM Cloud](https://cloud.ibm.com)
- Enable the **Lite Plan** for Watsonx
- Launch **Watsonx.ai**

---

### 🔹 2. Prepare Documents

Use the `create_admission_documents.ipynb` notebook to generate `.txt` files.

Sample files include:
- `eligibility_criteria.txt`
- `fee_structure.txt`
- `how_to_apply.txt`
- `important_dates.txt`

> 📌 Make sure each file is under **5MB** (TXT file size limit).

---

### 🔹 3. Upload Files to Watsonx Agent Lab

1. Navigate to: **Watsonx → Projects → Agent Lab**
2. Click **New Agent**
3. Choose: **Ground gen AI with vectorized documents**
4. Under “Add files”:
   - Upload the generated `.txt` documents
5. Define a **vector index name** (e.g., `admission_info_vector`)
6. Choose either:
   - **In-memory**
   - or connect to **Milvus / Elasticsearch**

---

### 🔹 4. Configure Prompt

Use a simple and effective prompt in Prompt Lab like:

> “Use only the uploaded documents to answer questions about college admissions. Be concise, factual, and student-friendly.”

Example enhanced prompts:
- “List the eligibility criteria for each course based on uploaded documents.”
- “What is the fee for BBA and MBA programs?”
- “Summarize the application process using the given data.”

---

### 🔹 5. Test and Deploy

Ask natural questions to test:
- “What is the fee for MBA?”
- “When does admission start?”
- “How to apply for B.Tech?”
- “Are scholarships available for SC/ST students?”

Then click:
- **Deploy → Web App / API** to share or integrate it.

---

## 🔍 Example Questions

- ✅ “What is the last date for admission?”
- ✅ “What is the eligibility for M.Tech?”
- ✅ “Are there scholarships for reserved categories?”
- ✅ “How can I apply for the BCA course?”

---

## 🛠 Troubleshooting

| Problem                            | Solution                                                                 |
|------------------------------------|--------------------------------------------------------------------------|
| File upload fails                  | Ensure TXT files are under 5MB limit. Split large documents if needed.  |
| Irrelevant or empty responses      | Check if the correct vector index and documents are attached.            |
| Agent not recognizing documents    | Re-upload files and confirm they were indexed successfully.              |

---

## 📦 File & Usage Notes

- **Supported formats**: `.txt`, `.pdf`, `.docx`  
- **Size limits**:
  - TXT: 5MB
  - PDF / DOCX: 50MB
- **IBM Lite plans** come with usage restrictions (runtime, storage, calls)
- You can **update the assistant in real-time** by replacing documents in the vector index.

---


---

## 🙋‍♀️ Author
Vaishnavi Balure
Project under [SB4Academia Challenge 2025]  
GS Moze College of Engineering, Balewadi, India

---

## 📄 License

This project is for **educational use only**. Contact the author for any reuse, modification, or deployment beyond academic purposes.




