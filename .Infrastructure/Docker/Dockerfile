FROM node

# install dependencies
WORKDIR /app
COPY package.json ./
RUN npm install

FROM node

WORKDIR /app
COPY --from=0 /app .
COPY . .

EXPOSE 5000
