# Applicant Tracking System (ATS)

This simple Python-based program leverages Natural Language Processing (NLP) and Machine Learning (ML) to evaluate resumes against job descriptions. By analyzing the content, it assigns a score ranging from 0 to 5, indicating how well the resume aligns with the job description. I used this project to learn simple NLP concepts and experiment with libraries.

---

## **Code Breakdown**

### **1. PDF to Text Conversion**
- Utilizes the `pdfminer` module to convert PDF files (job description and resume) into plain text for further processing.

### **2. Preprocessing Text**
- **Stopword Removal**: Commonly used words like "the," "and," or "yours" are removed using the `nltk` module to avoid skewing results.
- **Lemmatization**: Converts words to their root forms (e.g., "engineered" → "engineer," "crafting" → "craft") for consistency between the job description and resume.

### **3. Extracting Keywords**
- Implements the `tf-idf` algorithm from the `sklearn` module to identify and extract keywords from both the resume and the job description. These keywords are critical for the matching process.

### **4. Keyword Matching**
- A custom algorithm matches the extracted keywords from the job description to those in the resume.
- Returns a match percentage, representing how well the resume aligns with the job description based on keyword similarity.

### **5. Score Creation**
- **Training**: The program uses sample resumes categorized as strong or weak fits for the job to train itself on scoring criteria.
- **Percentage Transformation**: Transforms the generated percentage on a log scale and then normalizes them to a scale from 1-5.

---

This system simplifies the evaluation process, providing a structured and efficient way to match resumes with job descriptions using simple NLP and ML techniques.
