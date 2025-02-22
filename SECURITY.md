# Security Policy for LasMeta gLASM

## About LasMeta

LasMeta is the world's first AI-enhanced social VR poker gaming metaverse, developed by Bloklab Oy (Helsinki, Finland). Our platform ensures a secure, non-gambling environment where players can earn rewards through performance-based metrics.

- Website: https://lasmeta.io
- Portal: https://portal.lasmeta.io
- Developer: Bloklab Oy (EUID: FI32999875)
- Address: Itäkatu 1-5 3rd and 4th Floor, Helsinki, Finland

## Supported Versions

Currently supported versions for security updates:

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

## Security Measures

The LasMeta gLASM smart contract implements several security measures:

1. **Access Control**
   - Owner-only functions for critical operations
   - Role-based access control for administrative functions
   - Pausable functionality for emergency situations

2. **Reentrancy Protection**
   - ReentrancyGuard implementation
   - Check-Effects-Interactions pattern
   - Safe transfer implementations

3. **Integer Overflow Protection**
   - SafeMath library usage
   - Proper type casting
   - Bounds checking

4. **Gas Optimization**
   - Efficient storage usage
   - Optimized loops
   - Batch processing capabilities

5. **Emergency Controls**
   - Circuit breaker pattern
   - Emergency pause functionality
   - Token rescue capabilities

## Known Security Considerations

1. **Transfer Restrictions**
   - Tokens are non-transferable by design
   - This is intentional for the boosting mechanism

2. **Tier Management**
   - Only owner can add/modify tiers
   - Tier parameters are immutable after creation

3. **Boosting Mechanism**
   - Time-based calculations
   - Protection against timestamp manipulation

## Security Audit Status

The contract is pending a professional security audit. Current status:
- [ ] Internal review completed
- [ ] External audit scheduled
- [ ] Audit report published

## Reporting a Vulnerability

If you discover a security vulnerability, please follow these steps:

1. **DO NOT** disclose the vulnerability publicly
2. Email us at security@lasmeta.io
3. Include:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)

## Response Timeline

We will acknowledge receipt of your report within 24 hours and provide a more detailed response within 72 hours, including:
- Confirmation of the vulnerability
- Our planned actions
- Expected timeline for fix

## Bug Bounty Program

Our bug bounty program details will be announced in due time.

## Security Best Practices

When interacting with the LasMeta platform:
1. Always verify contract addresses
2. Use secure wallet implementations
3. Never share private keys
4. Monitor transactions
5. Keep software up to date

## Contact

- Security team: security@lasmeta.io
- Website: https://lasmeta.io
- Portal: https://portal.lasmeta.io
- Developer: Bloklab Oy
- Address: Itäkatu 1-5 3rd and 4th Floor, Helsinki, Finland
- EUID: FI32999875 