# 🐳 Docker in Action

## 📖 Table of Contents
1. [📌 Introduction](#-introduction)
2. [🛠 Setting Up the Environment](#-setting-up-the-environment)
3. [📝 Writing a Dockerfile](#-writing-a-dockerfile)
4. [🚀 Building and Running the Container](#-building-and-running-the-container)
5. [📦 Pushing to Docker Hub](#-pushing-to-docker-hub)
6. [📚 Further Reading](#-further-reading)

---

## 📌 Introduction
Docker allows developers to **package and distribute applications** efficiently. Instead of manually setting up environments, we can create **Docker images** and deploy them anywhere with ease.

---

## 🛠 Setting Up the Environment

1. **Create a new directory** for the project:
   ```sh
   mkdir hello-docker && cd hello-docker
   ```
2. **Open in VS Code**:
   ```sh
   code .
   ```
3. **Install the recommended Docker extensions** (optional but helpful).

---

## 📝 Writing a Dockerfile
A **Dockerfile** is a script that defines the environment for our application. It includes the **OS, dependencies, and runtime**.

1. **Create a file named `Dockerfile`** (no extension, case-sensitive `D` uppercase):
   ```sh
   touch Dockerfile
   ```
2. **Add the following content to the Dockerfile:**
   ```dockerfile
   # Use an official lightweight Node.js image
   FROM node:alpine

   # Set the working directory inside the container
   WORKDIR /app

   # Copy package.json and install dependencies
   COPY package.json .
   RUN npm install

   # Copy the rest of the application files
   COPY . .

   # Expose port 3000
   EXPOSE 3000

   # Command to run the app
   CMD ["node", "app.js"]
   ```

---

## 🚀 Building and Running the Container
1. **Build the Docker image**:
   ```sh
   docker build -t my-app .
   ```
2. **Run the container**:
   ```sh
   docker run -p 3000:3000 my-app
   ```

---

## 📦 Pushing to Docker Hub
1. **Log in to Docker Hub**:
   ```sh
   docker login
   ```
2. **Tag the image for Docker Hub**:
   ```sh
   docker tag my-app username/hello-docker
   ```
3. **Push the image**:
   ```sh
   docker push username/hello-docker
   ```

---

🚀 **Now, let’s take Docker into action!** 🐳

