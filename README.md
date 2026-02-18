
---

# 🐹 Web Service API with Gin (Go)

A simple RESTful web service built using **Go** and the **Gin web framework**.  
This project demonstrates how to:

- Build a lightweight HTTP API server  
- Implement REST endpoints (GET, POST, dynamic routes)  
- Structure backend services using Go modules  
- Work with JSON request/response bodies  

This project is ideal for learning **Go web development fundamentals**.

---

## 🎯 Learning Objectives

By working through this project, you will learn:

- How to build REST APIs using Gin
- How to define routes and handlers
- How to handle JSON requests and responses
- How to use Go modules for dependency management
- How to structure a basic backend web service

---

## 📁 Project Structure

- web-service-gin/
  - go.mod
  - go.sum
  - main.go
  - README.md

---

## ⚙️ Prerequisites

Make sure you have the following installed:

| Tool | Purpose |
|------|----------|
| Go | Go compiler & runtime |
| Git | Version control |
| Curl / Postman | API testing |

---

## 🦫 Installing Go

### Step 1: Check if Go is installed

```bash
go version
```

Step 2: Install Go (if missing)

Linux / macOS:
```bash
curl -OL https://go.dev/dl/go1.22.0.linux-amd64.tar.gz
sudo tar -C /usr/local -xvf go1.22.0.linux-amd64.tar.gz
export PATH=$PATH:/usr/local/go/bin
```

Windows:
```bash
https://go.dev/dl/
```

---

## 🚀 Getting Started
Step 1: Clone the Repository
```bash
git clone https://github.com/skipajenkins/web-service-gin.git
cd web-service-gin
```
---
Step 2: Install Dependencies
```bash
go mod tidy
```
---
Step 3: Run the Server
```bash
go run main.go
```

You should see:
```bash
Listening and serving HTTP on localhost:8080
```

---

## 🌐 API Endpoints

| Method | Endpoint      | Description        |
|---------|---------------|--------------------|
| GET     | /albums       | Fetch all albums  |
| GET     | /albums/:id   | Fetch album by ID |
| POST    | /albums       | Add a new album   |


---

## 🧠 Key Concepts

| Concept            | Explanation                                     |
|---------------------|-------------------------------------------------|
| Go Modules          | Dependency management using `go.mod`            |
| Gin Framework       | Lightweight web framework for APIs              |
| REST API            | HTTP-based service architecture                 |
| Routing             | Mapping URLs to handler functions               |
| JSON Binding        | Automatic JSON request parsing                  |
| HTTP Status Codes   | Standard response signaling                     |


---

## 📌 Example Requests
Fetch All Albums
```bash
curl http://localhost:8080/albums
```
---
Fetch Album by ID
```bash
curl http://localhost:8080/albums/2
```
---
Add New Album
```bash
curl -X POST http://localhost:8080/albums \
  -H "Content-Type: application/json" \
  -d '{"id":"4","title":"Kind of Blue","artist":"Miles Davis","price":42.99}'
```

---

## 🧱 How It Works

1.Gin initializes the router
```bash
router := gin.Default()
```

2.Routes are defined
```bash
router.GET("/albums", getAlbums)
router.POST("/albums", postAlbums)
```

3.Handlers process requests and return JSON
```bash
c.IndentedJSON(http.StatusOK, albums)
```

4.Server listens on port 8080
```bash
router.Run("localhost:8080")
```

---

## 🧩 Example Output
```bash
[
  {
    "id": "1",
    "title": "Blue Train",
    "artist": "John Coltrane",
    "price": 50.99
  }
]
```

---

## 🏗️ Built With

* Go (Golang)

* Gin Web Framework

* Go Modules

* REST Architecture

---

## 📜 License

This project is licensed under the MIT License — free to use, modify, and distribute.

---
