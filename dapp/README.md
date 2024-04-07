# ICO/ITO Launchpad DApp

The ICO/ITO Launchpad DApp, a cutting-edge platform designed for launching and participating in Initial Coin Offerings (ICO) and Initial Token Offerings (ITO) on the Solana blockchain. This Decentralized Application (DApp) leverages React, TypeScript, and Next.js frameworks to provide a seamless, interactive, and user-friendly experience for both project creators and investors. With integrated support for Circle’s Cross-Chain Transfer Protocol (CCTP), our platform ensures secure and efficient cross-chain transactions, broadening the accessibility and utility of token sales.

## Features:

- **Dynamic ICO/ITO Launchpad:** Facilitates the creation and participation in token sales with real-time updates and transaction processing.
- **Token Vesting Schedules:** Supports customizable vesting schedules for tokens, encouraging long-term investment and project commitment.
- **Wallet Integration:** Offers comprehensive wallet support for Solana, including popular wallets like Phantom, Solflare, and more.
- **Cross-Chain Compatibility:** Utilizes Circle's CCTP for secure and streamlined cross-chain token transfers, enhancing the token's liquidity and availability.
- **Responsive UI:** Built with React and Next.js for a responsive and intuitive user interface, ensuring a great experience across all devices.
- **Security Focused:** Implements best security practices to protect transactions and user data.

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/en/) (v14.x or later)
- [npm](https://npmjs.com/) or [Yarn](https://yarnpkg.com/)
- A Solana wallet (e.g., Phantom, Solflare)

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/bark-communitu/ico-ito-launchpad-dapp.git
cd ico-ito-launchpad-dapp
```

2. **Install dependencies**

```bash
npm install
# or
yarn
```

3. **Environment Configuration**

Create a `.env.local` file at the root of your project directory and configure your environment variables. Include your Solana network endpoint and any other necessary configurations.

### Running the App

Start the development server:

```bash
npm run dev
# or
yarn dev
```

Navigate to `http://localhost:3000` to view the app.

## Usage

- **For Project Creators:** Follow the on-site instructions to initialize your ICO/ITO, set up token vesting schedules, and manage your project.
- **For Investors:** Connect your Solana wallet, browse available ICO/ITO projects, contribute to token sales, and manage your investments directly through the DApp.

## Security

Security is a top priority. The DApp integrates with Circle's CCTP for secure cross-chain transactions, alongside implementing standard security practices for smart contract development and front-end interactions. Users are encouraged to perform their due diligence and participate responsibly.

## Contributing

We welcome contributions from the community! Please read our [CONTRIBUTING.md](CONTRIBUTING.md) guide for information on how to get involved.

## License

[LICENSE.md](LICENSE.md)

## Acknowledgments

- [Chainlink](https://chain.link/) for providing reliable price feeds.
- [OpenZeppelin](https://openzeppelin.com/) for secure smart contract libraries.
- [Circle](https://developers.circle.com/docs/cctp-overview) for enabling CCTP and cross-chain transfers.