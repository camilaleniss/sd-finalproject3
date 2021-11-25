# Final Project

# 1️⃣ Build the frontend and backend as Docker Hub images

```bash
# Build the image
docker build -t frontend-app .

# Tag the image
docker tag frontend-app camilaleniss/icesihealth-frontend-app

# Login to docker with your docker Id
docker login

# Push the image to docker hub
docker push camilaleniss/icesihealth-frontend-app
```

```bash
# Build the image
docker build -t backend-app .

# Tag the image
docker tag backend-app camilaleniss/icesihealth-backend-app

# Login to docker with your docker Id
docker login

# Push the image to docker hub
docker push camilaleniss/icesihealth-backend-app
```

# 2️⃣ Running the app

```bash
# Start the Docker service
sudo systemctl start docker

# Start minikube for local deployment
minikube start

# Apply the configuration in the yml of the path 
kubectl apply -f frontend-deploy.yml
kubectl apply -f database-deploy.yml
kubectl apply -f backend-deploy.yml
```