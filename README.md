# Intelligent-Telecom-Automation-System

An AI-powered Telecom Support Triage System integrated with DevOps automation using Docker, Terraform, GitHub Actions, and AWS.

---

# Project Overview

This project combines:

* Generative AI (LLM-based response generation)
* Agentic AI (decision-making triage workflow)
* DevOps (CI/CD, Docker, Terraform, AWS deployment)

The system accepts telecom-related user issues, analyzes them using AI, classifies urgency and intent, and returns structured responses.

The project also demonstrates automated cloud infrastructure provisioning and deployment using Infrastructure as Code (IaC).

---

# Features

* AI-powered telecom issue analysis
* Intent and urgency classification
* Automated ticket handling logic
* FastAPI backend deployment
* Streamlit frontend UI
* Docker containerization
* Terraform-based AWS provisioning
* GitHub Actions CI/CD pipeline
* AWS EC2 deployment
* REST API communication

---

# Tech Stack

## AI & Backend

* Python
* FastAPI
* Groq LLM API
* Pydantic

## Frontend

* Streamlit

## DevOps & Cloud

* Docker
* Terraform
* GitHub Actions
* AWS EC2
* Git & GitHub

---

# High Level Architecture

Developer pushes code to GitHub.

GitHub Actions automatically triggers the CI/CD pipeline.

Terraform provisions AWS infrastructure such as EC2 instances and security groups.

Docker containers are built and deployed on AWS.

The frontend communicates with the backend API using REST APIs.

Users access the application through the frontend interface.

---

# Project Structure

```bash
Intelligent-Telecom-Automation-System/
│
├── src/                        # Backend and frontend source code
├── terraform/                  # Terraform infrastructure files
├── .github/workflows/          # GitHub Actions CI/CD workflows
├── docs/                       # Reports and screenshots
├── Dockerfile                  # Docker configuration
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```

---

# Setup Instructions

## 1. Clone Repository

```bash
git clone https://github.com/atisha224/Intelligent-Telecom-Automation-System.git
cd Intelligent-Telecom-Automation-System
```

---

## 2. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 3. Run Backend

```bash
uvicorn src.main:app --host 0.0.0.0 --port 8000
```

Backend API:

```bash
http://localhost:8000/docs
```

---

## 4. Run Frontend

```bash
streamlit run src/ui.py
```

Frontend UI:

```bash
http://localhost:8501
```

---

# Docker Deployment

## Build Docker Image

```bash
docker build -t telecom-app .
```

## Run Docker Container

```bash
docker run -d -p 8000:8000 -e GROQ_API_KEY=YOUR_API_KEY telecom-app
```

---

# Terraform Deployment

## Initialize Terraform

```bash
terraform init
```

## Preview Infrastructure Changes

```bash
terraform plan
```

## Apply Infrastructure

```bash
terraform apply -auto-approve
```

---

# GitHub Actions CI/CD

The CI/CD pipeline automatically:

* Detects code pushes
* Initializes Terraform
* Plans infrastructure changes
* Deploys AWS resources

Workflow file:

```bash
.github/workflows/ci.yml
```

---

# API Endpoint

## POST /triage

### Sample Request

```json
{
  "message": "My internet connection is not working"
}
```

### Sample Response

```json
{
  "intent": "network_issue",
  "urgency": "high",
  "response": "Please restart your router and check cable connections."
}
```

---

# Key Outcomes

* Automated infrastructure provisioning
* Reduced manual configuration effort
* Containerized application deployment
* Cloud deployment using AWS
* Functional CI/CD implementation
* Integrated AI + DevOps workflow

---

# Future Enhancements

* Kubernetes deployment
* Load balancing
* Monitoring and logging
* Auto-scaling
* Advanced agent workflows
* Vector database integration

---

# Team Members

* Ankit Yadav
* Anshuman Geete
* Arti Jain
* Atisha Jain
* Avani Sharma
* Ishana Hatodiya

---

# Conclusion

This project demonstrates the integration of Generative AI, Agentic AI, and DevOps practices into a unified intelligent telecom automation platform. It showcases cloud deployment, CI/CD automation, infrastructure provisioning, and AI-powered issue triage in a scalable and practical workflow.
