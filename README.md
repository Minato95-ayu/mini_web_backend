# Aayu Language 🚀

**Aayu** is a brand new, highly readable, intent-driven programming language designed to bridge the gap between human thought and executable code.

## 🧠 How it Works

Aayu follows a clean, modern compilation pipeline:
**Human Intent** → **Aayu Code** → **AST (Abstract Syntax Tree)** → **Execution**

The language features a custom lexer, parser, and interpreter, enabling features like structured records, variable declarations, loops, error handling, and tasks (functions) in a natural syntax.

---

## 📂 Projects

### Project 4: Mini Web Backend (Pure Aayu)
This repository contains a proof-of-concept **Mini Web Backend** built entirely in **Pure Aayu** to demonstrate the language's capability to handle backend logic layers without relying on external servers or APIs.

**Features Implemented:**
- `Student` entity records for modeling data.
- Deep modularization using Aayu's `use` keyword across multiple files (`models`, `api`, `database`, `auth`).
- Backend Business Logic (Validation, Routing abstraction).
- File Storage abstraction via Aayu's `write` statement.

#### Example: `api.aayu`
```aayu
task create_student with student.
    show "Student Created".
end.

task get_student with id.
    show "Student Found".
end.
```

#### Example: `main.aayu`
```aayu
use models.
use api.
use database.
use auth.

run login.

show "Backend Started".

Student student1 is.
    name "Rahul"
    age 20
    id 1
end.

run create_student with student1.
run save_student with student1.
```

---

## 🚀 Running the Project

Ensure you have Python installed and the Aayu interpreter available. Run the `main.aayu` file from the interpreter root:

```bash
python run.py mini_web_backend/main.aayu
```

**Expected Output:**
```text
Login Success
Backend Started
Student Created
```

*(Note: The program will also write the student data to `students.txt` as handled by the `database.aayu` layer.)*

---

## 🛠️ Future Roadmap (Phase 2)

Aayu is rapidly evolving! The next steps for the language include:
1. **Building more Real-World Projects:**
   - Intent Driven Library Generator (Project 5)
2. **Aayu Specification v1.0:** Freezing the syntax and features.
3. **VS Code Extension:** Adding official syntax highlighting and IntelliSense for `.aayu` files.
4. **GitHub Linguist PR:** Registering Aayu as an official GitHub language!