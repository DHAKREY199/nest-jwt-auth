
# 🚀 NestJS JWT Authentication API

A production-ready **NestJS authentication service** that generates and validates JWT tokens using a **MySQL database** for user validation.

This project is fully deployed and accessible online.

---

## 🌐 Live API Base URL

```
https://nest-jwt-auth-w4sg.onrender.com
```

---

## 🔥 Features

✔ Generate JWT token for a valid user  
✔ Validate JWT token (active / expired)  
✔ JWT expiry configurable via `.env`  
✔ MySQL database integration  
✔ Cloud deployment on Render  
✔ Cloud database on Railway  

---

## 🧪 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/auth/token` | Generate a JWT token for user |
| GET | `/auth/validate` | Validate a provided JWT token |

---

## 📌 Sample cURL Requests

### 🔹 Generate JWT Token
```sh
curl --location 'https://nest-jwt-auth-w4sg.onrender.com/auth/token' --header 'Content-Type: application/json' --data-raw '{"email": "himanshu@gmail.com"}'
```

### 🔹 Validate JWT Token
```sh
curl --location 'https://nest-jwt-auth-w4sg.onrender.com/auth/validate' --header 'Authorization: Bearer <your_jwt_token_here>'
```

---

## 🗄️ Database

The MySQL database is hosted on **Railway (Docker-based deployment)**  
Website: https://railway.com/

Table created by TypeORM automatically:

| Field | Type |
|-------|------|
| id | INT (Primary, Auto Increment) |
| email | VARCHAR (Unique) |

A user row must exist to generate tokens, e.g.:

```sql
INSERT INTO user (email) VALUES ('himanshu@gmail.com');
INSERT INTO user (email) VALUES ('prayas@gmail.com');
INSERT INTO user (email) VALUES ('purujit@gmail.com');
```

---

## ⚙️ Environment Variables

Create a `.env` file in the project root:

```
PORT=3000

JWT_SECRET=your_secret_here
JWT_EXPIRES_IN=20s

DB_HOST=your_db_host_here
DB_PORT=your_db_port_here
DB_USER=your_db_username_here
DB_PASS=your_db_password_here
DB_NAME=your_database_name_here
```

⚠ Render deployment requires no quotes  
⚠ `JWT_EXPIRES_IN` supports formats like `20s`, `5m`, `1h`

---

## ▶️ Run Locally

```bash
npm install
npm run start:dev
```

App runs on:

```
http://localhost:3000
```

---

## 🏗️ Build for Production

```bash
npm run build
npm start
```

---

## ☁️ Deployment

| Service | Purpose | URL |
|--------|---------|-----|
| Render | Application deployment | https://dashboard.render.com |
| Railway | Cloud MySQL DB | https://railway.com/ |

CI/CD enabled through GitHub → Render deployments.

---

## 📂 Tech Stack

| Technology | Purpose |
|------------|---------|
| NestJS | Backend framework |
| TypeORM | ORM |
| MySQL | Database |
| JWT | Authentication |
| Render | Deployment |
| Railway | Cloud DB |

---

## 👨‍💻 Author

**Himanshu Dhakrey**  
GitHub: https://github.com/DHAKREY199

---

## 📝 License

This project is for educational & portfolio purposes.  
Free to clone and modify — credit appreciated.
