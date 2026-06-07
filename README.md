<div align="center">

<br />

# ✍️ WRITEZY

### *Your space to think out loud. Write without filters.*

<br />

[![Live Demo](https://img.shields.io/badge/🚀%20Live%20Demo-Visit%20Writezy-0D7073?style=for-the-badge&logoColor=white)](https://writezy-blog-platform-g2ky.vercel.app)

<br />

![React](https://img.shields.io/badge/React_18-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_v4-0EA5E9?style=flat-square&logo=tailwindcss&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white)

<br />

> Writezy is a full-stack AI-powered blog platform where writers publish, manage, and share stories —
> with a clean reading experience, rich text editing, comment moderation, and a smart admin dashboard.

<br />

---

</div>

## 📋 Table of Contents

- [✨ Features](#-features)
- [🖥️ Demo](#️-demo)
- [🛠️ Tech Stack](#️-tech-stack)
- [📁 Project Structure](#-project-structure)
- [⚙️ Local Setup](#️-local-setup)
- [🔑 Environment Variables](#-environment-variables)
- [🌐 API Reference](#-api-reference)
- [🚀 Deployment](#-deployment)
- [🤝 Contributing](#-contributing)
- [👩‍💻 Team](#-team)

---

## ✨ Features

- 🤖 &nbsp; **AI Blog Generation** — Generate full blog posts from a single title using **Groq LLaMA 3.3 70B**
- ✍️ &nbsp; **Rich Text Editor** — Write and format with **Quill** (headings, bold, lists, links)
- 🖼️ &nbsp; **Image CDN** — Thumbnail upload and delivery via **ImageKit**
- 🔐 &nbsp; **Secure Admin Panel** — JWT-authenticated dashboard to manage all content
- 💬 &nbsp; **Comment Moderation** — Approve or delete reader comments before they go live
- 🌙 &nbsp; **Dark / Light Mode** — Full theme toggle, persisted across sessions via localStorage
- 🔍 &nbsp; **Search & Filter** — Search by title or filter blogs by category in real time
- 📱 &nbsp; **Fully Responsive** — Pixel-perfect on mobile, tablet, and desktop
- 📰 &nbsp; **Newsletter Section** — Built-in email subscription UI
- 🐱 &nbsp; **Custom 404 Page** — Animated caveman page for unknown routes

---

## 🖥️ Demo

🔗 **[writezy-blog-platform-g2ky.vercel.app](https://writezy-blog-platform-g2ky.vercel.app)**

### Admin Login

| Field | Value |
|---|---|
| Email | `admin@example.com` |
| Password | `TripleShot` |

Click **Login →** in the top-right corner to access the admin dashboard.

---

## 🛠️ Tech Stack

### Frontend

| Technology | Role |
|---|---|
| React 18 + Vite | UI framework & dev server |
| Tailwind CSS v4 | Utility-first styling |
| React Router DOM v6 | Client-side routing |
| Axios | HTTP client |
| React Quill | Rich text editor |
| Framer Motion | Smooth animations |
| Moment.js | Human-readable dates |

### Backend

| Technology | Role |
|---|---|
| Node.js + Express | REST API server |
| MongoDB + Mongoose | Database & ODM |
| JWT | Stateless authentication |
| Multer | Multipart file handling |
| ImageKit SDK | Image upload & CDN |
| Groq SDK | AI content generation |

### Infrastructure

| Service | Purpose |
|---|---|
| Vercel | Frontend hosting |
| Render | Backend hosting |
| MongoDB Atlas | Cloud database |
| ImageKit | Image storage & CDN |

---

## 📁 Project Structure

```
Writezy-Blog-Platform/
│
├── client/                        # React frontend
│   ├── public/
│   └── src/
│       ├── assets/                # Images, icons, static data
│       ├── components/
│       │   ├── admin/
│       │   │   ├── BlogTableItem.jsx
│       │   │   ├── CommentTableItem.jsx
│       │   │   └── Sidebar.jsx
│       │   ├── BlogCard.jsx       # Blog preview card
│       │   ├── BlogList.jsx       # Filtered blog grid
│       │   ├── Footer.jsx
│       │   ├── Header.jsx         # Hero + search bar
│       │   ├── Loader.jsx         # Animated cat loader
│       │   ├── Navbar.jsx         # Nav + dark mode toggle
│       │   └── Newsletter.jsx
│       ├── context/
│       │   ├── AppContext.jsx     # Global state (token, blogs, axios)
│       │   └── ThemeContext.jsx   # Dark/light mode state
│       ├── pages/
│       │   ├── admin/
│       │   │   ├── AddBlog.jsx    # Create blog + AI generate
│       │   │   ├── Comments.jsx   # Comment moderation
│       │   │   ├── Dashboard.jsx  # Stats overview
│       │   │   ├── Layout.jsx     # Admin shell + sidebar
│       │   │   ├── ListBlog.jsx   # Manage all blogs
│       │   │   └── Login.jsx      # Admin login
│       │   ├── Blog.jsx           # Single blog + comments
│       │   ├── Home.jsx           # Public homepage
│       │   └── NotFound.jsx       # Custom 404
│       ├── App.jsx
│       ├── index.css
│       └── main.jsx
│
└── server/                        # Node.js backend
    ├── configs/
    │   ├── db.js                  # MongoDB connection
    │   ├── groq.js                # Groq AI client
    │   └── imageKit.js            # ImageKit client
    ├── controllers/
    │   ├── adminController.js     # Admin logic
    │   └── blogController.js      # Blog & comment logic
    ├── middleware/
    │   ├── auth.js                # JWT verification
    │   └── multer.js              # File upload config
    ├── models/
    │   ├── Blog.js
    │   └── Comment.js
    ├── routes/
    │   ├── adminRoutes.js
    │   └── blogRoutes.js
    └── server.js
```

---

## ⚙️ Local Setup

### Prerequisites

- Node.js v18+
- [MongoDB Atlas](https://www.mongodb.com/atlas) account
- [Groq](https://console.groq.com) API key
- [ImageKit](https://imagekit.io) account

### Step 1 — Clone

```bash
git clone https://github.com/priyapoonia0213-art/Writezy-Blog-Platform.git
cd Writezy-Blog-Platform
```

### Step 2 — Backend

```bash
cd server
npm install
```

Create `server/.env` (see [Environment Variables](#-environment-variables)) then:

```bash
node server.js
# or with auto-reload:
nodemon server.js
```

Server starts at `http://localhost:3000`

### Step 3 — Frontend

```bash
cd client
npm install
```

Create `client/.env`:

```env
VITE_BACKEND_URL=http://localhost:3000
```

```bash
npm run dev
```

App starts at `http://localhost:5173`

---

## 🔑 Environment Variables

### `server/.env`

```env
# Server
PORT=3000

# Authentication
JWT_SECRET=your_super_secret_jwt_key

# Admin Credentials
ADMIN_EMAIL=admin@example.com
ADMIN_PASSWORD=your_admin_password

# MongoDB
MONGODB_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/writezy?retryWrites=true&w=majority

# ImageKit
IMAGEKIT_PUBLIC_KEY=your_public_key
IMAGEKIT_PRIVATE_KEY=your_private_key
IMAGEKIT_URL_ENDPOINT=https://ik.imagekit.io/your_imagekit_id

# Groq AI
GROQ_API_KEY=your_groq_api_key
```

### `client/.env`

```env
VITE_BACKEND_URL=http://localhost:3000
```

---

## 🌐 API Reference

### Public Routes — No auth required

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/blog` | Get all published blogs |
| `GET` | `/api/blog/:id` | Get a single blog by ID |
| `POST` | `/api/blog/comments` | Get approved comments for a blog |
| `POST` | `/api/blog/add-comment` | Submit a new comment |
| `POST` | `/api/blog/generate` | Generate AI blog content from a title |

### Admin Routes — Requires `Authorization: <token>` header

| Method | Endpoint | Description |
|---|---|---|
| `POST` | `/api/admin/login` | Admin login → returns JWT token |
| `GET` | `/api/admin/dashboard` | Stats (blogs, comments, drafts) + recent blogs |
| `GET` | `/api/admin/blogs` | All blogs including unpublished |
| `POST` | `/api/blog/add` | Create a new blog (multipart/form-data) |
| `POST` | `/api/blog/delete` | Delete a blog by ID |
| `POST` | `/api/blog/toggle-publish` | Publish or unpublish a blog |
| `GET` | `/api/admin/comments` | All comments (pending + approved) |
| `POST` | `/api/admin/approve-comment` | Approve a pending comment |
| `POST` | `/api/admin/delete-comment` | Delete a comment |

---

## 🚀 Deployment

### Backend → Render

1. Go to [render.com](https://render.com) → **New Web Service**
2. Connect this GitHub repo → set root directory to `server/`
3. Build command: `npm install`
4. Start command: `node server.js`
5. Add all variables from `server/.env` under **Environment**
6. Deploy and copy your live URL (e.g. `https://writezy-api.onrender.com`)

### Frontend → Vercel

1. Go to [vercel.com](https://vercel.com) → **New Project**
2. Connect this GitHub repo → set root directory to `client/`
3. Add environment variable:
   ```
   VITE_BACKEND_URL = https://writezy-api.onrender.com
   ```
4. Deploy

### MongoDB Atlas

- Go to **Network Access** → **Add IP Address** → `0.0.0.0/0`  
  This allows Render's dynamic IPs to connect.

---

## 🤝 Contributing

We welcome contributions of all kinds — bug fixes, features, UI improvements, or docs.

```bash
# 1. Fork and clone your fork
git clone https://github.com/your-username/Writezy-Blog-Platform.git

# 2. Create a branch
git checkout -b feature/your-feature-name

# 3. Make changes and commit
git commit -m "feat: describe your change clearly"

# 4. Push and open a Pull Request
git push origin feature/your-feature-name
```

**Commit message conventions:**

| Prefix | When to use |
|---|---|
| `feat:` | New feature |
| `fix:` | Bug fix |
| `style:` | UI / styling change |
| `refactor:` | Code cleanup |
| `docs:` | Documentation update |

---

## 👩‍💻 Team

Writezy was collaboratively built by:

<table>
  <tr>
    <td align="center">
      <b>Priya</b><br/>
      <sub>Full Stack</sub>
    </td>
    <td align="center">
      <b>Saloni</b><br/>
      <sub>Full Stack</sub>
    </td>
    <td align="center">
      <b>Bhawana</b><br/>
      <sub>Full Stack</sub>
    </td>
  </tr>
</table>

---

<div align="center">

<br/>

**[⬆ Back to top](#️-writezy)**

<br/>

© 2026 Writezy — All Rights Reserved

*Made with ♥ by Priya, Saloni & Bhawana*

</div>
