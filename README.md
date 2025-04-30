# CryptoSun-Devtools
scripts for devs to interact with your contracts or localnet. CryptoSun DevTools provides developers with everything needed to test, debug, and interact with the CryptoSun protocol's Solana smart contracts in development environments. These tools simplify local development workflows and enable rapid iteration when building on the CryptoSun ecosystem.

# Features
* Local Environment Setup: Scripts to quickly configure a Solana localnet with CryptoSun contracts
* Contract Interaction: CLI tools to call and test contract functions
* Test Data Generation: Utilities to generate realistic test data for the DePIN system
* Transaction Simulation: Tools to simulate complex transaction sequences
* Debugging Utilities: Helpers for tracing and debugging contract execution
* Migration Scripts: Tools for upgrading between contract versions in development

# Installation

    bash
    # Clone the repository
    git clone https://github.com/cryptosun/cryptosun-devtools.git
    cd cryptosun-devtools
    
    # Install dependencies
    yarn install

    # Build the tools
    yarn build

# Quick Start

    # Start a local Solana validator with CryptoSun programs deployed
    yarn start:localnet

    # In a new terminal, initialize test environment with sample data
    yarn init:testdata

    # Interact with the token contract
    yarn run:token-script --action transfer --amount 100 --to <RECIPIENT_ADDRESS>

# Scripts
<h2>Setup Scripts</h2>
* setup-localnet.sh - Configures and starts a local Solana validator with CryptoSun programs
* reset-localnet.sh - Resets the local validator state
* setup-testnet.sh  - Deploys programs to Solana testnet for integration testing

<h2>Contract Interaction Scripts</h2>
* token-cli.js - Interact with the CSN token program (transfer, mint, burn)
* staking-cli.js - Manage staking operations (stake, unstake, claim rewards)
* energy-marketplace-cli.js - Simulate energy trading on the marketplace
* governance-cli.js - Create and vote on governance proposals

<h2>Utility Scripts</h2>
* generate-keypairs.js - Create and manage Solana keypairs for testing
* airdrop.js - Airdrop SOL and CSN tokens to test accounts
* simulate-energy-production.js - Generate simulated energy production data
* transaction-explorer.js - View detailed information about transactions

# Environment Configuration
<h2>Create a .env file in the project root:</h2>

    # Network settings
    SOLANA_RPC_URL=http://localhost:8899
    NETWORK=localnet

    # Contract addresses (only needed for testnet/devnet)
    TOKEN_PROGRAM_ID=
    STAKING_PROGRAM_ID=
    ENERGY_ORACLE_PROGRAM_ID=

    # Development settings
    LOG_LEVEL=debug

# Common Workflows
<h2>Setting up a Development Environment</h2>
    
    # Start from a clean state
    ./scripts/reset-localnet.sh

    # Deploy contracts and initialize state
    ./scripts/setup-localnet.sh

    # Generate test keypairs
    node scripts/generate-keypairs.js --count 5

    # Airdrop tokens to test accounts
    node scripts/airdrop.js --accounts test-accounts.json

<h2>Simulating</h2>

    # Generate sample energy production data
    node scripts/simulate-energy-production.js --days 7 --units 10

    # Register simulated mining hardware
    node scripts/mining-registry-cli.js --action register --count 5

    # Process simulated mining rewards
    node scripts/process-mining-rewards.js --cycle-days 1

# Debugging
<h2>Transaction Inspection</h2>

    # View detailed transaction information
    node scripts/transaction-explorer.js --signature <TRANSACTION_SIGNATURE>

# Contract Logs

    # Stream program logs
    solana logs --url localhost:8899 <PROGRAM_ID>

# Contributing
We welcome contributions to improve these development tools! Please check our <a>Contributing Guidelines</a> before submitting pull requests.

# Development Workflow

    Fork the repository
    Create your feature branch (git checkout -b feature/new-script)
    Commit your changes with descriptive commit messages
    Push to your branch
    Open a Pull Request

# Troubleshooting
<h2>Common Issues</h2>

    RPC Connection Errors: Ensure your local validator is running with solana-test-validator --log
    Program Loading Failures: Check that program IDs match in your environment configuration
    Transaction Simulation Errors: Verify account permissions and token balances

<h2>Getting Help</h2>

If you encounter issues not covered here, please:
  Check the Issues section for similar problems
  Join our Discord developer channel

# License
This project is licensed under the Apache License 2.0 - see the <a>LICENSE</a> file for details.

