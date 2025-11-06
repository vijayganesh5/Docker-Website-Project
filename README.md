# 🐳 Dockerized Personal Info Website

### **Task Description**

Create a simple web page that displays your basic details and run it inside a Docker container using **Docker Compose** on an **AWS EC2 (Ubuntu)** instance.

---

## 🚀 Tech Stack

* **AWS EC2 (Ubuntu)** — Cloud virtual machine
* **Docker** — To containerize the web application
* **Docker Compose** — To manage and run containers easily
* **Nginx** — To serve the webpage

---

## 🧩 Project Structure

```
mywebsite/
│
├── Dockerfile
├── docker-compose.yml
└── index.html
```

---

## 📜 Files Explanation

### **index.html**

Simple web page displaying your personal information.

```html
<h1>Hello, I’m Vijay Ganesh</h1>
<p>VFX Artist & DevOps Learner</p>
```

---

### **Dockerfile**

Defines how the Docker image is built.

```dockerfile
# Use an official Nginx image
FROM nginx:alpine

# Copy the HTML file into the Nginx web directory
COPY index.html /usr/share/nginx/html/index.html
```

---

### **docker-compose.yml**

Specifies how to run the container.

```yaml
version: '3'
services:
  web:
    build: .
    ports:
      - "80:80"
```

---

## 🛠️ Setup Instructions

### **1️⃣ Connect to EC2 Instance**

```bash
ssh -i your-key.pem ubuntu@your-ec2-public-ip
```

### **2️⃣ Install Docker and Docker Compose**

```bash
sudo apt update
sudo apt install -y docker.io docker-compose
sudo systemctl enable docker
sudo systemctl start docker
```

### **3️⃣ Clone or Create Project Folder**

```bash
mkdir mywebsite && cd mywebsite
```

### **4️⃣ Create the Project Files**

Create the `index.html`, `Dockerfile`, and `docker-compose.yml` as shown above.

---

## ▶️ Run the Application

```bash
sudo docker-compose up --build -d
```

---

## 🌐 Access the Website

Open your browser and visit:

```
http://<your-ec2-public-ip>
```

You should see your personal details displayed on the webpage.

---

## 🧹 Stop & Clean Up

```bash
sudo docker-compose down
```

---

## 📘 Summary

This project demonstrates how to:

* Launch and use an EC2 instance
* Create and build a Docker image using Nginx
* Use Docker Compose to deploy a simple static website
* Access the hosted page via your EC2’s public IP

---

## 🎉 Output Link with Screenshots:
- https://docs.google.com/document/d/1GjZEoWpF1V64sTmSE7ZMOu9OyQan9CipEOX925zoyHA/edit?usp=sharing

---
