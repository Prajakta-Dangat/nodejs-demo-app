# Node.js CI/CD Demo Application

A simple Node.js web application demonstrating CI/CD automation using GitHub Actions, Docker, and Docker Hub.

## 🚀 Technologies Used

- Node.js
- Docker
- Git
- GitHub
- GitHub Actions
- Docker Hub

## 📁 Project Structure

```text
nodejs-demo-app/
│
├── .github/
│   └── workflows/
│       └── main.yml
│
├── app.js
├── Dockerfile
├── package.json
├── package-lock.json
├── .gitignore
└── README.md
```

## ⚙️ Application

This project contains a simple Node.js web application running on port `3000`.

To run the application locally:

```bash
npm install
npm start
```

Open the application in your browser:

```text
http://localhost:3000
```

## 🧪 Run Tests

The project includes a basic test command to check the JavaScript syntax.

Run:

```bash
npm test
```

## 🐳 Docker

### Build Docker Image

```bash
docker build -t nodejs-demo-app .
```

### Run Docker Container

```bash
docker run -d -p 3000:3000 --name nodejs-demo-container nodejs-demo-app
```

Open:

```text
http://localhost:3000
```

### Check Running Container

```bash
docker ps
```

### Stop Container

```bash
docker stop nodejs-demo-container
```

## 🔄 CI/CD Pipeline

GitHub Actions automatically runs the CI/CD pipeline whenever code is pushed to the `main` branch.

### Pipeline Workflow

```text
Developer
    ↓
Git Push
    ↓
GitHub Repository
    ↓
GitHub Actions
    ↓
Checkout Code
    ↓
Setup Node.js
    ↓
Install Dependencies
    ↓
Run Tests
    ↓
Login to Docker Hub
    ↓
Build Docker Image
    ↓
Push Docker Image
    ↓
Docker Hub
```

## ⚙️ GitHub Actions

The CI/CD workflow is located at:

```text
.github/workflows/main.yml
```

The workflow performs the following tasks:

1. Checks out the source code.
2. Sets up Node.js.
3. Installs project dependencies.
4. Runs tests.
5. Logs in to Docker Hub.
6. Builds the Docker image.
7. Pushes the Docker image to Docker Hub.

## 🔐 GitHub Secrets

Docker Hub authentication is handled securely using GitHub Repository Secrets.

Required secrets:

```text
DOCKER_USERNAME
DOCKER_PASSWORD
```

`DOCKER_USERNAME` contains the Docker Hub username.

`DOCKER_PASSWORD` contains the Docker Hub Personal Access Token.

Sensitive credentials are not stored directly inside the workflow file.

## 📦 Docker Image

The Docker image is automatically built and pushed to Docker Hub.

Image format:

```text
YOUR_DOCKER_USERNAME/nodejs-demo-app:latest
```

Replace `YOUR_DOCKER_USERNAME` with your Docker Hub username.

## 🎯 Project Objective

The main objective of this project is to understand and implement a basic CI/CD pipeline using:

- Node.js
- Git
- GitHub
- GitHub Actions
- Docker
- Docker Hub

The project demonstrates how application code can be tested, containerized, and published automatically using GitHub Actions.

## 📚 Key Learning

Through this project, I explored:

- Node.js application setup
- npm commands
- Git and GitHub
- Dockerfile creation
- Docker image building
- Docker container execution
- GitHub Actions workflows
- CI/CD automation
- GitHub Secrets
- Docker Hub image publishing

## 🔄 CI/CD Process

The complete CI/CD process is:

```text
Code Change
    ↓
Git Commit
    ↓
Git Push
    ↓
GitHub
    ↓
GitHub Actions Triggered
    ↓
Install Dependencies
    ↓
Run Tests
    ↓
Build Docker Image
    ↓
Login to Docker Hub
    ↓
Push Image
    ↓
Docker Hub
```

## 📌 Important Files

### `app.js`

Contains the Node.js web application.

### `package.json`

Contains project information, dependencies, and npm scripts.

### `Dockerfile`

Contains instructions for creating the Docker image.

### `.github/workflows/main.yml`

Contains the GitHub Actions CI/CD workflow.

### `.gitignore`

Specifies files and folders that should not be committed to Git.

### `README.md`

Contains project documentation and instructions.

## 🛠️ Useful Commands

### Git Commands

```bash
git status
git add .
git commit -m "Update project"
git push
```

### Node.js Commands

```bash
npm install
npm test
npm start
```

### Docker Commands

```bash
docker build -t nodejs-demo-app .
docker images
docker ps
docker run -d -p 3000:3000 --name nodejs-demo-container nodejs-demo-app
docker stop nodejs-demo-container
docker rm nodejs-demo-container
```

## ✅ Project Outcome

After completing this project:

- The Node.js application runs successfully.
- The application is containerized using Docker.
- GitHub Actions automatically runs tests.
- GitHub Actions builds the Docker image.
- The Docker image is pushed automatically to Docker Hub.
- Docker Hub stores the published image.

## 👩‍💻 Author

**Prajakta Dangat**

BTech E&TC Engineering

## 📄 License

This project is created for learning and educational purposes.
