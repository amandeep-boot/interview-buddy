# 🧠 Interview Buddy

**Interview Buddy** is an AI-powered tool that helps users prepare for job interviews by asking personalized questions based on their resume and job description. It also answers follow-up queries using real-time context.

This monorepo contains:

- 🎨 [`frontend/`](./frontend): Built with **Next.js**, **TailwindCSS**, and **ShadCN UI**
- ⚙️ [`backend/`](./backend): Built with **FastAPI**, **PostgreSQL**, and integrated with **Groq LLM** (in a **DevContainer**)

---

## 🌐 Live Product Links

| Section     | URL                                                                                                |
| ----------- | -------------------------------------------------------------------------------------------------- |
| Frontend UI | [https://interview-buddy-frontend-pi.vercel.app](https://interview-buddy-frontend-pi.vercel.app)   |
| Swagger API | [https://interview-buddy-backend.vercel.app/docs](https://interview-buddy-backend.vercel.app/docs) |

---

## 💪 Local Setup Guide

### ✅ Clone the Monorepo with Submodules

```bash
git clone --recurse-submodules https://github.com/amandeep-boot/interview-buddy.git
cd interview-buddy
```

---

## ⚙️ Backend Setup (`/backend`) via DevContainer

This project uses **Dev Container** and **Docker** for backend development. Make sure you have:

- [VSCode](https://code.visualstudio.com/download)

- [Dev Container Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

- [Docker](https://www.docker.com/get-started/) 


### Steps:

1. Open the **Interview Buddy** project in VS Code.

2. When prompted, reopen in Dev Container, or manually click the **><** icon in the bottom-left corner of VS Code and choose "Reopen in Container".

3. Ensure Docker is running on your system before launching the container.

4. VS Code will automatically install all required dependencies inside the DevContainer.

5. Add a `.env` file inside the `/backend` folder:

6. Open the `interview-buddy` folder in VS Code.

7. When prompted, reopen in Dev Container.

8. VS Code will automatically install dependencies.

9. Add a `.env` file inside the `/backend` folder:

```env
API_KEY=your_groq_api_key
DATABASE_URL=your_postgresql_database_url
SECRET_KEY=your_jwt_secret
```

> ✅ Use services like [Neon](https://neon.tech) for free PostgreSQL hosting.

5. Once the container starts, run the server:

```bash
uvicorn app.main:app --reload --host 0.0.0.0 --port 80 --reload
```

Then visit: [http://localhost:8000/docs](http://localhost:8000/docs)

---

## 💻 Frontend Setup (`/frontend`)

### 1. Install dependencies

```bash
cd frontend
pnpm install
```

### 3. Run the Frontend

```bash
pnpm run dev
```

Then visit: [http://localhost:3000](http://localhost:3000)

---

## 📦 Tech Stack

| Layer    | Tools / Libraries               |
| -------- | ------------------------------- |
| Frontend | Next.js, TailwindCSS, ShadCN UI |
| Backend  | FastAPI, SQLAlchemy, Groq API   |
| Database | PostgreSQL                      |
| Auth     | JWT via OAuth2                  |
| Hosting  | Vercel (Frontend & Backend)     |
| Dev Env  | DevContainers (VS Code)         |

---

## 🚀 Features

- ✅ Resume PDF upload
- ✅ JD submission for context
- ✅ Personalized interview questions
- ✅ Chat-style follow-ups and Q&A
- ✅ Secure login with JWT
- ✅ Streamed LLM responses

---

## 👍 Contributing

Pull requests are welcome! Open an issue first to discuss what you would like to change.

---

## 📍 License

This project is licensed under the MIT License.

---

## ✨ Maintained by [Amandeep](https://github.com/amandeep-boot)

