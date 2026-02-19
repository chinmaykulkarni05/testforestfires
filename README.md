# WildfireIQ (previously named as testforestfires)
- WildfireIQ is a production-ready Machine Learning application that predicts forest fire risk using regression models.
- The project demonstrates the complete ML lifecycle — from data preprocessing and model selection to cloud deployment using AWS CI/CD pipelines.
- The system is deployed on AWS Elastic Beanstalk and supports automated deployments via AWS CodePipeline integrated with GitHub Webhooks.

# Live Demo
Application URL: (Add your Elastic Beanstalk URL here)

# ⚙️ Setup & Deployment Guide
1️⃣ Local Development Setup
step 1 : python -m venv environment (Create Folder & Create Virtual Environment)
step 2 : environment\Scripts\activate  (Activate Virtual Environment)
step 3 : pip install -r requirements.txt (Install dependencies)
step 4 : python application.py  (run the application)

2️⃣ Push Project to GitHub
step 1 : git init
step 2 : git add .
step 3 : git commit -m "Initial commit - End-to-End ML Deployment"
step 4 : git remote add origin https://github.com/your-username/WildfireIQ.git
step 5 : git branch -M main
step 6 : git push -u origin main

3️⃣ AWS Deployment Guide
This project is deployed using: AWS Elastic Beanstalk, AWS CodePipeline, GitHub Webhooks
Part A: Create Elastic Beanstalk Application
step 1 : Login to AWS Console
step 2 : Search for Elastic Beanstalk
step 3 : Click Create Application
step 4 : Application Name: WildfireIQ
step 5 : Platform: Python
step 6 : Platform Branch: Python 3.8 running on 64-bit Amazon Linux 2
step 7 : Platform Version: Recommended
step 8 : Application Code: Choose Sample Application
step 9 : Click Create
Wait until environment status becomes Healthy

Part B: Create AWS CodePipeline
step 1 : Go to AWS Console
step 2 : Search for CodePipeline
step 3 : Click Create Pipeline
step 4 : Pipeline Name: wildfireiq-pipeline
step 5 : Leave default settings → Click Next

Source Stage
step 1 : Source Provider: GitHub (Version 1)
step 2 : Connect to GitHub
step 3 : Select Repository
step 4 : Branch: main
step 5 : Change Detection: GitHub Webhooks
step 6 : Click Next

Build Stage
Skip Build Stage (for now)
Click Next

Deploy Stage
step 1 : Deploy Provider: AWS Elastic Beanstalk
step 2 : Region: (Your region, e.g., Mumbai)
step 3 : Application Name: WildfireIQ
step 4 : Environment Name: WildfireIQ-env
step 5 : Click Next → Create Pipeline

Access Application
After deployment:
step 1 : Go to Elastic Beanstalk
step 2 : Click on your Environment
step 3 : Click on the Application URL
step 4 : Enter input values
step 5 : Click Predict
step 6 : Get real-time forest fire risk prediction
