# 🔥 TubeEngine (YouTube x Twitter)

**TubeEngine** is a full-stack MERN project that combines the core functionalities of **YouTube** (videos, subscriptions, playlists) and **Twitter** (tweets, likes, comments) into one powerful media-sharing platform. This project is now fully deployed on a **Google Cloud VM** using **Docker** and **NGINX**.

---

## 🌐 Live Links

| Resource            | Link                                                                 |
|---------------------|----------------------------------------------------------------------|
| 🧪 Postman Docs     | [View API Documentation](https://documenter.getpostman.com/view/39785896/2sB2izDt48) |
| 🧠 DB Schema Model  | [Eraser Diagram](https://app.eraser.io/workspace/OJQXZCrbUtiEVt8QAo5G) |
| 🚀 Live App (GCP)   | [Visit App](http://34.93.82.254:8080) *(HTTP only)*                  |
| 🚀 Live App (vercel)    | [View on Vercel](https://tube-mern-project.vercel.app/)              |

---

## 🔥 Features

### 👤 User Management
- Signup, login, logout, JWT-based authentication
- Profile updates, avatar upload
- Watch history, liked video tracking

### 🎥 Video Handling
- Upload/publish/unpublish
- Edit/delete videos, stream with resolutions
- Auto-cleanup on cancel upload

### 🐦 Tweet System
- Post, edit, delete tweets
- Like/dislike tweets

### 🔔 Subscriptions
- Subscribe/unsubscribe channels
- View subscriber counts

### 🎶 Playlists
- Create/manage playlists
- Add/remove videos

### ❤️ Likes & Comments
- Like/unlike videos, tweets, comments
- Full comment system on videos

### 📊 Dashboard Stats
- Views, likes, comment stats
- Channel analytics

### 🩺 Health Check
- `GET /healthcheck` returns `{ status: "Ok" }`

---

## 🧰 Tech Stack

| Layer      | Tech                                                                 |
|------------|----------------------------------------------------------------------|
| Frontend   | React.js, Axios, React Router, Tailwind CSS                          |
| Backend    | Node.js, Express.js                                                  |
| Database   | MongoDB with Mongoose                                                |
| Auth       | JWT                                                                  |
| Storage    | Cloudinary                                                           |
| Deployment | Docker, Docker Compose, NGINX, GitHub Actions CI/CD, GCP VM (Debian) |
| Api Testing| Postman                                                              |

---

## 🚀 Deployment Setup (GCP + Docker)

This app is deployed on a **Google Cloud VM** with the following architecture:

- **Reverse Proxy**: NGINX
- **Containers**: Backend, Frontend, MongoDB
- **CI/CD**: GitHub Actions triggers deploy on push to `main`

### Project Structure

mern-project/  
├── backend/  
├── frontend/  
├── nginx/  
├── docker-compose.yml  
└── .github/workflows/deploy.yml  

---

## 📦 Local Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/CodewithDeep23/mern-project.git
    cd mern-project
    ```

2. **Setup Environment Variables:**  
- Create .env files inside both /backend and /frontend based on sample .env.sample.

3. **Run With Docker:**
    ```bash
    sudo docker-compose up --build
    ```

---

## 🛠 CI/CD (GitHub Actions)
Every time you push to `main`, GitHub Actions:
- SSH into GCP VM using secret keys
- Pulls latest code
- Rebuilds Docker containers
- Restarts services

**Secrets used:**

- `GCP_SSH_KEY` (private SSH key)
- VM must have corresponding public key in `~/.ssh/authorized_keys`

---

## 🙋 About the Author

Hi! I'm **Deepankar Singh**, a passionate Development Engineer with a strong foundation in full-stack web development and deployment engineering.  
This project is part of my personal portfolio to showcase hands-on expertise in building scalable, containerized applications using the MERN stack, Docker, NGINX, and CI/CD automation on cloud infrastructure (GCP).

📫 Let's connect:
- [LinkedIn](www.linkedin.com/in/deepankar-singh-a35b14296)
- [GitHub](https://github.com/CodewithDeep23)

--- 

If you found this project helpful, feel free to ⭐ the repo!