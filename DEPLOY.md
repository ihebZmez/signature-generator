## Step 1 — build locally

npm run build

## Step 2 — send ONLY dist

scp -r dist docker user@VM:/app/

## Step 3 — run on VM

cd /app
docker-compose up -d --build