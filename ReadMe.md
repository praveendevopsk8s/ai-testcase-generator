
# AI-Powered Test Case Generator 🧠✅

This is a lightweight, local AI tool built to help QA engineers quickly generate structured, high-quality test cases from product requirement documents.

---

## 🔍 About the Project

Creating test cases manually from requirement docs can be tedious and time-consuming. This AI-powered tool automates that process by reading requirement documents and generating well-formatted test cases that include:

- ✅ **Test Description**
- 🔄 **Steps to be Followed**
- 🎯 **Expected Results**

---

## 🚀 Features

- 📂 Upload support for `.txt`, `.pdf`, `.docx`, `.pptx`, `.csv`, and `.pcap` files
- 🧠 Uses **Llama3.2 (via Ollama)** for local LLM-powered test generation
- 📋 Generates QA-friendly test cases with step-by-step instructions and assertive expected results
- 💾 Download output as a clean `.csv` file
- 🌐 Built with **Streamlit** for a fast and simple UI

---

## 🧰 Tech Stack

- **Python**
- **Streamlit**
- **Ollama** for running `deepseek-r1` model
- **PyPDF2**, **python-docx**, **python-pptx**, **pyshark** for file handling

---

## 📦 Setup Instructions

1. Install [Ollama](https://ollama.com) and pull the model:

   ```bash
   ollama pull deepseek-r1
   ```

2. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/ai-testcase-generator
   cd ai-testcase-generator
   ```

3. Create and activate your Python environment:

   ```bash
   python -m venv venv
   source venv/bin/activate   # or venv\Scripts\activate on Windows
   ```

4. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. Run the Streamlit app:

   ```bash
   streamlit run app.py
   ```

---

## 📎 Example Use Cases

- Generate functional and regression test cases from requirement specs
- Help QA engineers kick-start test planning
- Speed up test documentation for startups or small dev teams

---

## 🛠️ Planned Improvements

- Group test cases by feature/module
- Priority/severity tagging
- Export to `.xlsx` or direct integration with test case management tools
- Switchable models (LLaMA 3.2, Claude, etc.)

---

## 🤝 Contributions & Feedback

This is an open proof-of-concept project. Contributions, issues, and suggestions are welcome!

---

## 📄 License

MIT License

---

Let's build better QA tools with AI. 💡
