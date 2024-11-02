# Astro app stage
FROM node:18-alpine AS astro
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install
COPY . .
RUN npm run build

# Secondary app stage
FROM node:18-alpine AS secondary
WORKDIR /app-secondary
COPY package-secondary.json package-lock-secondary.json ./
RUN npm install
COPY . /app-secondary
