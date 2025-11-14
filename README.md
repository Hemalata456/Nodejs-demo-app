**Node.js CI/CD Pipeline with GitHub Actions & Docker**

A production-style CI/CD setup for a Node.js application using GitHub Actions and Docker.
Every push to main triggers automated testing, Docker image creation, and image publishing to Docker Hub.


📌 **Key Features**

Automated CI/CD using GitHub Actions

Docker image build + push to Docker Hub


📁 Project Structure

nodejs-demo-app/
├── app.js
├── Dockerfile                 # Docker build config
├── package.json
├── .github/
│   └── workflows/
│       └── main.yml           # CI/CD workflow
└── README.md


🔄 **CI/CD Pipeline Overview**

🛠️ Workflow Stages

1. Checkout source code

2. Set up Node.js

3. Install dependencies

4. Run tests

5. Build Docker image

6. Login to Docker Hub using GitHub Secrets

7. Push image to Docker Hub


🔐 **Required GitHub Secrets**

Navigate to:
         Settings → Secrets and Variables → Actions

Add:
   | Secret Name       | Description                         |
   | ----------------- | ----------------------------------- |
   | `DOCKER_USERNAME` | Docker Hub username (`hemalata456`) |
   | `DOCKER_PASSWORD` | Docker Hub password                 |


🐳 **Docker Image**

After each successful pipeline run, the image is published to:
           docker.io/hemalata456/nodejs-demo-app


▶️ **Run Application Locally (Node)**

  npm install
  npm start

Runs at: http://localhost:3000


▶️ **Run Application Using Docker**

docker pull hemalata456/nodejs-demo-app
docker run -p 3000:3000 hemalata456/nodejs-demo-app


👤 **Author**

*Challa Hemalata*
DevOps Intern | Cloud Enthusiast

📧 hemalatach154@gmail.com
🐙 GitHub: @hemalata456