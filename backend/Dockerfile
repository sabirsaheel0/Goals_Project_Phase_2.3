# regular dockerfile
FROM node:16-alpine

WORKDIR /app

COPY package*.json .

RUN npm install --omit=dev

COPY . .

EXPOSE 5000

CMD [ "node","app.js" ]


# # distroless dockerfile
# FROM node:16-alpine AS build-env
# WORKDIR /app
# COPY package*.json .
# RUN npm install --omit=dev
# COPY . .

# FROM gcr.io/distroless/nodejs22-debian12
# COPY --from=build-env /app /app
# WORKDIR /app
# EXPOSE 5000
# CMD ["app.js"]