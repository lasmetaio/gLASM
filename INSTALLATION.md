# Installation Guide for LasMeta gLASM

This guide will help you set up the LasMeta gLASM smart contract development environment for the world's first AI-enhanced social VR poker gaming metaverse.

## About LasMeta

LasMeta offers players the chance to play for free and earn rewards through a performance metric-based system. Unlike traditional gambling platforms, LasMeta involves no fiat currency and no financial losses. Visit us at:
- Website: https://lasmeta.io
- Portal: https://portal.lasmeta.io

Developed by Bloklab Oy (Helsinki, Finland)
EUID: FI32999875
Best Blockchain Startup Europe 2024 by Hackernoon

## Prerequisites

- Node.js (v14.x or later)
- npm (v6.x or later)
- Git

## Installation Steps

1. Clone the repository:
```bash
git clone https://github.com/lasmetaio/gLASM.git
cd gLASM
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env
```
Then edit `.env` with your actual values:
- Add your RPC URLs for different networks
- Add your private key (without 0x prefix)
- Add your Etherscan API key
- Add your CoinMarketCap API key (optional, for gas reporting)

## Compilation

Compile the smart contracts:
```bash
npm run compile
```

## Testing

Run the test suite:
```bash
npm test
```

For test coverage:
```bash
npm run coverage
```

## Deployment

1. Local deployment:
```bash
npm run deploy:local
```

2. Testnet deployment (Sepolia):
```bash
npm run deploy:sepolia
```

3. Mainnet deployment:
```bash
npm run deploy:mainnet
```

## Contract Verification

After deployment, verify your contract on Etherscan:
```bash
npx hardhat verify --network <network> <deployed-contract-address>
```

## Development

1. Start local Hardhat node:
```bash
npx hardhat node
```

2. Run tests in watch mode:
```bash
npx hardhat test --watch
```

## Integration with LasMeta Portal

For integration with the LasMeta portal (https://portal.lasmeta.io), ensure you have:
1. Proper API access
2. Required authentication tokens
3. Correct network configuration

## Troubleshooting

If you encounter any issues:

1. Make sure all environment variables are properly set
2. Try deleting the `cache` and `artifacts` folders and recompiling
3. Ensure you're using the correct Node.js version
4. Check that all dependencies are properly installed

## Security

Remember to never commit your `.env` file or expose your private keys.

## Support

For additional support:
- Visit our website: https://lasmeta.io
- Open an issue in the GitHub repository
- Contact our development team at Bloklab Oy
- Address: Itäkatu 1-5 3rd and 4th Floor, Helsinki, Finland 