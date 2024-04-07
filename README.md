# Cross-Chain ICO with Vesting (Ethereum & Solana)

This repository contains a Proof of Concept (PoC) for a cross-chain Initial Coin Offering (ICO) / Initial Token Offering (ITO) with integrated token vesting functionality. Designed for Ethereum with extended compatibility for Solana, this project leverages the robust smart contract capabilities of Ethereum for the ICO/ITO and vesting mechanisms, integrating with Solana to broaden access and interoperability. Aimed at providing a secure and transparent investment avenue, it incorporates dynamic pricing and encourages long-term token holding.

**Notice:** The Smart Contracts / Programs provided herein have not been audited and are intended for demonstration purposes only. Users should exercise caution and conduct their own due diligence.

## Features

- **Dynamic Pricing:** Leverages Chainlink's real-time ETH/USD rates for accurate token pricing.
- **Token Vesting:** Enforces a vesting schedule on tokens purchased during the ICO to foster long-term holding.
- **Refund Mechanism:** Facilitates refunds for contributions exceeding the ICO cap, enhancing fairness.
- **Upgradeability:** Employs the UUPS upgrade pattern, allowing seamless future updates without state loss.
- **Security Measures:** Incorporates reentrancy guards and pausability features to bolster contract security.
- **Cross-Chain Compatibility:** Utilizes a bridge mechanism for token transfer and functionality between Ethereum and Solana blockchains.

## Getting Started

### Prerequisites

- Node.js (v14.x or newer)
- npm (included with Node.js)
- An Ethereum wallet with ETH for deployment
- Solana CLI for Solana deployments
- Rust for compiling Solana programs

### Installation

1. **Clone the Repository**

    ```bash
    git clone https://github.com/bark-community/smart-contracts.git
    cd smart-contracts/contracts/ico-with-vesting
    ```

2. **Install JavaScript Dependencies**

    ```bash
    npm install
    ```

3. **Environment Configuration**

    Create a `.env` file in the root directory, specifying your Ethereum node URL and private key:

    ```plaintext
    INFURA_URL="https://mainnet.infura.io/v3/YOUR_PROJECT_ID"
    PRIVATE_KEY="YOUR_PRIVATE_KEY"
    ```

### Deployment

#### Ethereum Contracts

Compile and deploy the Ethereum contracts:

```bash
npx hardhat compile
npx hardhat run scripts/deploy.js --network mainnet
```

Replace `mainnet` with your target Ethereum network.

#### Solana Programs

Compile and deploy the Solana programs:

```bash
solana program deploy /path/to/solana_program.so --url mainnet-beta
```

### Bridge Configuration

Ensure the cross-chain bridge is properly set up to recognize and manage the ICO/ITO's tokens.

## Application development

Transfer DApp USDC and other tokens on devnet / mainnet between Solana and other chains

## Usage

Participants can contribute ETH to purchase tokens, which are then subject to a vesting schedule. Tokens can be bridged between Ethereum and Solana following the bridge's procedures.

- **Ethereum:** Send ETH to purchase tokens with a vesting schedule.
- **Cross-Chain Bridge:** Bridge tokens between Ethereum and Solana.
- **Solana:** Interact with tokens within the Solana ecosystem.

[dApp]()

## Testing

Run automated tests to ensure contract reliability:

```bash
npx hardhat test
```

For Solana:

```bash
anchor test
```

## Security

This project has not undergone formal security auditing. Users and contributors should review the code thoroughly. Any discovered vulnerabilities or concerns should be reported promptly.

## Built With

- [Solidity](https://soliditylang.org/) - Ethereum smart contract development
- [Hardhat](https://hardhat.org/) - Ethereum development environment
- [OpenZeppelin Contracts](https://openzeppelin.com/contracts/) - Secure smart contract library
- [Anchor](https://github.com/coral-xyz/anchor) - Solana's framework for Solana program development
- [Solana](https://www.npmjs.com/package/create-solana-dapp) - Solana´s dapp scaffold UI framework

## Contributing

Contributions are encouraged! Please refer to [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to contribute effectively.

## License

[LICENSE.md](LICENSE.md)

## Acknowledgments

- [Chainlink](https://dev.chain.link/) for providing reliable oracle services for ETH/USD and SOL/USD price feeds.
- [Chainlink](https://github.com/smartcontractkit/ccip-starter-kit-hardhat) Chainlink Cross-Chain Interoperability Protocol (CCIP) provides a single, simple interface through which dApps and web3 entrepreneurs can securely cross-chain, including token transfers and arbitrary messaging.
- [OpenZeppelin](https://openzeppelin.com/) for their comprehensive smart contract library.
- [Anchor](https://www.anchor-lang.com/) for the development framework for Solana programs.
- [Circle](https://developers.circle.com/stablecoins/docs/cctp-getting-started?_gl=1*rl4fm4*_gcl_au*NTA4MTY3NzAyLjE3MTI0Njk1OTE.*_ga*MTgzMTY2NzQ5My4xNzEyNDY5NTkx*_ga_GJDVPCQNRV*MTcxMjQ2OTU5MS4xLjEuMTcxMjQ2OTYyOC4yMy4wLjA.) Cross-Chain Transfer Protocol (CCTP) enables USDC to flow securely between blockchains.
