# Simple Onion Routing Network

## Overview
This project is a basic implementation of an onion routing network that enhances privacy by securely transmitting messages through multiple nodes before reaching the final destination. Each message is encrypted at every hop to maintain confidentiality.

## Features
- Initialize multiple nodes and users.
- Central registry for node registration.
- Secure message transmission using encryption.
- Support for RSA and symmetric encryption.
- Message forwarding through a structured network circuit.
- API endpoints for retrieving message information.

## Project Structure
```
Simple-Onion-Routing-Network-TD4/
│── src/
│   ├── crypto.ts   # Cryptographic utilities
│   ├── network.ts  # Network routing logic
│   ├── registry.ts # Node registration handling
│── __test__/
│   ├── tests/
│   │   ├── onionRouting.test.ts  # Tests for onion routing
│── package.json
│── README.md
```

## Installation
1. Clone the repository:
   ```sh
   git clone <repository-url>
   cd Simple-Onion-Routing-Network-TD4
   ```
2. Install dependencies:
   ```sh
   npm install
   ```

## Usage
### Initializing the Network
Modify the network initialization script to start the network with a desired number of nodes and users.

### API Endpoints
The following API routes are available:
- **Node Routes:**
  - `GET /getLastReceivedEncryptedMessage`
  - `GET /getLastReceivedDecryptedMessage`
  - `GET /getLastMessageDestination`
  - `GET /getPrivateKey`
- **User Routes:**
  - `GET /getLastReceivedMessage`
  - `GET /getLastSentMessage`

## Cryptographic Functions
The cryptographic module includes:
- RSA key generation (`generateRsaKeyPair`)
- RSA encryption/decryption (`rsaEncrypt`, `rsaDecrypt`)
- Symmetric key management (`createRandomSymmetricKey`)
- Symmetric encryption/decryption (`symEncrypt`, `symDecrypt`)
- Key import/export utilities

## Running Tests
Automated tests are implemented using Jest.
Run tests with:
```sh
npm run test
```
### Test Summary
✔ **27 Passed Tests**
✎ **5 Pending Tests** (Require further implementation)

## Future Enhancements
- Complete pending test implementations.
- Strengthen security features.
- Improve message forwarding efficiency.

## License
This project is licensed under the MIT License.

