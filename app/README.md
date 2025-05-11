# Library Management System (MERN)

A MERN stack application for managing library operations, deployed on Kubernetes with Minikube.

## Running Instructions
1. Clone the repository: `git clone https://github.com/<your-username>/library-management-k8s.git`
2. Install dependencies: `yarn` in `app/backend` and `app/frontend`.
3. Set up MongoDB and update `app/backend/.env` with `MONGO_URL`.
4. Build Docker images: `docker build -t <username>/library-backend:latest ./app/backend` and `docker build -t <username>/library-frontend:latest ./app/frontend`.
5. Deploy to Minikube: `kubectl apply -f k8s/deployment.yaml` and `kubectl apply -f k8s/service.yaml`.
6. Access: `minikube service library-frontend-service`.
