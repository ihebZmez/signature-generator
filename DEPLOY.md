## Step 1 — build locally

npm run build

## Step 2 — send ONLY dist

scp -r dist docker ihebzmcfac@10.0.1.118:/home/ihebzmcfac/

## Step 3 — run on VM

cd /opt/signature-generator-cfac-group
mv /home/ihebzmcfac/dist /opt/signature-generator-cfac-group/
mv /home/ihebzmcfac/docker /opt/signature-generator-cfac-group/

## Step 4 — build application on vm

```bash
docker compose down
docker compose up -d --build
```