
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

===============================================
Creating Docker image and running the container
AT first build the Docker image with command:
# sudo docker build -t .
or
# sudo docker build -t testcasegen .

Now run the image to get the container:
# sudo docker run -d -p 8501:8501 --name testcasegen <container ID>
or 
# sudo docker run -d -p 8501:8501 --name testcasegen testcasegen 

Now tag and push to the Dockerhub:
# sudo docker login -u praveendevopsk8s
enter the password

Tag the image:
# sudo docker tag testcasegen praveendevopsk8s/testcasegen:latest 

Now push to the Dockerhub:
# sudo docker push praveendevopsk8s/testcasegen:latest 

https://hub.docker.com/repository/docker/praveendevopsk8s/testcasegen/tags

Now pull the image from the Dockerhub and run it
# sudo docker pull praveendevopsk8s/testcasegen:latest 

Running the image:
# sudo docker run -d -p 8501:8501 --name testcase gen praveendevopsk8s/testcasegen:latest 

Currently we have some issue with the container, Ollama is NOT working correctly, so must perform these steps inside the container:

**Run an interactive session in the container:**
# sudo docker exec -it testcase bash


**Then, check if ollama is running:
ps aux | grep ollama

If it's not running, start it manually:
ollama serve &


Then, try running a basic prompt:
ollama run deepseek-r1 "Hello, what is 2+2?"


After above operations second time click it got the results**
