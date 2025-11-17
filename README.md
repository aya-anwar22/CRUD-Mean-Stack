
# Task Management App (MEAN Stack)

A simple CRUD web application built with the **MEAN stack** (MongoDB, Express.js, Angular, Node.js).  
It allows users to **create, read, update, and delete** tasks from a single data model.  
No authentication or advanced UI is included — just basic CRUD functionality.

---

## 🛠️ Tech Stack
- **Frontend:** Angular (Standalone Components)
- **Backend:** Express.js + Node.js
- **Database:** MongoDB
- **API Base URL:** `http://localhost:3000/api/tasks`

---

## 📂 Project Structure
```

project-root/
├── backend/          ← Express server (API)
├── frontend/         ← Angular app
└── README.md

````

---

## ⚙️ Backend Setup

1. Navigate to the backend folder:
   ```bash
   cd backend
````

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file inside the `backend` folder with:

   ```
   PORT=3000
   MONGO_URI=mongodb://localhost:27017/taskdb
   ```

   > If using MongoDB Atlas, replace the URI accordingly:
   > `MONGO_URI=mongodb+srv://<user>:<password>@cluster0.mongodb.net/taskdb`

4. Start the server:

   ```bash
   npm start
   ```

   The backend should now be running on `http://localhost:3000`.

---

### 🔗 API Endpoints

| Method | Endpoint         | Description             |
| ------ | ---------------- | ----------------------- |
| GET    | `/api/tasks`     | Get all tasks           |
| POST   | `/api/tasks`     | Create a new task       |
| PUT    | `/api/tasks/:id` | Update an existing task |
| DELETE | `/api/tasks/:id` | Delete a task           |

**Example POST body:**

```json
{
  "title": "Buy groceries",
  "description": "Milk, bread, and eggs",
  "completed": false
}
```

---

## 💻 Frontend Setup (Angular)

1. Open a new terminal and navigate to the frontend folder:

   ```bash
   cd frontend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Run the Angular app:

   ```bash
   ng serve
   ```

   or:

   ```bash
   npm start
   ```

4. Open your browser at:

   ```
   http://localhost:4200
   ```

> The frontend connects to the backend API at `http://localhost:3000/api/tasks`.
> If your backend runs on a different port or host, update the `apiUrl` inside
> `src/app/services/task.service.ts`.

---

###  Build Production Version (Optional)

To create a production build:

```bash
ng build --configuration production
```

This will generate a `/dist` folder containing optimized frontend files.

---

## 🧪 Quick Test (Optional)

You can test API endpoints using `curl`:

```bash
# Get all tasks
curl http://localhost:3000/api/tasks

# Add a new task
curl -X POST http://localhost:3000/api/tasks \
  -H "Content-Type: application/json" \
  -d '{"title":"Test Task","description":"Example","completed":false}'
```

---

## ⚡ Common Issues

* **CORS error:**
  Ensure `cors` is installed and used in backend:

  ```js
  const cors = require('cors');
  app.use(cors());
  ```

* **MongoDB not connecting:**
  Check your `MONGO_URI` and make sure MongoDB service is running.

* **Angular errors (`ngModel`, `*ngFor`):**
  Make sure each standalone component imports `CommonModule` and `FormsModule` if needed.

---

##  Create ZIP for Submission

To package your project:

```bash
zip -r task-crud-mean.zip backend frontend README.md
```

This will create a `task-crud-mean.zip` file containing everything.

---


```

---

## 💬 2) Message to Send with the ZIP File

You can send this message to your client by email or chat:

---

**Subject:** Task CRUD Application (MEAN Stack)

**Message:**
```

Hello [Client Name],

Here’s the completed MEAN stack CRUD project you requested (attached as `task-crud-mean.zip`).

Inside the zip:

* `backend/` → Express + MongoDB API
* `frontend/` → Angular app (standalone)
* `README.md` → Detailed instructions on how to set up and run both parts

Quick Start:

1. Run MongoDB locally or connect to your Atlas database
2. Start the backend:
   `cd backend && npm install && npm start`
3. Start the frontend:
   `cd frontend && npm install && ng serve`
4. Open your browser at `http://localhost:4200`

Please let me know if you’d like me to deploy it online or help with production setup.

Best regards,
**Aya Anwar**

````

---

## ⚙️ 3) (Optional) Quick ZIP Command

If you want to compress everything before sending:
```bash
zip -r task-crud-mean.zip backend frontend README.md
````

---

