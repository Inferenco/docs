# Add Nova Wallet Ecosystem Documentation

## Description

This PR adds comprehensive documentation for Inferenco's official wallet ecosystem to the Cedra docs wallet section.

## Changes Made

### New Documentation Pages

1. **`docs/getting-started/wallets/nova-wallet.md`**
   - Official Android mobile wallet for Cedra
   - Feature overview (secure storage, multi-account, biometric auth, etc.)
   - Download link: [Google Play Store](https://play.google.com/store/apps/details?id=com.inferenco.novawallet)
   - Getting started guide
   - Security features

2. **`docs/getting-started/wallets/nova-desk.md`**
   - Official desktop wallet for Windows, Linux, and Linux ARM64
   - Feature overview (secure encryption, embedded DApp browser, session management)
   - Download link: [https://inferenco.com/nova-desk](https://inferenco.com/nova-desk)
   - Platform-specific installation instructions
   - Correct vault-first workflow (Vault Selection → Create Vault with Password → Create Account)
   - Supported networks: Testnet and Devnet

3. **`docs/getting-started/wallets/nova-connect.md`**
   - Wallet adapter for dApp integration
   - Brief description of AIP-62 compliance and features
   - Quick integration code example
   - Link to official documentation: [https://inferenco.com/docs#nova-connect-introduction](https://inferenco.com/docs#nova-connect-introduction)

### Updated Files

4. **`docs/getting-started/wallets/index.md`**
   - Updated wallet list to include Nova Wallet, Nova Desk, and Nova Connect
   - Changed "two wallets" to "the following wallets"

5. **`sidebars.ts`**
   - Added navigation entries for all three new wallet pages under "Connect a Wallet"

6. **`.gitignore`**
   - Added `screenshots/` directory to ignore list

## Key Details

- **No GitHub references**: Only official Inferenco links used
- **No mainnet references**: Cedra networks listed as Testnet and Devnet only
- **Platform accuracy**: Nova Desk listed for Windows, Linux x64, and Linux ARM64 (no macOS)
- **Correct user flow**: Vault creation before account creation as per Nova Desk screenshots
- **Nova Connect**: Minimal documentation with link to official docs

## Testing

- All markdown files are valid and properly formatted
- Sidebar navigation correctly includes new entries
- All external links are valid and use HTTPS
- No broken references

## Related Links

- [Nova Wallet on Google Play](https://play.google.com/store/apps/details?id=com.inferenco.novawallet)
- [Nova Desk Download](https://inferenco.com/nova-desk)
- [Nova Connect Documentation](https://inferenco.com/docs#nova-connect-introduction)
