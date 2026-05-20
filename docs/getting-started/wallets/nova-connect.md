# <img src="/img/nova-ecosystem/nova-logo.png" alt="Nova Connect Logo" width="64" style={{display: 'inline', verticalAlign: 'middle', marginRight: '12px', transform: 'translateY(-2px)'}} />Nova Connect

**Nova Connect** is the official wallet adapter that enables dApps to connect with Nova Wallet (mobile) and Nova Desk (desktop). It provides a unified interface for wallet connectivity across both platforms.

## Screenshots

import LightboxGallery from '@site/src/components/LightboxGallery';

<LightboxGallery
  images={[
    { id: '1', src: '/img/nova-ecosystem/nova-connect/connect-to-nova-wallet.png', alt: 'Connect to Nova Wallet' },
    { id: '2', src: '/img/nova-ecosystem/nova-connect/nova-wallet-request.png', alt: 'Nova Wallet Request' },
    { id: '3', src: '/img/nova-ecosystem/nova-connect/external-browser-connected-nova-wallet.png', alt: 'External Browser Connected - Nova Wallet' },
    { id: '4', src: '/img/nova-ecosystem/nova-connect/connect-to-nova-desk.png', alt: 'Connect to Nova Desk' },
    { id: '5', src: '/img/nova-ecosystem/nova-connect/nova-desk-request.png', alt: 'Nova Desk Request' },
    { id: '6', src: '/img/nova-ecosystem/nova-connect/external-browser-connected-nova-desk.png', alt: 'External Browser Connected - Nova Desk' },
    { id: '7', src: '/img/nova-ecosystem/nova-connect/show-external-connections.png', alt: 'Show External Connections' },
  ]}
  thumbnailWidth="360px"
  thumbnailHeight="240px"
/>

For complete integration documentation, visit:

[**Nova Connect Documentation**](https://inferenco.com/docs#nova-connect-introduction)

## Key Features

- **AIP-62 Wallet Standard** compliance
- **Unified API** for both mobile and desktop wallets
- **Multiple Integration Methods**: Auto-register, plugin-style, or direct client
- **End-to-End Encryption** for mobile communication
- **Session Management** across page reloads

## Quick Integration

```typescript
// Side-effect import - auto-registers Nova Connect
import "@inferenco/nova-wallet-adapter/auto-register";

// Use with wallet-standard
import { getCedraWallets, connect } from "@cedra-labs/wallet-standard";

// Connect to Nova Wallet/Nova Desk
const wallets = getCedraWallets();
await connect("Nova Connect");
const wallet = wallets.find(w => w.name === "Nova Connect");
const account = await wallet.account();
```

For full details, see the [official documentation](https://inferenco.com/docs#nova-connect-introduction).
