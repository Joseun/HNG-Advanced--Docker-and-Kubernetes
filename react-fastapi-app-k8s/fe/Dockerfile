FROM node:18-alpine

WORKDIR /app

COPY package.json ./

RUN npm install

COPY . ./

ENV REACT_APP_API_URL http//localhost:8000
ENV REACT_APP_LESSION_DAY day1

EXPOSE 3000

RUN npm ci

RUN npm run build

CMD ["npm", "run", "start"]
