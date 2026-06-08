FROM node:24-alpine@sha256:2bdb65ed1dab192432bc31c95f94155ca5ad7fc1392fb7eb7526ab682fa5bf14

# Copy the package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm ci --only=production

# Copy the rest of your action's code
COPY . .

# Run `node /main.js`
ENTRYPOINT [ "node", "/main.js" ]
