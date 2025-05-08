# 30 Days DevOps Challenge - Weather Dashboard

Day 1: Building a weather data collection system using AWS S3 and OpenWeather API

# Weather Data Collection System - DevOps Day 1 Challenge

## Project Overview
This project is a Weather Data Collection System that demonstrates core DevOps principles by combining:
- External API Integration (OpenWeather API)
- Cloud Storage (AWS S3)
- Infrastructure as Code
- Version Control (Git)
- Python Development
- Error Handling
- Environment Management

## Features
- Fetches real-time weather data for multiple cities
- Displays temperature (°F), humidity, and weather conditions
- Automatically stores weather data in AWS S3
- Supports multiple cities tracking
- Timestamps all data for historical tracking

## Technical Architecture
- **Language:** Python 3.x
- **Cloud Provider:** AWS (S3)
- **External API:** OpenWeather API
- **Dependencies:** 
  - boto3 (AWS SDK)
  - python-dotenv
  - requests

```markdown
## Project Structure
weather-dashboard/
  src/
    __init__.py
    weather_dashboard.py
  .env
  .gitignore
  requirements.txt

## Setup Instructions
1. Clone the repository:
--bash
git clone https://github.com/ShaeInTheCloud/30days-weather-dashboard.git


For Project Folder Setup
First, we need to creat a clean and organized project structure with these steps:

mkdir weather-dashboard
cd weather-dashboard
mkdir src
touch src/__init__.py 
src/weather_dashboard.py

Then, we need these essential files:
touch requirements.txt README.md .env
echo ".env" >> .gitignore
echo ".zip" >> .gitignore
echo "__pycache__/" >> .gitignore

This setup gives us a neat workspace to keep everything in its place.

Dependencies: Tools and Libraries

Next, we need to install the necessary Python libraries by creating a requirements.txt file:

echo "boto3==1.26.137" >> requirements.txt
echo "python-dotenv==1.0.0" >> requirements.txt
echo "requests==2.28.2" >> requirements.txt
pip install -r requirements.txt

Key Dependencies:

boto3: AWS SDK for Python to interact with AWS services.
python-dotenv: For managing environment variables securely.
requests: To fetch real-time weather data from the OpenWeather API.

⚙ Configuring the Environment
AWS Credentials: We will use the aws configure command to set up our AWS access key and secret access key:
aws configure

2. Environment Variables:We need to add the OpenWeather API key and S3 bucket name to the .env file:

echo "OPENWEATHER_API_KEY=<Your-Weather-Key>" >> .env
echo "AWS_BUCKET_NAME=<your-bucket-name>" >> .env

Pro tip: Always use IAM users for AWS tasks, not the root account, for better security.

🏃 Running the Script: Fetching Weather Data
With everything set up, we can ran the Python script to fetch weather data and store it in our S3 bucket:
python3 src/weather_dashboard.py
Yes!! Our S3 bucket is up and running, and live weather data start flowing in. 🌬Seeing it all come together is incredibly satisfying.

🎓 Key Takeaways:
• Learned how to create and manage AWS S3 buckets programmatically using boto3.
• Gained experience in integrating external APIs like OpenWeather into a Python application.
• Enhanced my skills in managing sensitive credentials securely using environment variables.
• Practiced using Git for source code versioning and collaboration.
