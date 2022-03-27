FROM node:14.16.0-alpine3.13

RUN : \
    && addgroup app && adduser -S -G app app \
    && mkdir \app && chown app:app /app \
    && :
    
USER app

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

EXPOSE 3000 

CMD ["npm", "start"]

# *SAVE FOR REFERENCE*
# * functional Dockerfile for previous unit covering "docker-compose up" but, now not working for some reasen
# FROM node:14.16.0-alpine3.13

# RUN : \
#     && addgroup app && adduser -S -G app app \
#     && chown app:app /app \
#     && :

# USER app

# WORKDIR /app
# COPY package*.json ./
# RUN npm install
# COPY . .

# EXPOSE 3000 

# CMD ["npm", "start"]



# FROM node:14.16.0-alpine3.13

# RUN : \
#     && addgroup app && adduser -S -G app app \
    # && mkdir /app \ MAYBE COMMENTED
    # && chown app:app /app \ MAYBE COMMENTED
#     && :
    
# USER app

# WORKDIR /app
# COPY package*.json ./
# RUN npm install
# COPY . .

# EXPOSE 3000 

# CMD ["npm", "start"]