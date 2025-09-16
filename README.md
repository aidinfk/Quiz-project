# 🧩 Python OOP Quiz Application

A **console-based quiz application** built with **Python** to showcase the power of **Object-Oriented Programming (OOP)** in practice.  
This project allows you to create unlimited quiz questions, store them in a structured Python dictionary, and run a fully interactive quiz in the console.

---

## 🚀 Features
- ✅ Object-Oriented design for scalability and maintainability  
- ✅ Unlimited question creation with flexible structure  
- ✅ Questions stored in `data.py` as a dictionary  
- ✅ Easy integration with [Open Trivia Database](https://opentdb.com/) for automatic question generation  
- ✅ Minimal configuration required in `main.py` to adapt to new question formats  

---

## 📂 Project Structure
📦 quiz-app
┣ 📜 main.py # Entry point of the application
┣ 📜 question_model.py # Defines the Question class (OOP)
┣ 📜 quiz_brain.py # Quiz logic and flow
┣ 📜 data.py # Question data (custom or from API)
┗ 📜 README.md # Project documentation


---

## 🛠️ How It Works
1. **Define your questions** inside `data.py` in a dictionary/array structure:
   ```python
   question_data = [
       {"text": "The Earth is flat.", "answer": "False"},
       {"text": "Python is an interpreted language.", "answer": "True"}
   ]

2. In main.py, the quiz logic builds a question_bank using a loop:
question_bank = []
for question in question_data:
    question_text = question["text"]      # 👈 Change this if key name differs
    question_answer = question["answer"]  # 👈 Change this if key name differs
    new_question = Question(question_text, question_answer)
    question_bank.append(new_question)

🔑 Important: 
If your data.py uses different keys, just update
question["text"] and question["answer"] accordingly

3. Run the quiz:
python main.py

