# 📘 Ansible example 5 –  Ising Roles (Apache Role Example)

In this lesson, you'll learn how to use **Ansible Roles** to organize and reuse your automation code. We'll create a role to install and configure Apache, and serve a custom HTML page using a Jinja2 template.

---

## 📁 Project Structure

lesson-5/
├── inventory.ini
├── main.yml # Playbook that calls the role
└── roles/
└── apache_role/
├── tasks/
│ └── main.yml
├── templates/
│ └── index.html.j2
├── defaults/
│ └── main.yml
└── ...

### 1. Create the Role

```bash
ansible-galaxy init roles/apache_role
```
2. Edit the Role Files
roles/apache_role/tasks/main.yml
roles/apache_role/templates/index.html
roles/apache_role/defaults/main.yml

3. Create the Playbook using role

4. Run 
```bash
ansible-playbook -i inventory.ini main.yml
```
5. Check tpur browser