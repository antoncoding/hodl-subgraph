# Subgraph

## Deployed Subgraphs
1. [Hodl Ropsten](https://thegraph.com/explorer/subgraph/hodlmybeer/hodl-ropsten)
2. [Hodl Kovan](https://thegraph.com/explorer/subgraph/hodlmybeer/hodl-kovan)

## Install

```shell
yarn i
```

## Building the graph

```shell
# create subgraph manifest
npm run prepare:ropsten

# compile types
npm run codegen

# build subgraph
npm run build

```

## Deploy

### Get Access Token

You will need an access token for deployment. After you get that on [the graph](https://thegraph.com/explorer/dashboard), you need to run the following command before deploying.

```shell
graph auth https://api.thegraph.com/deploy/ <ACCESS_TOKEN>
```

Make sure you include the last `/` at the end of the url!

### Ropsten

```shell
npm run deploy:ropsten
```

### Kovan

```shell
npm run deploy:kovan
```

### Deploy on other networks

Then run
```shell

# create a subgraph.yaml file
mustache config/<network>.json subgraph.template.yaml > subgraph.yaml

# deploy
graph deploy --node https://api.thegraph.com/deploy/ --ipfs https://api.thegraph.com/ipfs/ <subgraph-name>
```
