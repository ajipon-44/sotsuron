# node.jsのイメージ
FROM node:latest

# 環境変数
ENV APP_PATH /app
ENV PORT 3000

# 作業ディレクトリ
WORKDIR $APP_PATH
COPY ./ $APP_PATH
RUN yarn install
RUN yarn build

EXPOSE $PORT

ENTRYPOINT ["yarn", "start"]
