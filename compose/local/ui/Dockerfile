FROM node:lts-alpine

# git
RUN apk update && apk upgrade && \
    apk add --no-cache bash git libsass

WORKDIR /app

COPY ./ui/package.json /app/package.json
COPY ./ui/package-lock.json /app/package-lock.json
RUN npm install

CMD ["npm", "run", "serve"]
