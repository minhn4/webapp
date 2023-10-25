# Web App

Just an web app with TypeScript and Next.js

## Docker

For local:

`export NEXT_PUBLIC_PAYPAL_CLIENT_ID=<YOUR_PAYPAL_CLIENT_ID> DATABASE_URL=<YOUR_DATABASE_URL> NEXTAUTH_SECRET=<YOUR_NEXTAUTH_SECRET> NEXTAUTH_URL=http://localhost:3000 AUTH0_ISSUER_BASE_URL=<YOUR_AUTH0_ISSUER_BASE_URL> AUTH0_CLIENT_ID=<YOUR_AUTH0_CLIENT_ID> AUTH0_CLIENT_SECRET=<YOUR_AUTH0_CLIENT_SECRET>`

`docker build -t webapp:$(git rev-parse --short=8 HEAD) --build-arg NEXT_PUBLIC_PAYPAL_CLIENT_ID=${NEXT_PUBLIC_PAYPAL_CLIENT_ID} .`

`docker run -p 3000:3000 -e DATABASE_URL=${DATABASE_URL} webapp:$(git rev-parse --short=8 HEAD)`

## docker-compose

`docker compose up -d`