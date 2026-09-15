# 🍰 Bakery Website on Docker (AWS EC2)

## 📌 Overview
This project demonstrates a production‑style workflow to deploy a static website inside a Docker container hosted on an AWS EC2 instance. It covers infrastructure setup, Docker installation, image building, and containerized deployment.

## 🚀 Steps Implemented
1. **Provision EC2 Instance**
   - Created an Ubuntu EC2 machine with security rules (port masking for controlled access).
   - Added User Data script to install Docker automatically at launch.

2. **Install & Configure Docker**
   - Verified Docker service with `systemctl status docker`.
   - Added `ubuntu` user to the Docker group for non‑root access.

3. **Prepare Website Assets**
   - Used Tooplate Sweet Bakery Template (https://www.tooplate.com/zip-templates/2168_sweet_bakery.zip).
   - Unzipped and packaged into `.tar` format.
   - Moved assets into the project directory.

4. **Build Docker Image**
   ```bash
   docker build -t bakeryimg:latest .

