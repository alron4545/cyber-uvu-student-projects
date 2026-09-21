FROM node:18-alpine

WORKDIR /app

# Copy manifests first so the npm ci layer is cached until dependencies change.
COPY package.json package-lock.json ./
RUN npm ci

COPY . .

EXPOSE 4000

CMD ["npm", "start"]
