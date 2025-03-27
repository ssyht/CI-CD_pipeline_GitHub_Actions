## Verify that your Flask app is running after the GitHub Actions workflow deploys it to your EC2 instance.

** After GitHub Actions Deploys**
Once you push to the main branch and GitHub Actions finishes, your Flask app should be running at:

```bash
http://<your-ec2-public-ip>:5000
```
**
Option 1: Check in the Browser **
Open your browser and go to:

```bash
http://<your-ec2-ip>:5000
```
You should see:

```
Hello from your EC2-deployed Flask App!
```

**Option 2: Check from Terminal using curl
**
From your local machine, run:

```bash
$ curl http://<your-ec2-ip>:5000
```
Expected output:
```bash
Hello from your EC2-deployed Flask App!
```
**Option 3: Check from inside the EC2 instance
**
If you're SSH'd into the EC2 server:

```bash
$ curl localhost:5000
```

**If it works locally but not externally, it's almost always a Security Group issue (make sure port 5000 is open to 0.0.0.0/0).**

