# Stage 1: Build the Next.js application
FROM node:21-alpine AS build

WORKDIR /app

COPY . .

RUN npm install

RUN npm test courses
RUN npm run test:e2e

RUN npm run build

EXPOSE 8080

# Start the Next.js application
CMD ["npm", "start"]
