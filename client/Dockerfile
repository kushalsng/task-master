FROM node:18-alpine

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

# Expose the port that the client will run on
EXPOSE 5173

CMD [ "npm", "run","dev" ]

# # Stage 1: Build the React app
# FROM node:17-alpine AS build
# WORKDIR /app
# COPY . .
# RUN npm install
# RUN npm run build

# # Stage 2: Serve the built app
# FROM node:17-alpine AS serve
# WORKDIR /app
# COPY --from=build /app/build /app/build
# RUN npm install -g serve

# # Expose port 80
# EXPOSE 80

# # Command to serve the built app
# CMD ["serve", "-s", "build", "-l", "80"]