FROM node:16

EXPOSE 5000

COPY package*.json .

RUN npm install

RUN npm install -g serve

COPY . .

RUN npm run build

RUN REACT_APP_BACKEND_URL=http://localhost:80 npm run build

CMD [ "serve", "-s", "-l", "5000", "build" ]