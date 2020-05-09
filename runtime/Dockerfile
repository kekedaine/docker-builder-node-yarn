FROM node:12-alpine

EXPOSE 3000
WORKDIR /app

ONBUILD COPY --from=builder /app .
ONBUILD ADD . /app
ONBUILD RUN yarn build

CMD ["yarn", "start"]