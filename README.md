# NATS: Simple Docker, Nodejs and Go example

## Overview
- simple NATS deployment for local experimentation
- NATS server running in container
- Go client as subscriber
- Node.js client as publisher

## Commands
```bash
# start container
docker-compose up -d

# install go dependencies
cd go-client-sub && \
go mod init go-client-sub && \
go get github.com/nats-io/nats.go/@latest

# run go client (subscriber)
go run main.go

# new tmux session or terminal window

# install node dependencies
cd node-client-pub && \
npm init -y && \
npm install nats

# run node client (publisher)
node index.js

# view messages in go client terminal
```
