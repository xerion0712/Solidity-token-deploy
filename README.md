# One-Click ERC20 Deployment

A streamlined factory contract for deploying ERC20 tokens with initial balance allocation to the sender. Built on Truffle Drizzle and OpenZeppelin's secure smart contract libraries.

**Technical Deep Dive**: [Read the Medium Article](https://medium.com/@NicoFrega/erc20-token-deployer-fd4b544598ab)

## Quick Start

### Prerequisites
- [MetaMask](https://metamask.io/) (browser wallet)
- [Ganache](http://truffleframework.com/ganache/) (local blockchain)

### Installation & Setup

1. **Environment Configuration**
   ```bash
   echo 'RINKEBY_PRIVATE_KEY="YOUR_PRIVATE_KEY"' > .env
   ```

2. **Local Deployment**
   ```bash
   truffle deploy --network ganache  # Deploy factory to local blockchain
   npm run start                     # Launch frontend at localhost:3000
   ```

3. **MetaMask Configuration**
   - Network: Custom RPC
   - RPC URL: `http://127.0.0.1:7545`
   - Chain ID: `5777`
   - Import Ganache account using private key

## Development Scripts

| Command | Description |
|---------|-------------|
| `npm run start` | Start development server |
| `npm run test` | Run frontend component tests |
| `npm run build` | Create production build |
| `npm run test:truffle` | Execute smart contract tests |
| `npm run coverage` | Generate test coverage report |

## Network Deployment
```bash
truffle deploy --network [network_name]
```

## Contract Addresses
- **Rinkeby Factory**: 0xc922efc865436117055608b7a908e23e75da48f0

## Troubleshooting

**Contract Address Errors**  
Clear build artifacts and recompile:
```bash
rm -rf build/contracts/*
truffle compile
```

**Test Compatibility**  
Temporarily use reactstrap 5.0.0-beta for Jest compatibility:
```json
"reactstrap": "5.0.0-beta"
```

**Background Processes**  
Terminate solidity-coverage ghost processes:
```bash
npm run stop
```

## License
MIT Licensed - See LICENSE file for details.
