FROM node:22-alpine

USER node
WORKDIR /home/node/new

COPY --chown=node:node out/package.json ./
RUN corepack prepare --activate

COPY --chown=node:node out .
RUN corepack pnpm rebuild

ENTRYPOINT ["corepack", "pnpm"]
CMD ["start"]