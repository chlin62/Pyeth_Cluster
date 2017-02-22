FROM ubuntu

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y npm nodejs-legacy
RUN apt-get install -y git
RUN apt-get install -y curl

RUN npm install -g grunt
RUN npm install -g pm2

RUN git clone https://github.com/EthereumEx/eth-netstats.git /var/lib/eth-netstats
WORKDIR /var/lib/eth-netstats
RUN npm update -g
RUN npm install
RUN npm install -g grunt-cli
RUN grunt all

CMD ["npm", "start"]
