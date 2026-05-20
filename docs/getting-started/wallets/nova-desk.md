# <img src="/img/nova-ecosystem/nova-logo.png" alt="Nova Desk Logo" width="64" style={{display: 'inline', verticalAlign: 'middle', marginRight: '12px', transform: 'translateY(-2px)'}} />Nova Desk

**Nova Desk** is the official desktop wallet for the Cedra blockchain. Built for power users and developers, Nova Desk combines enterprise-grade security with a seamless user interface.

## Demo

🎥 [**Watch Nova Desk Demo Video**](https://youtu.be/plNLLY66klU)

## Screenshots

### Nova Desk Gallery

import LightboxGallery from '@site/src/components/LightboxGallery';

<LightboxGallery
  images={[
    { id: '1', src: '/img/nova-ecosystem/nova-desk/vault-selection.png', alt: 'Vault Selection Screen' },
    { id: '2', src: '/img/nova-ecosystem/nova-desk/light-theme.png', alt: 'Dashboard - Light Theme' },
    { id: '3', src: '/img/nova-ecosystem/nova-desk/dark-theme.png', alt: 'Dashboard - Dark Theme' },
    { id: '4', src: '/img/nova-ecosystem/nova-desk/browser.png', alt: 'Integrated DApp Browser' },
    { id: '5', src: '/img/nova-ecosystem/nova-desk/send.png', alt: 'Send Tokens' },
    { id: '6', src: '/img/nova-ecosystem/nova-desk/receive.png', alt: 'Receive Tokens' },
    { id: '7', src: '/img/nova-ecosystem/nova-desk/swap.png', alt: 'Swap via Avera DEX' },
    { id: '8', src: '/img/nova-ecosystem/nova-desk/nfts.png', alt: 'NFT Gallery' },
    { id: '9', src: '/img/nova-ecosystem/nova-desk/transactions.png', alt: 'Transaction History' },
  ]}
  thumbnailWidth="800px"
/>

## Features

### Core Features
- **Multi-Platform**: Available for Windows, macOS, Linux, and FreeBSD
- **Secure Encryption**: AES-256-GCM encryption with Argon2 key derivation for superior security
- **Embedded DApp Browser**: Full-featured browser with direct bridge to connected dApps
- **Session Management**: Configurable session timeout with automatic locking

### Advanced Security
- **Vault Selection & Management**: Choose or create encrypted vault folders for wallet data
- **Brute Force Protection**: Automatic lockout after 5 failed attempts (5-minute cooldown)
- **Secure Memory Management**: Zeroized memory for sensitive data (private keys, passwords)
- **Storage Isolation**: Each account has isolated encrypted storage
- **Audit Logging**: Comprehensive security event logging for monitoring

### DApp Integration
- **Full Browser Integration**: Embedded browser with WebKitGTK
- **Bridge API**: REST API for dApp communication via local server at `http://127.0.0.1:21984`
- **Transaction Signing**: Sign and submit transactions directly from browser
- **Message Signing**: Sign arbitrary messages for authentication
- **Avera DEX Integration**: Native support for Avera decentralized exchange on Testnet

### User Experience
- **Modern UI**: Built with Dioxus framework for reactive, native-feeling interface
- **Dark/Light Theme**: Customizable theme system with beautiful designs
- **System Tray**: Minimize to system tray for quick access
- **QR Code Support**: Generate and scan QR codes for addresses and transactions
- **NFT Gallery**: Built-in NFT viewing and management with detailed views
- **Transaction History**: Detailed transaction records with filtering and pagination
- **Responsive Design**: Adapts to different window sizes and screen resolutions
- **Lock & Switch**: Lock wallet or switch vault without closing the application
- **Wallet Events Dashboard**: Real-time wallet events and community events display

## Download

Get Nova Desk for your platform:

[**Download Nova Desk**](https://inferenco.com/nova-desk)

## Supported Platforms
- Windows (x64)
- macOS (Intel)
- macOS (Apple Silicon / M1/M2/M3)
- Linux (x64)
- Linux (ARM64 / Raspberry Pi)
- FreeBSD

## Getting Started

### Installation
1. Download Nova Desk for your operating system from the link above
2. Run the installer:
   - **Windows**: Run the `.exe` installer
   - **macOS**: Extract the Zip file and move to Applications
   - **Linux x64**: Use the AppImage
   - **Linux ARM64**: Use the ARM64-specific build
   - **FreeBSD**: Use the FreeBSD-specific build
3. Launch Nova Desk from your applications menu

### Create Your First Vault and Account
1. Open Nova Desk
2. On the **Vault Selection** screen, choose a folder location for your new vault or select an existing vault
3. Click **Continue to Create or Import**
4. Enter and confirm a strong **Wallet password** to encrypt your vault data
5. Click **Continue to Account Options**
6. Choose to create a new account or import an existing one
7. If creating new: securely store your 12 or 24-word recovery phrase
8. Verify your recovery phrase
9. Your vault and first account are ready to use!

## Supported Networks

Nova Desk currently supports:
- **Testnet** - For development and testing
- **Devnet** - For early feature testing

## Security Features

### Encryption Stack
- **Key Derivation**: Argon2id with configurable parameters
- **Symmetric Encryption**: AES-256-GCM for data at rest
- **Secure Randomness**: Uses OS-provided CSPRNG

### Protection Mechanisms
- **Brute Force Protection**: 5 attempts max, 5-minute lockout with exponential backoff
- **Session Timeout**: Configurable timeout (default: 30 minutes)
- **Memory Zeroization**: Sensitive data is cleared from memory when no longer needed
- **Storage Isolation**: Each account has its own encrypted storage tree

## Avera DEX Swap

Nova Desk features native integration with **Avera DEX** on Testnet:

- Direct integration with Avera Router smart contracts
- Automatic token list fetching from Avera API
- Best quote selection from multiple fee tiers (0.01%, 0.05%, 0.1%, 0.25%, 0.3%, 1.0%)
- Auto-refreshing quotes every 10 seconds
- Stale quote protection
- Slippage tolerance controls (0.1%, 0.5%, 1%, Custom)
- Real-time price display with exchange rate

## Connecting to dApps

Nova Desk provides multiple ways for dApps to connect:

### Deep Link
```
inferenco://login?redirect=https://dapp.example.com/callback
```

### Browser Bridge
- dApps can communicate via local HTTP server at `http://127.0.0.1:21984`
- Full REST API for signing, account management, and more

### JavaScript API
```javascript
// In dApp
if (window.novaDesk) {
    const publicKey = await window.novaDesk.requestPublicKey();
    const signature = await window.novaDesk.requestSignTransaction(txPayload);
}
```

## Platform-Specific Notes

### Windows
- Uses named pipes for inter-process communication
- Native window management with winit

### macOS
- Native menu bar integration
- Uses Unix domain sockets for deep link communication
- Optimized for Apple Silicon (M1/M2/M3)

### Linux
- Requires WebKitGTK 4.1 for browser functionality
- Uses Unix domain sockets for deep link communication
- X11 backend forced for WebKitGTK compatibility
- ARM64 builds available for Raspberry Pi and other ARM devices

### FreeBSD
- Native support with platform-specific build
- Uses Unix domain sockets for deep link communication
