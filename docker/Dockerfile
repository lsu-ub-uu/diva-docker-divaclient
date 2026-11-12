FROM node:26.13.1-bookworm-slim

WORKDIR /usr/divaclient

COPY . .

RUN npm ci --only=production

ENV NODE_ENV=production

RUN useradd -m divauser && \
    chown -R divauser:divauser /usr/divaclient/dist
USER divauser

CMD ["npm", "run", "start"]