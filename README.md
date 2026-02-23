🐳 Dockerized MERN Image CRUD System
A production-ready Full-Stack application built with the MERN stack, fully containerized using Docker, and integrated with Cloudinary for professional cloud image management.

🚀 Overview
This project serves as a comprehensive implementation of Docker orchestration. It demonstrates how to decouple a full-stack application into micro-services (Frontend, Backend, and Database) that communicate seamlessly within a virtualized network.

🛠️ Tech Stack
Frontend: React.js, React Router, Bootstrap.

Backend: Node.js, Express.js.

Database: MongoDB.

DevOps/Infrastructure: Docker, Docker Compose, Nginx.

Cloud Storage: Cloudinary API.

🐳 Docker Features Implemented
Multi-Stage Builds: Optimized Dockerfiles for smaller, faster images.

Service Orchestration: Unified management of 3+ services using docker-compose.

Networking: Custom bridge network for secure inter-container communication.

Data Persistence: Docker Volumes used to ensure MongoDB data survives container restarts.

Environment Injection: Dynamic configuration via .env files.


Shutterstock
استكشاف
📋 Prerequisites
Docker and Docker Compose installed.

Cloudinary account (for API keys).

⚙️ Installation & Setup
Clone the repository:

Bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
Environment Variables:
Create a .env file in the backend directory:

مقتطف الرمز
MONGO_URI=mongodb://db:27017/mern_db
CLOUD_NAME=your_cloud_name
API_KEY=your_api_key
API_SECRET=your_api_secret
Run the Application with Docker:

Bash
docker-compose up -d --build
Access the app:

Frontend: http://localhost:8080

Backend API: http://localhost:5005

🏗️ Architecture Detail
frontend/: Contains the React code. Served by Nginx in production mode.

backend/: Node.js server handling Multer uploads and Cloudinary logic.

db: Persistent MongoDB instance.

🔧 Troubleshooting & Lessons Learned
Time Sync: Solved "Stale Request" errors with Cloudinary by synchronizing the host/container system clock using ntpdate/chrony.

Network Bridging: Resolved communication issues between React (client-side) and Express (container-side) by properly mapping ports and environment URLs.

Permission Handling: Configured Docker volumes with correct Linux permissions for seamless database writes.

🤝 Contributing
Feel free to fork this project, open issues, or submit pull requests to help improve the Docker configuration or add new features!
