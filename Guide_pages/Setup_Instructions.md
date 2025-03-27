# Setup Instructions

## Prerequisites
- AWS account with access to EC2
- GitHub account with access to create a repository
- SSH key pair (PEM file) for secure connection to EC2

## Steps

### 1. Clone the Repository
```bash
git clone https://github.com/ssyht/CI-CD_pipeline_GitHub_Actions.git
```
### 2. Launch an EC2 Instance
* Choose Ubuntu Server (20.04 or 22.04 LTS)
* Make sure your security group allows:
- SSH (Port 22)
* Custom TCP (Port 5000) for the Flask app

### 3. SSH into EC2 Instance

```bash
chmod 400 your-key.pem
ssh -i your-key.pem ubuntu@your-ec2-ip
```

### 4. Set up the instance
Go to your GitHub repo > Settings > Secrets > Actions, and add:
