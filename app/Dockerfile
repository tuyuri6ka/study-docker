FROM node:20.15.0

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y git vim sudo procps nkf locales && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# package.json がある場合
# RUN npm install

WORKDIR /usr/src/app

# create-react-app した後にコメントアウト（./app 配下に react project があるときに有効）
# コンテナを起動する際に実行されるコマンド
WORKDIR /usr/src/app/bulletinboard
CMD [ "sh", "-c", "yarn install && yarn start" ]
