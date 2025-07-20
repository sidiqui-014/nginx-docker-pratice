

📄 Project description

🗂 Files used

🐳 Docker build & run commands

⬆ GitHub push steps (that helps to add project from terminal to git hub)

📎 Bonus .gitignore info



---

✅ README.md File:

# 🚀 Nginx Docker Practice Project

This is a simple Docker project to practice running a static index.html webpage using the *Nginx* web server in a Docker container.  
All steps were done using the Linux terminal (MobaXterm) and the project was pushed to GitHub manually using Git commands.

---

## 📁 Project Structure

mynginx-practice/ ├── index.html             # Simple static HTML file ├── nginxdockerfile        # Custom Dockerfile for Nginx └── .gitignore             # Optional file to ignore unnecessary files

---

## 🐳 Dockerfile Used

File: nginxdockerfile

Dockerfile
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html


---

🔧 Docker Commands Used

# Build Docker image
docker build -f nginxdockerfile -t mynginximage .

#-f this help to use my dockerfile instead of defaalut dockerfile 
# -t this help to name image as your image name ( as you can see above)

# Run container on port 8080
docker run -d -p 8080:80 mynginximage

# Check it's running (optional)
docker ps

# Open in browser
http://<your-ec2-ip>:8080


---

💻 Git Commands Used to Push to GitHub

# Navigate to project folder
cd ~/mynginx-practice

# Initialize git
git init

# Add all files
git add .

# Commit the files
git commit -m "Initial commit - nginx docker practice"

# Add GitHub repo (use your own URL)
git remote add origin https://github.com/yourusername/nginx-docker-practice.git

# Set branch to main and push
git branch -M main
git push -u origin main


---

📎 .gitignore File (Optional)

Added to ignore temporary files:

*.log
*.tmp
node_modules/

Commands used:

sudo vi .gitignore          # Created the file
git add .gitignore          # Staged it
git commit -m "add gitignore file"  # Committed
git push                    # Pushed to GitHub


---

✅ Output

After starting the Docker container, visiting:

http://<your-ec2-ip>:8080

...will show your custom index.html page served by Nginx.


---

✨ Purpose

This project helped in learning:

Writing a basic Dockerfile

Running containers using custom HTML

Pushing projects to GitHub using terminal commands only

#####thanks for reading ... #learning #docker #devops


