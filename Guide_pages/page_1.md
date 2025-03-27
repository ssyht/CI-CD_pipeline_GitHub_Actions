## EC2 Setup Commands (Ubuntu)

Step 1: SSH into your EC2 instance
- Replace your-key.pem and your-ec2-ip with your values:

```bash
$ chmod 400 your-key.pem
$ ssh -i your-key.pem ubuntu@<your-ec2-ip>
```

Step 2: Install Python, pip, venv

```bash
$ sudo apt update
$ sudo apt install python3-pip python3-venv -y
```

Step 3: (Optional but Recommended) Install Git

```bash
sudo apt install git -y
```

Step 4: Create a directory for the app
```bash
$ mkdir -p ~/flask-app
```
- This should match the target: "~/flask-app" path from your GitHub Actions YAML.

Step 5: Allow incoming traffic on port 5000
Make sure your Security Group attached to the EC2 instance allows:
* Type: Custom TCP
* Port: 5000
* Source: Anywhere (or restrict to your IP if needed)
