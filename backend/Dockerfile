FROM node:14.16.0-alpine3.13

# "original" working RUN command otherwise no other changes to "original"
# RUN :addgroup app && adduser -S -G app app
RUN : \
    && addgroup app \
    && adduser -S -G app app \
    && mkdir \app && chown app:app /app \
    && :

USER app

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . . 

EXPOSE 3001 

CMD ["npm", "start"]