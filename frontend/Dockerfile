# Updated Dockerfile for the frontend (arda_case/frontend/Dockerfile)

FROM node:18

WORKDIR /app

# Copy only package.json and lock file first for better caching
COPY package*.json ./

# Clean and reinstall dependencies with compatibility mode
RUN npm install 
RUN npm install -g vite

# Copy the rest of the app
COPY . .

# Expose frontend port
EXPOSE 5174

CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
