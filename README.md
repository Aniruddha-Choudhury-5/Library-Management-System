Library Management System
A web-based library management system implementing various Data Structures and Algorithms (DSA) concepts for efficient book tracking, user management, and library operations.
Features
1. Book Management

Data Structure Used: AVL Tree

Self-balancing binary search tree for storing book records
O(log n) time complexity for insertions, deletions, and searches
Books are indexed by ISBN for quick retrieval
Maintains balance factor to ensure optimal performance



2. User Management

Data Structure Used: Hash Table

Constant time O(1) lookup for user information
Handles user authentication and profile management
Implements chaining for collision resolution
Dynamic resizing when load factor exceeds threshold



3. Borrowing System

Data Structure Used: Queue

FIFO structure for managing book reservations
Implements waiting list for popular books
Priority queue for handling special user requests
O(1) time complexity for enqueue and dequeue operations



4. Search Functionality

Data Structure Used: Trie

Efficient prefix-based search for book titles and authors
Supports autocomplete suggestions
Space-efficient storage of book metadata
O(m) time complexity for searches, where m is the length of the search string



Technical Architecture
Frontend

React.js for building the user interface
Tailwind CSS for styling
Redux for state management
Axios for API communication

Backend

Node.js with Express
MongoDB for persistent storage
JWT for authentication
RESTful API architecture

API Endpoints
Books
CopyGET    /api/books          - Get all books
POST   /api/books          - Add new book
GET    /api/books/:id      - Get book by ID
PUT    /api/books/:id      - Update book
DELETE /api/books/:id      - Delete book
GET    /api/books/search   - Search books
Users
CopyPOST   /api/users/register - Register new user
POST   /api/users/login    - User login
GET    /api/users/profile  - Get user profile
PUT    /api/users/profile  - Update profile
Borrowing
CopyPOST   /api/borrow/:bookId - Borrow book
POST   /api/return/:bookId - Return book
GET    /api/borrowed       - Get borrowed books
Installation

Clone the repository:

bashCopygit clone https://github.com/yourusername/library-management.git
cd library-management

Install dependencies:

bashCopy# Install backend dependencies
cd backend
npm install

# Install frontend dependencies
cd ../frontend
npm install

Configure environment variables:

bashCopy# Backend .env
PORT=5000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret

# Frontend .env
REACT_APP_API_URL=http://localhost:5000/api

Start the application:

bashCopy# Start backend server
cd backend
npm run dev

# Start frontend application
cd frontend
npm start
Data Structure Implementation Details
AVL Tree for Book Management
javascriptCopyclass AVLNode {
    constructor(book) {
        this.book = book;
        this.height = 1;
        this.left = null;
        this.right = null;
    }
}

class AVLTree {
    constructor() {
        this.root = null;
    }

    // Core operations
    insert(book) { /* Implementation */ }
    delete(isbn) { /* Implementation */ }
    search(isbn) { /* Implementation */ }
    
    // Helper methods
    getHeight(node) { /* Implementation */ }
    getBalance(node) { /* Implementation */ }
    rotateRight(y) { /* Implementation */ }
    rotateLeft(x) { /* Implementation */ }
}
Hash Table for User Management
javascriptCopyclass HashTable {
    constructor(size = 53) {
        this.keyMap = new Array(size);
    }

    _hash(key) { /* Implementation */ }
    set(key, value) { /* Implementation */ }
    get(key) { /* Implementation */ }
    resize() { /* Implementation */ }
}
Performance Considerations

Time Complexity

Book Search: O(log n)
User Lookup: O(1) average case
Borrowing Operations: O(1)
Search Suggestions: O(m) where m is query length


Space Complexity

AVL Tree: O(n) where n is number of books
Hash Table: O(m) where m is number of users
Trie: O(k) where k is total length of all strings



Contributing

Fork the repository
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request

License
This project is licensed under the MIT License - see the LICENSE file for details.
Testing
Run tests using:
bashCopy# Backend tests
cd backend
npm test

# Frontend tests
cd frontend
npm test
Support
For support, please open an issue in the GitHub repository or contact the maintainers at support@librarymanagement.com.Last edited just now