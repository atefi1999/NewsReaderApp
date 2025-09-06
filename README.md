# NewsReaderApp

A simple Python application to **manage, search, and save news articles**.  
Users can add news, list them by category, search by title, and save their favorite news.

---

## ✨ Features
- Add and remove news articles
- List all news
- Search news by title
- Filter news by category
- Save news for individual users
- Prevent duplicate news in user's saved list

---

## 🛠 Requirements
- Python 3.x  
> No external libraries are needed — only Python standard library.

---

## ▶️ Usage

### 1. Sample Run
```bash
python news_reader_app.py
```

2. Example Output
```backtick
--- News 1 ---
Title: First News
Content: This is the first news content.
Category: Politics
Author: Ali Rezaei
Date: 2025-09-04

--- News 2 ---
Title: Second News
Content: This is the second news content.
Category: Sports
Author: Maryam Ahmadi
Date: 2025-09-03

--- News 3 ---
Title: Third News
Content: This is the third news content.
Category: Politics
Author: Hossein Mohammadi
Date: 2025-09-02
```
📌 Political News:
```backtick
--- News 1 ---
Title: First News
Content: This is the first news content.
Category: Politics
Author: Ali Rezaei
Date: 2025-09-04

--- News 2 ---
Title: Third News
Content: This is the third news content.
Category: Politics
Author: Hossein Mohammadi
Date: 2025-09-02
```

✅ News found:
Title: Second News
Content: This is the second news content.
Category: Sports
Author: Maryam Ahmadi
Date: 2025-09-03

✅ News 'First News' saved for user reza.
✅ News 'Second News' saved for user reza.
ℹ️ News 'First News' is already saved.

📌 Saved news by reza:
```backtick
--- News 1 ---
Title: First News
Content: This is the first news content.
Category: Politics
Author: Ali Rezaei
Date: 2025-09-04

--- News 2 ---
Title: Second News
Content: This is the second news content.
Category: Sports
Author: Maryam Ahmadi
Date: 2025-09-03
```
---
# 📂 Project Structure
```markdown
.
├── news_reader_app.py  # Main program
└── README.md           # Project documentation
```
