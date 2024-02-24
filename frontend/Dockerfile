FROM node:14.16.0-alpine3.13

RUN addgroup app && adduser -S -G app app
USER app

WORKDIR /app
COPY package*.json ./
ENV REACT_APP_API_URL=http://64.227.147.149:3001/api
RUN npm install
COPY . .

EXPOSE 3000 

CMD ["npm", "start"]