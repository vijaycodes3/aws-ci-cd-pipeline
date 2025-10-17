# Automated CI/CD Pipeline
This project implements a **CI/CD pipeline using Jenkins, Docker, and Kubernetes** to deploy a Node.js web app on AWS.

**Technologies Used:** Jenkins, Docker, Kubernetes, AWS EC2  
**Highlights:**
- Automated build, test, and deployment.
- Containerized Node.js app using Docker.
- Kubernetes used for orchestration with a LoadBalancer.

**How to Run:**
1. Clone repo  
2. Build Docker image → `docker build -t vijay-node-app .`  
3. Deploy → `kubectl apply -f k8s/`  
