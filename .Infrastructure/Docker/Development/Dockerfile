FROM mhart/alpine-node:12

# install dependencies
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install

FROM mhart/alpine-node

WORKDIR /app
COPY --from=0 /app .
COPY . .

EXPOSE 5000
