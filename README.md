# 🚀 **Setup Local Environment**  

## 🐳 **Spin up Your DB with Docker**  
Make sure Docker is installed and running. To start the database container:  
```bash
docker-compose up -d
```

---

## 💻 **Running Without Docker (For Devs)**  
Ensure that PostgreSQL is up and running locally, or you can run it via Docker as shown above.

---

### 🔥 **1. Install UV (Python Package and Project Manager)**  
Install `uv` using the following command:  
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

---

### 🐍 **2. Install Python 3.13 Using UV**  
Install the specific Python version:  
```bash
uv python install 3.13.0
```

---

### 🌐 **3. Create a Virtual Environment and Activate It**  
Create and activate the virtual environment:  
```bash
uv venv --python 3.13
source .venv/bin/activate
```

---

### 📦 **4. Install Dependencies**  
Install all dependencies listed in `pyproject.toml`:  
```bash
uv pip install -r pyproject.toml
```

---

### 🚀 **5. Start the Project**  
Now you are ready to run the project! 🎉  
```bash
python manage.py runserver
```

---

## ✅ **💡 Pro Tips:**  
- To stop the Docker container:  
```bash
docker-compose down
```
- If you face any dependency issues, try running:  
```bash
uv pip install --upgrade -r pyproject.toml
```
- Check for any pending database migrations:  
```bash
python manage.py makemigrations
python manage.py migrate
```