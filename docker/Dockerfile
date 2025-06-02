FROM node:22.14.0-slim

WORKDIR /usr/divaclient

COPY . .

RUN npm ci --only=production

ENV NODE_ENV=production

RUN useradd -m divauser
USER divauser

CMD ["npm", "run", "start"]