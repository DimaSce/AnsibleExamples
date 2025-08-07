# 📘 Ansible First Playbook

## 📁 Files

- `nginx.yml`: Ansible playbook to install and configure nginx and install curl
- `index.html`: Static HTML file to be copied to the server

---



## 🚀 Run the Playbook

```bash
ansible-playbook -i inventory.ini nginx.yml
```

Make sure `inventory.ini` points to your target (e.g., localhost with Docker container).

---

## ✅ Verify the Result

If `curl` is available in the container:

```bash
ansible test -i inventory.ini -m shell -a "curl localhost"
```

Expected output:

```html
<h1>Hello from Ansible!</h1>
```

---


