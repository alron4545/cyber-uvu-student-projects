# Vite 8 requires Node 20.19+ or 22.12+, so this uses a newer base than the API.
FROM node:22-alpine

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci

COPY . .

EXPOSE 5173

# --host 0.0.0.0 makes the dev server reachable from outside the container.
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
