# 🌦️ Weather Data Collection System – 30 Days DevOps Challenge (Day 1)

This project is part of my **30 Days DevOps Challenge**, where I build a weather dashboard that collects real-time weather data from the **OpenWeather API** and stores it in **AWS S3**. It combines essential DevOps concepts like external API integration, cloud storage, version control, and infrastructure setup using Python.

---

## 🚀 Project Overview

This system demonstrates core DevOps practices by combining:

- 📡 External API Integration (OpenWeather API)  
- ☁️ Cloud Storage with AWS S3  
- ⚙️ Infrastructure Setup  
- 🔐 Environment Variable Management  
- 🐍 Python Development  
- ❗ Error Handling  
- 🗂️ Version Control with Git  

---

## 🔧 Features

- Fetches real-time weather data for **multiple cities**
- Displays **temperature (°F)**, **humidity**, and **weather conditions**
- Automatically stores data in an **S3 bucket**
- Adds **timestamps** to each entry for historical tracking
- Easy to extend with **more cities or APIs**

---

## 🛠️ Technical Architecture

| Component       | Description                         |
|----------------|-------------------------------------|
| Language        | Python 3.x                          |
| Cloud Provider  | AWS (S3)                            |
| External API    | [OpenWeather API](https://openweathermap.org/api) |
| Key Libraries   | `boto3`, `requests`, `python-dotenv` |

---

## 📁 Project Structure

weather-dashboard/
├── src/
│ ├── init.py
│ └── weather_dashboard.py
├── .env
├── .gitignore
├── requirements.txt
└── README.md

yaml
Copy
Edit

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/NazBilgic/weather-api-collector.git
cd weather-api-collector
2. Set Up the Folder Structure (if starting from scratch)
bash
Copy
Edit
mkdir weather-dashboard && cd weather-dashboard
mkdir src
touch src/__init__.py src/weather_dashboard.py
touch requirements.txt README.md .env
Add common patterns to .gitignore:

bash
Copy
Edit
echo ".env" >> .gitignore
echo "__pycache__/" >> .gitignore
3. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
requirements.txt:

text
Copy
Edit
boto3==1.26.137
python-dotenv==1.0.0
requests==2.28.2
4. Configure Environment Variables
env
Copy
Edit
OPENWEATHER_API_KEY=<your-openweather-api-key>
AWS_BUCKET_NAME=<your-s3-bucket-name>
💡 Use IAM users for AWS tasks instead of root for better security.

5. Run the Script
bash
Copy
Edit
python3 src/weather_dashboard.py
✅ Your script will fetch weather data and upload it to the specified S3 bucket.

🎯 Key Takeaways
🔧 Created and managed AWS S3 buckets using boto3

🌐 Integrated OpenWeather API into a Python script

🔐 Used .env to manage sensitive credentials securely

🗃️ Versioned code using Git throughout the process

☁️ Practiced a full cycle of cloud-native development

Made with ☕, ☁️, and a love of DevOps
By Naz Bilgiç