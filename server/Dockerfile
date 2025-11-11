FROM node:18

WORKDIR /app

# Install deps using lockfile
COPY package*.json ./
RUN npm ci --omit=dev || npm install --omit=dev

# Copy the rest of the backend
COPY . .

# Your app listens on 3000
EXPOSE 3000

# Start exactly how you run it locally
CMD ["node", "server.js"]
