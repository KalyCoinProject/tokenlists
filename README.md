# KalyChain Tokenlists

Token Lists is a specification for lists of token metadata (e.g. address, decimals, etc.) that can be used by any dApp
interfaces that needs one or more lists of tokens. Anyone can create and maintain a token list, as long as they follow
the specification. The KalySwap community invites you to add your token to our tokenlists!


## Adding Your Token to an Existing List


### General Requirements
1. Token should be verified on the [Kalyscan Explorer](https://kalyscan.io).
2. Token must be added to a list that it qualifies for:
    * **[KalySwap Tokenlist](./kalyswap.tokenlist.json)**: Token must be on the KalyChain network.


## Adding Your Token
1. Add an entry in the `tokens` field of the appropriate tokenlist. Please use the [checksum address](https://docs.ethers.io/v5/api/utils/address/#address). Here is an example using ETH:
    ```json
    {
      "chainId": 3888,
      "address": "0x89aE5C335372bF4d06ece4cEE1e92D04c3fdf1e0",
      "decimals": 18,
      "name": "Ether",
      "symbol": "ETH",
      "logoURI": "https://raw.githubusercontent.com/KalyCoinProject/tokens/main/assets/3888/0x89aE5C335372bF4d06ece4cEE1e92D04c3fdf1e0/logo_24.png"
    }
    ```
2. Update the `timestamp` field to the current timestamp.
3. Update the `version` field to adhere to semantic versioning:

    * Increment major version when tokens are removed
    * Increment minor version when tokens are added
    * Increment patch version when tokens already on the list have minor details changed (name, symbol, logo URL, decimals)

    ***Note:*** Changing a token address or chain ID is considered both a remove and an add, and should be a major version update.

## Adding Your Token Logo

Token logos are [hosted here](https://github.com/KalyCoinProject/tokens).
