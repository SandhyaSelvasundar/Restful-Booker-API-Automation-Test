# Dockerfile for Node service
FROM node:14

WORKDIR /app

# Install Newman globally
RUN npm install -g newman

# Copy your application files
COPY . .

CMD ["tail", "-f", "/dev/null"]  # Keep container running
