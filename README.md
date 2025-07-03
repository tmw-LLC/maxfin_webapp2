 **Markdown guide** including how to **build the image directly with the desired name** and **push to Docker Hub**, without needing to tag it after building:

````markdown
# 🚀 Build, Tag, and Push Docker Image to Docker Hub

This guide walks you through building a Docker image directly with your Docker Hub tag (`etumoses/maxfin-webapp:latest`) and pushing it.

---

## 📦 Target Image Name

```text
docker.io/etumoses/maxfin-webapp:latest
````

---

## ✅ Step-by-Step Instructions

### 1. Build the Image with Desired Name

```bash
docker build -t etumoses/maxfin-webapp:latest .
```

> `-t` specifies the tag (name\:tag), and `.` indicates the Dockerfile is in the current directory.

---

### 2. Login to Docker Hub

```bash
docker login
```

Enter your Docker Hub **username** (`etumoses`) and **password** or **access token**.

---

### 3. Push the Image to Docker Hub

```bash
docker push etumoses/maxfin-webapp:latest
```

> This uploads the image to your Docker Hub repository.

---

### ✅ Verify Upload

Go to:

```
https://hub.docker.com/repository/docker/etumoses/maxfin-webapp
```

You should see the image there with the `latest` tag.

---

## 🧼 (Optional) Cleanup Local Image

To delete the image locally after pushing:

```bash
docker rmi etumoses/maxfin-webapp:latest
```

---
