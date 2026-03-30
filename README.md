# 🚀 On-Screen Marking Backend System

> A **scalable, schema-driven evaluation platform** that enables **question-wise assessment of answer sheets** using coordinate-based PDF processing and asynchronous workflows.

---

## 🔥 Why This Project Stands Out

- ⚡ **Question-wise evaluation (not full PDF)** using coordinate mapping  
- 🚀 **Zero-wait experience** via background processing (Bull Queue)  
- 🧠 **Schema-driven architecture** for flexible subject configurations  
- 👥 **Role-based workflow** (Admin → Evaluator → Reviewer → Principal)  
- 📄 **Dynamic PDF generation** with annotations, marks, and comments  

---

## 🧠 Core Idea

Instead of evaluating entire answer sheets, this system:

👉 Extracts **only the required question areas** from PDFs  
👉 Uses **predefined coordinates + page mapping**  
👉 Ensures faster evaluation and better performance  

---

## 🏗️ Tech Stack

- **Backend**: Node.js (Express)
- **Database**: MongoDB
- **Queue System**: Bull (Redis)
- **Image Processing**: Sharp
- **Cloud Storage**: Tencent Cloud (COS/VOD)

---

## ⚙️ High-Level Workflow

```text
Upload Answer PDF
        ↓
Assign Task (Admin)
        ↓
Push Job to Queue (Bull)
        ↓
Background Processing (Worker)
        ↓
PDF → Images Conversion
        ↓
Coordinate-based Extraction (Question-wise)
        ↓
Evaluator Marks Answers
        ↓
Reviewer Validates
        ↓
Final Annotated PDF Generated

```
