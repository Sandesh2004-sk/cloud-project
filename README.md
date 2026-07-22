# Sahyadri College Website Replica

A responsive front-end replica of the Sahyadri College of Engineering and Management, Mangalore website developed for educational and learning purposes. The project recreates the visual design, navigation structure, and user interface of the original website while demonstrating web development and cloud deployment skills.

> **Disclaimer:** This project is created solely for educational purposes and is not affiliated with or endorsed by Sahyadri College of Engineering and Management. All trademarks, logos, and content belong to their respective owners.

---

## Project Overview

This project demonstrates the development and deployment of a responsive college website using modern web technologies and Amazon Web Services (AWS). The website provides a clean user interface with multiple sections such as Home, About, Departments, Admissions, Placements, Campus Life, and Contact.

The project was deployed on an Amazon EC2 instance running Amazon Linux 2023 and configured with Nginx as the web server.

---

## Features

- Responsive design for desktop, tablet, and mobile devices
- Modern and attractive UI
- Navigation bar with smooth scrolling
- Hero section
- About College section
- Departments section
- Placement Highlights
- Campus Facilities
- Gallery
- Contact Information
- Footer with social links
- Fast loading pages
- Cloud deployment using AWS EC2

---

## Tech Stack

### Frontend

- HTML5
- CSS3
- JavaScript

### Cloud

- Amazon Web Services (AWS)
- Amazon EC2
- Amazon Linux 2023
- Security Groups
- Elastic IP (Optional)
- Nginx Web Server

---

## Project Structure

```
Sahyadri-Website/
│
├── index.html
├── about.html
├── admissions.html
├── departments.html
├── placements.html
├── gallery.html
├── contact.html
│
├── css/
│   ├── style.css
│   ├── responsive.css
│
├── js/
│   ├── script.js
│
├── images/
│
├── assets/
│
└── README.md
```

---

# AWS Deployment Architecture

```
User Browser
       │
       ▼
Public IP / Elastic IP
       │
       ▼
Amazon EC2 Instance
(Amazon Linux 2023)
       │
       ▼
Nginx Web Server
       │
       ▼
Website Files
(/usr/share/nginx/html)
```

---

# Prerequisites

- AWS Account
- EC2 Instance
- Amazon Linux 2023
- SSH Key Pair (.pem)
- Nginx
- Git (Optional)

---

# EC2 Setup

## Step 1

Launch an EC2 Instance

- Amazon Linux 2023
- t2.micro
- Allow HTTP
- Allow HTTPS
- Allow SSH

---

## Step 2

Connect using SSH

```bash
ssh -i your-key.pem ec2-user@YOUR_PUBLIC_IP
```

---

## Step 3

Update System

```bash
sudo dnf update -y
```

---

## Step 4

Install Nginx

```bash
sudo dnf install nginx -y
```

---

## Step 5

Start Nginx

```bash
sudo systemctl start nginx
```

Enable on boot

```bash
sudo systemctl enable nginx
```

Check status

```bash
sudo systemctl status nginx
```

---

## Step 6

Copy Website Files

```bash
sudo cp -r * /usr/share/nginx/html/
```

or

```bash
sudo cp -r ./* /usr/share/nginx/html/
```

---

## Step 7

Restart Nginx

```bash
sudo systemctl restart nginx
```

---

## Step 8

Verify Website

Open

```
http://YOUR_PUBLIC_IP
```

---

# Security Group Configuration

Inbound Rules

| Type | Port |
|-------|------|
| SSH | 22 |
| HTTP | 80 |
| HTTPS | 443 |

---

# Useful Commands

Update Server

```bash
sudo dnf update -y
```

Restart Nginx

```bash
sudo systemctl restart nginx
```

Start Nginx

```bash
sudo systemctl start nginx
```

Stop Nginx

```bash
sudo systemctl stop nginx
```

Check Status

```bash
sudo systemctl status nginx
```

View Logs

```bash
sudo journalctl -u nginx
```

Check Listening Ports

```bash
sudo ss -tulnp
```

---

# Deployment Workflow

```
Develop Website
       │
       ▼
Upload Files to EC2
       │
       ▼
Store Files
/usr/share/nginx/html
       │
       ▼
Nginx Serves Website
       │
       ▼
Accessible Through Public IP
```

---

# Learning Outcomes

Through this project, I learned:

- AWS EC2 Instance Creation
- Linux Command Line
- SSH Connectivity
- Amazon Linux Administration
- Nginx Installation and Configuration
- Web Server Deployment
- Cloud Hosting
- Security Group Configuration
- Website Deployment Process
- Static Website Hosting

---

# Future Improvements

- Add backend functionality
- Student Login Portal
- Faculty Login
- Online Admission System
- Database Integration
- CMS Dashboard
- Responsive Animations
- Dark Mode
- Contact Form Backend
- SSL using Let's Encrypt
- Domain Name Integration

---

# Author

**Sandesh Kamshetty**

Computer Science Engineering

Sahyadri College of Engineering and Management, Mangalore

GitHub: https://github.com/your-github

LinkedIn: https://linkedin.com/in/your-linkedin

---

# License

This repository is intended for educational and learning purposes only.

This project is not affiliated with or endorsed by Sahyadri College of Engineering and Management. All rights to original branding, logos, and content belong to their respective owners.
