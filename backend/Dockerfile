# rubyのイメージ
FROM ruby:3.2.2

# 必要なパッケージのインストール
RUN apt-get update
RUN apt-get install -y build-essential

# 環境変数
ENV APP_PATH /app

# 作業ディレクトリ
WORKDIR $APP_PATH

COPY Gemfile $APP_PATH/Gemfile
COPY Gemfile.lock $APP_PATH/Gemfile.lock

RUN bundle install

CMD ["rails", "s", "-b", "0.0.0.0", "-p", "3001"]
