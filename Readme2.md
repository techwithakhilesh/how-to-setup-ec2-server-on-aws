# 🚀 How to Launch Your First Amazon EC2 Instance (Beginner Friendly Guide)


## Here’s a simple step-by-step guide 👇

### 1️⃣ Login to AWS Console

#### Go to AWS Management Console and search for EC2.

💡 Why?
EC2 lets you create virtual servers in the cloud.

### 2️⃣ Choose Your Region

Select your preferred region from the top-right corner
Example: Mumbai (ap-south-1)

💡 Why?
Region affects:
✔ Server location
✔ Speed / latency
✔ Cost

3️⃣ Click “Launch Instance”

### Go to EC2 Dashboard → Click Launch Instance

💡 Why?
This opens the setup wizard to create your server.

### 4️⃣ Name Your Instance

Examples:

my-nginx-server
dev-server

💡 Why?
Makes it easier to identify later.

### 5️⃣ Select an AMI (Operating System)

Choose:

### Amazon Linux (recommended for beginners)
Ubuntu

💡 Why?
AMI = OS image for your server.
No OS = no server.

### 6️⃣ Choose Instance Type

Popular options:

t2.micro / t3.micro (Free Tier)

💡 Why?
Instance type decides:
✔ CPU
✔ RAM
✔ Performance

Example:

Practice / small app → micro
Production → larger type
### 7️⃣ Create / Select Key Pair

Click Create new key pair

Choose:

.pem → Mac / Linux
.ppk → Windows PuTTY

💡 Why?
Used for secure SSH login.
Without this, you may not access your server.

### 8️⃣ Configure Security Group (Firewall)

Add inbound rules:

SSH → Port 22 → My IP
HTTP → Port 80 → Anywhere
HTTPS → Port 443 → Anywhere (optional)

💡 Why?
Security Group protects your server and controls access.

### 9️⃣ Configure Storage

Default 8 GB is enough for learning.

💡 Why?
Used to store:
✔ OS
✔ App files
✔ Logs

### 🔟 Launch Instance

Review all settings → Click Launch Instance

💡 Why?
AWS will create your cloud machine.

 Wait for Status Checks

Wait until:
✅ Instance state = Running
✅ Status checks = 2/2 passed

💡 Why?
Server must be fully ready before login.

 Connect to Your Server
Option A: Browser

### EC2 → Select Instance → Connect → EC2 Instance Connect

Option B: SSH (Mac/Linux)
chmod 400 my-key.pem
ssh -i my-key.pem ec2-user@your-public-ip

💡 Why?
This gives you terminal access to:
✔ Install software
✔ Deploy apps
✔ Manage files

👉 Default username for Amazon Linux: ec2-user

### 🔧 Basic Setup After Login

Install Nginx:

  - sudo yum update -y
  - sudo yum install nginx -y
  - sudo systemctl start nginx
  - sudo systemctl enable nginx
