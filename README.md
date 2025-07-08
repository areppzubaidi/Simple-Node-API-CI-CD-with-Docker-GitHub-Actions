# 🚀 Simple Node API CI/CD with Docker & GitHub Actions

A beginner-friendly Node.js + Express REST API project that includes continuous integration and deployment (CI/CD) using GitHub Actions. The app is also fully containerized with Docker for local or production use.

---

## 📦 Tech Stack

| Technology     | Purpose                           |
|----------------|------------------------------------|
| Node.js        | JavaScript runtime                 |
| Express.js     | Backend web framework              |
| Docker         | Containerization                   |
| GitHub Actions | CI/CD automation                   |

---

## 🧰 Features

- ✅ Simple Express.js API (`GET /`)
- ✅ Run locally with Node.js or Docker
- ✅ Automated CI/CD pipeline using GitHub Actions
- ✅ Docker image build during CI/CD process
- ✅ Clean project structure and documentation

---

## 🗂 Project Structure

```

simple-node-api/
├── .github/
│   └── workflows/
│       └── ci-cd.yml       # GitHub Actions pipeline
├── src/
│   └── index.js            # Express app code
├── Dockerfile              # Container definition
├── .dockerignore           # Files ignored in Docker builds
├── package.json            # App dependencies and scripts
└── README.md               # Project guide

````

---

## 🚀 Getting Started

### ▶️ Run Locally (without Docker)

1. **Clone the repository**
```bash
git clone https://github.com/your-username/simple-node-api.git
cd simple-node-api
````

2. **Install dependencies**

```bash
npm install  # Install project dependencies
```

3. **Start the app**

```bash
npm start  # Starts server on http://localhost:3000
```

---

### 🐳 Run with Docker

1. **Build the Docker image**

```bash
docker build -t simple-node-api .  # Build Docker image
```

2. **Run the container**

```bash
docker run -p 3000:3000 simple-node-api  # Run app in container
```

3. **Test it**
   Open your browser or run:

```bash
curl http://localhost:3000  # Should return "Hello from GitHub Actions CI/CD!"
```

---

## 🤖 GitHub Actions CI/CD

The GitHub Actions workflow (`.github/workflows/ci-cd.yml`) will automatically:

* ✅ Checkout the code
* ✅ Install dependencies
* ✅ Run tests
* ✅ Build the Docker image
* (Optionally) push the Docker image to Docker Hub

### ✅ Trigger

```yaml
on:
  push:
    branches: [ "main" ]  # Only runs when code is pushed to main branch
```

### 🔁 Pipeline Summary

| Step                 | Description                         |
| -------------------- | ----------------------------------- |
| Checkout Code        | Pulls your source code              |
| Setup Node.js        | Installs Node 18                    |
| Install Dependencies | `npm install`                       |
| Run Tests            | `npm test` (currently dummy)        |
| Build Docker Image   | `docker build -t simple-node-api .` |

---

## 🧪 Testing

Right now, the test script is a placeholder:

```bash
npm test
```

You can replace it with real unit tests using [Jest](https://jestjs.io/).

---

## 🛠 Improvements (Optional Next Steps)

* Add Jest + Supertest for unit/integration testing
* Add automatic deployment to Render, Railway, or AWS
* Push Docker images to Docker Hub or GHCR

---

## 📸 Sample Output

```bash
> curl http://localhost:3000
🚀 Hello from GitHub Actions CI/CD!
```

