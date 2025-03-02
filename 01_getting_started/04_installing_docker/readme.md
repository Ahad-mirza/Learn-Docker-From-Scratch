# 🐳 Docker Installation Guide

## 📖 Table of Contents
1. [📌 Introduction](#-introduction)
2. [📥 Installing Docker](#-installing-docker)
   - [🔹 Check for Existing Installations](#-check-for-existing-installations)
   - [🔹 Download Docker](#-download-docker)
   - [🔹 System Requirements](#-system-requirements)
   - [🔹 Windows-Specific Setup](#-windows-specific-setup)
   - [🔹 Verify Installation](#-verify-installation)
3. [📚 Further Reading](#-further-reading)

---

## 📌 Introduction
Docker allows you to create and manage containers efficiently. To ensure smooth operation, you should install the latest version of Docker.

---

## 📥 Installing Docker

### 🔹 Check for Existing Installations
If you have an existing Docker version installed, consider upgrading to avoid compatibility issues. Run:
```sh
docker --version
```
If the version is outdated, follow the steps below to update Docker.

### 🔹 Download Docker
Download the latest version of Docker Desktop from [Docker Hub](https://www.docker.com/products/docker-desktop/).

### 🔹 System Requirements
Before installation, verify that your system meets Docker’s requirements:
- Sufficient disk space and RAM
- Hardware virtualization enabled (for Windows/macOS)
- Compatible operating system version

### 🔹 Windows-Specific Setup
For Windows users, ensure the following features are enabled:
1. **Enable Hyper-V & Containers**:
   - Open **Turn Windows Features On or Off**.
   - Enable **Hyper-V** and **Containers**.
2. **Update Linux Kernel** (for Linux containers on Windows):
   - Follow the official guide to update the **Linux kernel**.

### 🔹 Verify Installation
After installation, verify if Docker Engine is running by executing:
```sh
docker version
```
This command should display both **client** and **server** versions.

If you face any issues, visit the [Docker Community Forums](https://forums.docker.com/) for troubleshooting.

---

🛠️ **Enjoy coding with Docker!** 🚀🐳

