# --- Stage 1: Build & Dependency Installation ---FROM node:20-alpine AS builder
WORKDIR /usr/src/app# Copy package files first to leverage Docker layer cachingCOPY package*.json ./# Install all dependenciesRUN npm ci# Copy the rest of the application source codeCOPY . .# --- Stage 2: Production Run Environment ---FROM node:20-alpine AS runner
WORKDIR /usr/src/app# Set production environmentENV NODE_ENV=production
# Copy package filesCOPY package*.json ./# Install only production dependencies to keep the image slimRUN npm ci --only=production# Copy application files from the builder stageCOPY --from=builder /usr/src/app/server.js ./server.js# Expose the application portEXPOSE 3000# Run the app under a non-root user for AWS security best practicesUSER node
CMD ["node", "server.js"]
