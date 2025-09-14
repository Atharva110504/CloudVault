# Cloud-computing-project

☁️ CloudVault - Cloud File Storage System

**CloudVault** is a simple, secure, and scalable cloud-based file storage system built using **Flask** and **AWS S3**. This project allows users to upload files via a web interface, and those files are securely stored in an Amazon S3 bucket. It’s designed for quick deployment, ease of use, and efficient file handling.

---

## 📌 Features

✔ Upload files securely to the cloud  
✔ Simple and clean user interface  
✔ File validation to prevent empty uploads  
✔ Uses AWS S3 for reliable and scalable storage  
✔ Designed for quick deployment on an EC2 instance  
✔ Responsive layout with modern styling

---

## 📂 Project Structure
CloudVault/
├── app.py # Flask backend logic
├── README.md # Project documentation
├── requirements.txt # Python dependencies (Flask, boto3)
└── (additional files) # EC2 setup scripts, configuration files

## 🚀 Tech Stack

- **Backend:** Python, Flask  
- **Cloud Storage:** AWS S3  
- **Deployment:** AWS EC2  
- **Security:** AWS IAM Roles and S3 permissions  
- **Frontend:** HTML, CSS (inline styling)  
- **Version Control:** Git/GitHub

---

## ⚙️ Installation and Setup

### Prerequisites
✔ AWS account with an S3 bucket created  
✔ EC2 instance with Python3 installed  
✔ IAM user with S3 access permissions

### Steps
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/cloudvault.git
   cd cloudvault
Set up the environment on your EC2 instance:

bash
Copy code
sudo yum update -y
sudo yum install python3-pip -y
pip3 install Flask boto3
Configure your AWS credentials (either via environment variables or IAM role).

Update S3_BUCKET_NAME and region in app.py:

python
Copy code
S3_BUCKET_NAME = 'your-s3-bucket-name'
s3 = boto3.client('s3', region_name='your-region')
Run the application:

bash
Copy code
python3 app.py
Visit http://<your-ec2-public-ip>:5000/ in your browser to upload files.


🔑 Security Notes
The app uses AWS IAM for secure access to the S3 bucket.
Files are validated to prevent empty or invalid uploads.
Deploying on EC2 with proper firewall rules ensures controlled access.

📖 How to Use
Navigate to the web interface.
Click "Choose File" and select the file you want to upload.
Click "Upload File."
Upon successful upload, you’ll see a confirmation message.
