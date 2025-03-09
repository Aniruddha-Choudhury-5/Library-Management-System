Library Management System: 
This is a Flask-based Library Management System that organizes books into categories using a graph-based data structure. It allows users to add categories, add books, list books, and search for books efficiently.

Features
✅ Add book categories dynamically
✅ Add books under specific categories
✅ List all books in the library
✅ Search for books by title
✅ Implements linked lists for book storage and graph-based management
✅ Simple Flask API with JSON responses

Tech Stack
Backend: Python (Flask)
Data Structures: Graph, Linked List, Queue (Waitlist)
Frontend (Optional): HTML + CSS (index.html)


Setup & Installation
Clone the repository:
bash
Copy
Edit
git clone https://github.com/yourusername/library-management.git
cd library-management
Install dependencies:
bash
Copy
Edit
pip install flask
Run the application:
bash
Copy
Edit
python app.py
Open your browser and go to:
cpp
Copy
Edit
http://127.0.0.1:5000/
API Endpoints
Method	Endpoint	Description
GET	/	Renders homepage (index.html)
POST	/add-category	Adds a new book category
POST	/add-book	Adds a book to a category
GET	/list-books	Lists all books in the library
GET	/search-books?query=<title>	Searches for books by title


Future Enhancements
🔹 User authentication system
🔹 Borrow/return books with availability tracking
🔹 UI improvements with React/Bootstrap

Contributions & suggestions are welcome! 🚀
