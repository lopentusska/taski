FROM node:18

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

# CMD ["npx", "-y", "http-server", "-p", "8000", "/app/build"]
CMD cp -r build result_build
