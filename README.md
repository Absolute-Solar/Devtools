# CryptoSun-Devtools

The Absolute Solar Devtools repository provides a collection of utilities, scripts, and tools that complement the Absolute Solar SDK. These tools are designed to streamline development, testing, and deployment processes for applications interacting with the CryptoSun token (CSN) and the Absolute Solar ecosystem on the Solana blockchain.
While the SDK offers core functionality for managing CSN, staking, and (future) governance and energy trading, this devtools repo includes supplementary tools such as:

1.) Scripts for setting up local Solana test environments. <br>
2.) Utilities for deploying and managing smart contracts. <br>
3.) Tools for monitoring blockchain activity and energy data. <br>
4.) Testing frameworks and mock data generators.

These tools are not essential for basic SDK usage but provide significant value for developers looking to optimize their workflows, test thoroughly, or automate repetitive tasks.

# Tools Included

1.) Local Testnet Setup: Scripts to quickly spin up a local Solana testnet for development and testing. <br>
2.) Smart Contract Deployment: Utilities to deploy and manage Absolute Solar's Rust-based smart contracts. <br>
3.) Monitoring Tools: Scripts to monitor blockchain activity, staking rewards, and energy production data. <br>
4.) Testing Utilities: Mock data generators and testing frameworks to simulate real-world scenarios. <br>
5.) Energy Data Simulators: Tools to simulate solar energy production and consumption for testing energy trading features.

# Installation
To use the tools in this repository, follow these steps:

### 1.) Clone the Repository:

    git clone https://github.com/AbsoluteSolarCrypto/absolute-solar-devtools.git
    cd absolute-solar-devtools


### 2.) Install Dependencies:

1.) Ensure you have Rust and Cargo installed. <br>
2.) Install Solana CLI Tools. <br>
3.) Run cargo build to compile the tools.

### 3.) Configure Environment:

Set up environment variables as needed (e.g., SOLANA_RPC_URL for connecting to a specific Solana network).


# Usage
Local Testnet Setup
To set up a local Solana testnet:

    ./scripts/setup_testnet.sh

This script initializes a local validator and configures it for development.

### Smart Contract Deployment
To deploy a smart contract:

    cargo run --bin deploy_contract -- --contract-path /path/to/contract.so --keypair /path/to/keypair.json

Replace /path/to/contract.so with the path to your compiled contract and /path/to/keypair.json with your Solana keypair.

### Monitoring Tools
To monitor staking rewards:

    cargo run --bin monitor_staking -- --wallet <YOUR_WALLET_ADDRESS>

This tool fetches and displays real-time staking reward data for the specified wallet.

### Testing Utilities
To generate mock energy data for testing:

    cargo run --bin generate_mock_data -- --output mock_energy_data.json

This creates a JSON file with simulated energy production and consumption data.

# Contributing
We welcome contributions to the Absolute Solar Devtools! To contribute:

1.) Fork the Repository: Create a personal fork of this repo. <br>
2.) Create a Branch: Work on a new feature or bug fix in a dedicated branch. <br>
3.) Submit a Pull Request: Once ready, submit a PR to the main repository.

Please review our Contributing Guidelines and Code of Conduct before contributing.

# License
This repository is licensed under the MIT License.

# Support
For questions or assistance, contact us at nick@solarcrypto.ca or visit solarcrypto.ca.

This devtools repository is designed to evolve alongside the Absolute Solar ecosystem. Watch this repo for updates on new tools and utilities!


