# 🚀 Social Media Platform Backend API

A production-style backend service for a Social Media Platform, implementing core social networking features such as:

- User management  
- Creating posts with hashtags  
- Following and unfollowing users  
- Liking and unliking posts  
- Personalized feed generation  
- User activity history tracking  

This project is built with **Node.js, Express, TypeScript, TypeORM, and SQLite**, using migration-based schema design and clean backend architecture principles.

---
🎥 Backend Assignment Walkthrough (CLI + Browser Demo)

Watch the backend system in action demonstrating API endpoints, CLI testing, and browser requests.

👉 https://loom.com/share/YOUR_VIDEO_ID

## ✨ Key Features

✅ Full CRUD support for all entities  
✅ Posts with hashtag tagging  
✅ Follow/unfollow system with duplicate prevention  
✅ Like/unlike support with unique constraints  
✅ Personalized feed endpoint (`/api/feed`)  
✅ Hashtag search (`/api/posts/hashtag/:tag`)  
✅ Followers listing (`/api/users/:id/followers`)  
✅ User activity timeline (`/api/users/:id/activity`)  
✅ Pagination support (`limit`, `offset`)  
✅ Joi request validation for data integrity  
✅ Migration-driven database schema (`synchronize: false`)  
✅ Interactive PowerShell testing script for endpoint coverage  

---

## 🛠 Tech Stack

| Layer        | Technology |
|-------------|------------|
| Runtime      | Node.js |
| Framework    | Express.js |
| Language     | TypeScript |
| ORM          | TypeORM |
| Database     | SQLite |
| Migrations   | TypeORM Migrations |
| Validation   | Joi |
| Testing Tool | PowerShell Script (`test.ps1`) |

---

## 📂 Project Structure

```bash
src/
 ├── controllers/     # Business logic
 ├── routes/          # API route definitions
 ├── entities/        # TypeORM entity models
 ├── migrations/      # Database migration files
 ├── data-source.ts   # TypeORM DataSource configuration
 └── index.ts         # Application entry point

test.ps1              # Interactive CLI testing script
DESIGN.md             # Schema + indexing documentation

**Architecture Principles

Entities → Data structure only

Controllers → Core business logic

Routes → API endpoint wiring

Migrations → Schema evolution and version control

Testing Script → Endpoint verification through CLI


📌 Full database design is documented in DESIGN.md.
** API Endpoints
Feed

GET /api/feed?userId=1&limit=10&offset=0

Returns posts from followed users, sorted by newest first.

Posts by Hashtag

GET /api/posts/hashtag/:tag

Case-insensitive hashtag matching with pagination.

Followers

GET /api/users/:id/followers

Returns followers list with total follower count.

Activity History

GET /api/users/:id/activity

Tracks posts, likes, and follow/unfollow activity.

** Getting Started

Clone the repository:

git clone https://github.com/Mahiisss/Social-media-backend-api.git
cd Social-media-backend-api


Install dependencies:

npm install


Run migrations:

npm run migration:run


Start the server:

npm run dev


Server runs at:

http://localhost:3000

🧪 Testing (Windows)

Run the interactive PowerShell script:

Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\test.ps1


This will test all CRUD operations and special endpoints.

** Migration Commands
npm run migration:generate
npm run migration:run
npm run migration:revert
























