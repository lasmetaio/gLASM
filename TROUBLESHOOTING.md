# Troubleshooting Guide for LasMeta gLASM

This guide helps you resolve common issues you might encounter while working with the LasMeta gLASM smart contract in our AI-enhanced social VR poker gaming metaverse.

## About LasMeta

LasMeta is the world's first AI-enhanced social VR poker gaming metaverse, offering players a unique opportunity to play for free and earn rewards through performance metrics. Visit us at:
- Website: https://lasmeta.io
- Portal: https://portal.lasmeta.io

Developed by Bloklab Oy (Helsinki, Finland)
EUID: FI32999875
Best Blockchain Startup Europe 2024 by Hackernoon

## Common Issues

### 1. Compilation Errors

#### Error: HH606: The project cannot be compiled, read the error messages for details.

**Possible causes:**
- Missing dependencies
- Incorrect Solidity version
- Syntax errors

**Solutions:**
1. Install dependencies:
```bash
npm install
```
2. Check Solidity version in `hardhat.config.js`
3. Run solhint to check for syntax errors:
```bash
npm run lint
```

### 2. Deployment Issues

#### Error: Invalid nonce

**Possible causes:**
- Incorrect network configuration
- Pending transactions

**Solutions:**
1. Reset your account nonce in MetaMask
2. Wait for pending transactions to complete
3. Check network configuration in `hardhat.config.js`

#### Error: Insufficient funds

**Solutions:**
1. Ensure your wallet has enough funds for deployment
2. Check gas price settings
3. Use a faucet for testnet deployments

### 3. LasMeta Platform Integration Issues

#### Error: Portal Connection Failed

**Solutions:**
1. Verify API endpoints
2. Check authentication tokens
3. Ensure correct network selection

#### Error: Reward Distribution Failed

**Solutions:**
1. Check tier configuration
2. Verify player eligibility
3. Confirm DeFi integration settings

### 4. Testing Issues

#### Error: Test timeout

**Solutions:**
1. Increase timeout in `hardhat.config.js`:
```javascript
mocha: {
  timeout: 40000
}
```
2. Optimize test code
3. Run tests individually

#### Error: Coverage failed

**Solutions:**
1. Clear hardhat cache:
```bash
npx hardhat clean
```
2. Update solidity-coverage
3. Check for complex contract logic

### 5. Environment Issues

#### Error: Cannot find module

**Solutions:**
1. Reinstall dependencies:
```bash
rm -rf node_modules
npm install
```
2. Check package.json
3. Clear npm cache:
```bash
npm cache clean --force
```

### 6. Smart Contract Specific Issues

#### Error: Invalid tier ID

**Solutions:**
1. Verify tier exists
2. Check tier status (active/inactive)
3. Ensure tier has been started

#### Error: Boosting calculation error

**Solutions:**
1. Check timestamp calculations
2. Verify boost parameters
3. Debug with console.log

## Best Practices

1. **Always Test Locally First**
   - Use hardhat network
   - Test all functions
   - Verify gas usage

2. **Keep Dependencies Updated**
   ```bash
   npm update
   ```

3. **Regular Backups**
   - Contract addresses
   - Configuration files
   - Test data

4. **Monitor Gas Usage**
   - Use gas reporter
   - Optimize expensive functions
   - Batch operations when possible

## Debug Tools

1. **Hardhat Console**
   ```bash
   npx hardhat console --network localhost
   ```

2. **Event Logging**
   - Monitor contract events
   - Use debug events in development

3. **Network Tools**
   - Etherscan
   - Block explorers
   - Gas trackers

## Getting Help

1. Visit our website: https://lasmeta.io
2. Check GitHub Issues
3. Join our Discord community
4. Contact our support team

## Security Considerations

1. **Never share private keys**
2. **Always verify contract addresses**
3. **Test with small amounts first**
4. **Monitor for unusual activity**

## Updates and Maintenance

1. **Regular Updates**
   - Dependencies
   - Contract implementations
   - Documentation

2. **Backup Procedures**
   - Contract data
   - Configuration files
   - Deployment records

## Contact Support

For technical support:
1. Email: support@lasmeta.io
2. Visit: https://lasmeta.io
3. Portal: https://portal.lasmeta.io
4. Developer: Bloklab Oy
5. Address: Itäkatu 1-5 3rd and 4th Floor, Helsinki, Finland
6. EUID: FI32999875 