# 📘 Ansible Apache + Jinja2 Template
You need to open port 8080:80 for apache
```bash
docker run -d --name ansible-test \
  -p 8080:80 \
  --privileged \
  ansible-test:latest
 ``` 

## 📁 Files

- `apache.yml`: Ansible playbook to install and configure apache
- `index.html`: Dynamically HTML file to be copied to the server

---



## 🚀 Run the Playbook

```bash
ansible-playbook -i inventory.ini apache.yml
```

Make sure `inventory.ini` points to your target (e.g., localhost with Docker container).

---

## ✅ Verify the Result

If `curl` is available in the container:

```bash
ansible test -i inventory.ini -m shell -a "curl localhost"
```

Check in your browser
http://localhost:8080

---


