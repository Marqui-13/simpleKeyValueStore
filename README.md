# Simple Key-Value Store Chaincode for Hyperledger Fabric

This repository contains a simple chaincode (smart contract) written in Go for Hyperledger Fabric. It implements a basic key-value store, allowing users to set and retrieve values associated with specific keys. This example serves as a foundational piece for understanding how to develop and deploy chaincodes in a Hyperledger Fabric network.

## Prerequisites

- Go programming language (version 1.13 or newer)
- Hyperledger Fabric network setup

## Installation

1. Clone this repository into the `src` folder of your `$GOPATH` to ensure it is properly recognized by Go:


git clone https://github.com/Marqui-13/simple-key-value-chaincode.git $GOPATH/src/simple-key-value-chaincode


2. Navigate to the cloned repository directory:


cd $GOPATH/src/simple-key-value-chaincode


## Deployment

To deploy this chaincode to your Hyperledger Fabric network, follow the standard chaincode installation and instantiation procedures provided in the Hyperledger Fabric documentation. This typically involves:

- Packaging the chaincode
- Installing the chaincode on your peer(s)
- Instantiating the chaincode on your channel

## Chaincode Functions

- `set`: Stores a key-value pair in the ledger. Expects two arguments: the key and the value.
- `get`: Retrieves the value associated with a key from the ledger. Expects one argument: the key.

## Usage

After deploying the chaincode to your Fabric network, you can interact with it using the Fabric peer CLI or SDKs:

- To set a value:


peer chaincode invoke -n mycc -c '{"Args":["set", "myKey", "myValue"]}' -C mychannel


- To get a value:


peer chaincode query -n mycc -c '{"Args":["get", "myKey"]}' -C mychannel


## Contributing

We welcome contributions to enhance this simple chaincode or improve the documentation. Please feel free to fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Hyperledger Fabric community for their extensive documentation and examples.