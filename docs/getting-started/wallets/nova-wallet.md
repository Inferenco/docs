# <img src="/img/nova-ecosystem/nova-logo.png" alt="Nova Wallet Logo" width="64" style={{display: 'inline', verticalAlign: 'middle', marginRight: '12px', transform: 'translateY(-2px)'}} />Nova Wallet

**Nova Wallet** is the official mobile wallet for the Cedra blockchain. Available on Android, Nova Wallet provides a secure and user-friendly way to manage your digital assets, interact with dApps, and participate in the Cedra ecosystem.

## Demo

🎥 [**Watch Nova Wallet Demo Video**](https://www.youtube.com/shorts/BNZETysCRmk)

## Screenshots

### Nova Wallet Gallery

import LightboxGallery from '@site/src/components/LightboxGallery';

<LightboxGallery
  images={[
    { id: '1', src: '/img/nova-ecosystem/nova-wallet/dashboard.png', alt: 'Main Dashboard' },
    { id: '2', src: '/img/nova-ecosystem/nova-wallet/light.png', alt: 'Light Theme Dashboard' },
    { id: '3', src: '/img/nova-ecosystem/nova-wallet/dark.png', alt: 'Dark Theme Dashboard' },
    { id: '4', src: '/img/nova-ecosystem/nova-wallet/browser.png', alt: 'DApp Browser' },
    { id: '5', src: '/img/nova-ecosystem/nova-wallet/activity.png', alt: 'Activity History' },
    { id: '6', src: '/img/nova-ecosystem/nova-wallet/nft-collection.png', alt: 'NFT Collection' },
    { id: '7', src: '/img/nova-ecosystem/nova-wallet/swap.png', alt: 'Swap via Avera DEX' },
    { id: '8', src: '/img/nova-ecosystem/nova-wallet/settings.png', alt: 'Settings' },
    { id: '9', src: '/img/nova-ecosystem/nova-wallet/nft-detail.png', alt: 'NFT Detail View' },
  ]}
  thumbnailWidth="280px"
/>

## Features

### Core Features
- **Secure Storage**: Industry-standard encryption for your private keys and seed phrases
- **Multi-Account Support**: Manage up to 20 accounts from a single wallet
- **Biometric Authentication**: Face ID and Touch ID support for quick, secure access
- **Mnemonic Backup**: 12 or 24-word recovery phrases with BIP-39 standard
- **Hardware-Backed Security**: Uses Android's Secure Enclave (Keystore) for key protection

### Cedra-Specific Features
- **Full Cedra Blockchain Support**: Testnet and Devnet
- **Token Management**: View and manage all your Cedra tokens and NFTs
- **Transaction History**: Complete record of all your on-chain activity
- **Gas Customization**: Adjust gas fees for your transactions
- **Multi-Agent Transactions**: Support for complex transactions involving multiple signers
- **Avera DEX Integration**: Access Avera decentralized exchange for token swaps on Testnet

### dApp Integration
- **WalletConnect Compatible**: Seamlessly connect to Cedra dApps
- **Transaction Signing**: Sign transactions and messages directly from your mobile device
- **Expert-Safe-Protocol**: Secure communication with dApps via URI-based protocol
- **Deep Link Support**: Open dApps directly from wallet links

## Download

Get Nova Wallet for your Android device:

[**Download directly from Inferenco**](https://inferenco.com/nova-wallet)

## Getting Started

### Create a New Wallet
1. Download and install Nova Wallet from the Inferenco website
2. Open the app and tap **Create Wallet**
3. Securely store your 12 or 24-word recovery phrase
4. Verify your recovery phrase
5. Set up biometric authentication (optional but recommended)
6. Your wallet is ready to use!

### Import Existing Wallet
1. Open Nova Wallet
2. Tap **Import Wallet**
3. Enter your 12 or 24-word recovery phrase
4. Set a strong password
5. Your existing accounts will be restored

## Security

Nova Wallet implements multiple layers of security:

- **Encryption**: All sensitive data is encrypted using AES-256-GCM with PBKDF2 key derivation
- **Secure Storage**: Private keys are stored in Android's Secure Enclave (Keystore)
- **Biometric Protection**: Optional biometric authentication adds an extra layer of security
- **Auto-Lock**: Wallet automatically locks after inactivity
- **Key Escrow**: Additional protection mechanism for key management
