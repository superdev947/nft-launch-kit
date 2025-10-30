# NFT Launch Kit

A modern, no-code solution for building Web3 NFT minting websites with TypeScript, Next.js, and Wagmi. Create professional NFT launch pages without writing smart contracts or complex blockchain code.

## 🚀 Features

- **🔗 Multi-Wallet Support**: Connect with MetaMask, Coinbase Wallet, and WalletConnect
- **⚡ Built with Next.js 12**: Server-side rendering and optimized performance
- **💎 TypeScript**: Type-safe development experience
- **🎨 Tailwind CSS**: Beautiful, responsive UI components out of the box
- **🔐 Wagmi Integration**: Powerful React Hooks for Ethereum
- **📱 Responsive Design**: Mobile-first approach for all devices
- **🎯 Modular Components**: Reusable and customizable components

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14 or higher)
- **npm** or **yarn**
- A Web3 wallet (MetaMask recommended)

## 🛠️ Installation

1. **Clone the repository**

```bash
git clone https://github.com/superdev947/nft-launch-kit.git
cd nft-launch-kit
```

2. **Install dependencies**

```bash
npm install
# or
yarn install
```

3. **Configure your environment**

Update the Alchemy API key in `pages/_app.tsx`:

```typescript
const { chains, provider, webSocketProvider } = configureChains(defaultChains, [
  alchemyProvider({ apiKey: "YOUR_ALCHEMY_API_KEY" }),
  publicProvider(),
]);
```

You can get a free API key from [Alchemy](https://www.alchemy.com/).

4. **Run the development server**

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the result.

## 📁 Project Structure

```
nft-launch-kit/
├── components/
│   ├── baseModal/          # Reusable modal component
│   ├── button/             # Button components
│   ├── connectModal/       # Wallet connection modal
│   ├── errorBoundary/      # Error handling
│   ├── layouts/
│   │   ├── footer/         # Footer component
│   │   ├── header/         # Header with wallet connection
│   │   └── pageLayout/     # Page wrapper layout
│   └── mainLayout/         # Main app layout
├── pages/
│   ├── _app.tsx           # App configuration with Wagmi
│   ├── index.tsx          # Landing page
│   └── api/               # API routes
├── public/
│   └── assets/            # Static assets (images, icons)
├── styles/
│   ├── globals.css        # Global styles
│   └── Home.module.css    # Module-specific styles
├── types/
│   └── objects.ts         # TypeScript type definitions
├── next.config.js         # Next.js configuration
├── tailwind.config.js     # Tailwind CSS configuration
└── tsconfig.json          # TypeScript configuration
```

## 🎯 Usage

### Connecting a Wallet

The application automatically provides wallet connection functionality through the `ConnectModal` component. Supported wallets include:

- **MetaMask** (Popular choice)
- **Coinbase Wallet**
- **WalletConnect**

### Customizing the Landing Page

Edit `pages/index.tsx` to customize your landing page content, including:
- Hero section text
- Call-to-action buttons
- Banner images
- Descriptions

### Adding Custom Components

All components are located in the `components/` directory. Each component is modular and can be easily customized or extended.

## 🔧 Configuration

### Wagmi Configuration

The Wagmi client is configured in `pages/_app.tsx`. You can customize:
- Supported chains
- RPC providers
- Wallet connectors
- Auto-connect behavior

### Tailwind CSS

Customize your design system in `tailwind.config.js`. The default configuration includes:
- Custom color schemes
- Typography
- Spacing utilities
- Responsive breakpoints

## 📦 Build for Production

```bash
npm run build
npm start
# or
yarn build
yarn start
```

## 🚢 Deployment

### Vercel (Recommended)

The easiest way to deploy is using [Vercel](https://vercel.com/):

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/superdev947/nft-launch-kit)

### Other Platforms

This Next.js application can be deployed to any platform that supports Node.js:
- Netlify
- AWS Amplify
- Google Cloud Platform
- Heroku

## 🛣️ Roadmap

- [ ] NFT minting functionality
- [ ] Dashboard for contract management
- [ ] Multiple theme templates
- [ ] Smart contract integration with Thirdweb
- [ ] Whitelist management
- [ ] Gasless transactions
- [ ] IPFS integration for metadata

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
