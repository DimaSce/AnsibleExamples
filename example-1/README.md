# 🧪 Ansible Lab – Lesson 1: Getting Started with Ansible

## 🚀 Step-by-step Instructions

### 1. Install Ansible

For Ubuntu/Debian:
```bash
sudo apt update
sudo apt install -y ansible
```
### 2. Build a Test SSH Server (Docker)
Create Fockerfile

Build the image:
```bash
docker build -t ansible-ssh .
```
Run the container:

```bash
docker run -d --name ansible-test -p 2222:22 ansible-ssh
```
Test SSH Connection
```bash
ssh ansible@127.0.0.1 -p 2222
```
### 3. Configure Ansible Inventory and Test

Create inventory.ini
Ping the test host:
```bash
ansible -i inventory.ini test -m ping
```
### 4. Run Commands
```bash
ansible test -i inventory.ini -m command -a "uname -a"
echo "Hello from Ansible" > hello.txt
#Copy file to server
ansible test -i inventory.ini -m copy -a "src=hello.txt dest=/tmp/hello.txt"
# Check
ansible test -i inventory.ini -m shell -a "cat /tmp/hello.txt"
```


