FROM node:20-alpine

WORKDIR /opt/server

# Copy package files first for better caching

COPY package.json /opt/server/

# Clean install based on lockfile
RUN npm ci

# Copy the application code
COPY server.js /opt/server/

EXPOSE 8080

CMD ["node", "server.js"]
