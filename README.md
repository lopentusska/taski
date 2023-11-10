# Taski

### Simple app to take care of daily tasks, so you don't forget to do anything.

## Used technologies:
#### Django
#### Django REST
#### React

## Start the project:

### Clone the repository
```bash
git clone git@github.com:lopentusska/taski.git
```

### Create .env file with the following script
```bash
cd taski/
echo '''DB_NAME=taski_db
POSTGRES_USER=taski_user
POSTGRES_PASSWORD=taski_password
DB_HOST=localhost
DB_PORT=5432
DJANGO_SECRET_KEY=your_secret_key
DJANGO_DEBUG=True
DJANGO_ALLOWED_HOSTS=127.0.0.1 localhost''' > .env
```

# Run project in docker:

```bash
docker compose up -d
```
#### wait some time to let docker build containers

#### logs:
```bash
docker logs <container_name> -f
```

#### stop containers:
```bash
docker compose down
```
 

### postgresql
```bash
sudo su postgres
psql
CREATE DATABASE taski_db;
CREATE USER taski_user WITH PASSWORD 'taski_password';
GRANT ALL PRIVILEGES ON DATABASE taski_db TO taski_user;
ALTER USER taski_user CREATEDB;
```

### Create venv and install requirements.txt
```bash
cd backend/
python -m venv venv
source venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

### Run migrations and start server
```bash
python manage.py migrate
python manage.py runserver
```

### Optionally create superuser
```bash
python manage.py createsuperuser
```

## Start frontend
```bash
cd frontend/
npm install 
npm start
```
