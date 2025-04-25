import { createWeb3Modal, defaultWagmiConfig } from '@web3modal/wagmi'
import { mainnet, bsc } from 'wagmi/chains'
import { ethers } from 'ethers'

// 1. WalletConnect Project ID
const projectId = 'ff2db6544a529027450c74a34fc4fb74'

// 2. Create wagmiConfig
const metadata = {
  name: 'Web3Modal Demo',
  description: 'Web3Modal + Wagmi + Ethers.js',
  url: 'https://your-site-url',
  icons: ['https://walletconnect.com/walletconnect-logo.png']
}
const chains = [bsc, mainnet]
const wagmiConfig = defaultWagmiConfig({ chains, projectId, metadata })

// 3. Create Web3Modal
createWeb3Modal({ wagmiConfig, projectId, chains })

// 4. Add a connect button to the page
const connectBtn = document.createElement('w3m-button')
document.body.appendChild(connectBtn)

// Handling the minting and wrapping functionality (as per your configuration)
