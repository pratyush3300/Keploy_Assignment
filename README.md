# Book API Server

## Overview
A simple Express.js server that provides REST APIs for managing books, using MongoDB for data storage.

## Features
- **GET /books** – Retrieve all books
- **POST /books** – Add a new book
- **PUT /books/:id** – Update an existing book by ID
- **DELETE /books/:id** – Delete a book by ID

## Tech Stack
- Node.js + Express
- MongoDB + Mongoose
- HTML + JavaScript (Optional frontend)

## Setup Instructions

### 1. Prerequisites
- Node.js and npm installed
- MongoDB running locally (`mongodb://localhost:27017/bookdb`)

### 2. Installation
```bash
git clone <repo-url>
cd book-api-server
npm install
```
Create a `.env` file and add:
```
MONGO_URI=mongodb://localhost:27017/bookdb
PORT=5000
```

### 3. Run Server
```bash
node server.js
```

### 4. API Sample Requests (Use curl or Postman)
- Get Books: `curl http://localhost:5000/books`
- Add Book: `curl -X POST -H "Content-Type: application/json" -d '{"title":"1984","author":"Orwell","year":1949}' http://localhost:5000/books`
- Update Book: `curl -X PUT -H "Content-Type: application/json" -d '{"year":1950}' http://localhost:5000/books/<id>`
- Delete Book: `curl -X DELETE http://localhost:5000/books/<id>`

### 5. Frontend (Optional)
Open `public/index.html` in browser.