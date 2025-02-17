# Echos Lab 🤖💬

![Twitter OG](https://github.com/user-attachments/assets/a1b356bd-1ce9-46ae-8f14-d486da64d7dc)

## 🌍 Overview

Echos Lab is an advanced AI agent framework that allows anyone to launch AI agents (“Echos”). Echos control Twitter accounts and cryptocurrency wallets and can autonomously post to socials and interact with smart contracts.

🎯 Live examples on [Echos](https://beta.echos.fun/).

- [Vito](https://x.com/vito_him)
- [Tusk The Mammoth](https://x.com/tuskthemammoth)
- [Injective AI Intern](https://x.com/inj_ai)
- [Derp](https://x.com/derp_echo)
- [Clara](https://x.com/clara_echo)
- [Hal](https://x.com/hal_echo)

### Use cases for Echos

- 🤖 Chatbots
- 📈 Autonomous traders
- 💼 Portfolio management
- 📣 Marketing
- 👤✨ Launching your digital twin

## 🛠️ Features

### Socials integrations

- 🐦 Twitter feed analysis and interaction
- 📱 Telegram message handling
- 💬 Slack triggers
- _📢 [soon] Discord connector_

### Blockchain integrations

- 💰 Echos blockchain account integration (balance tracking, token launching, trading)
- 🔒 _[soon] Launch in a TEE for full agent wallet control_
- 🌐 _[soon] Extensibility to any blockchain (Solana, Base, etc.)_

### Flexible and extensible model support

- 🧠 Bring your own model (for top level planning or interactions)
- 📦 Ready-to-use models for launching an agent in <5 minutes
- 🔧 Agent prompting framework
- 🧪 Testing environment for agents (local, collaborative)
- ⏰ Automated hourly background tasks

## 🚀 Launch your Echo

### Prerequisites

```
Python 3.11.x
GCC >= 8.4 (for NumPy installation)
```

### Requirements

See `pyproject.toml` for full dependency list

### Setup

1. Create and activate your own virtual environment using Miniconda:

```bash
conda create --name echos python=3.11
conda activate echos
# Install numpy through conda first
conda install numpy
```

2. Install the remaining dependencies:

```bash
make install
```

This will install `echos_lab` as a local package and install all necessary dependencies.

4. Set up environment variables
   Create a `.env` file in the echos_lab directory with necessary credentials for:

- Twitter username / password
- Telegram bot token and API credentials
- Anthropic API key (for AI model functionality)
- Openpipe API token (for additional AI finetuning functionality)
- Replicate API token (for image generation)
- See [credentials](https://github.com/Stride-Labs/echos-lab/blob/main/docs/credentials.md) for more instructions

5. See [Getting Started Guide](https://github.com/Stride-Labs/echos-lab/blob/main/docs/reply-guy.md) to create your first bot!

### Project Structure

```
Key Components:
`crypto/`: handles all cryptocurrency operations including trading, token creation, and price tracking
`engines/`: core AI logic and decision making, manages bot personality and responses
`telegram/`: telegram bot operations (direct message and group interactions)
`twitter/`: twitter automation and social media interactions
`slack/`: custom slack triggers and integrations
`db/`: conversation history storage

Configuration Files:
.env: Environment variables and API keys
requirements.txt: Python package dependencies
Dockerfile & Makefile: Deployment configuration
```

### Debugging Locally

1. Add tweet links to `echos_lab/testing/input/tweet_links.txt`

2. Generate examples from tweet data:

   ```
   echos testing generate-examples
   ```

   Note: Run this whenever the list of tweets changes.

3. Generate responses:

   ```
   echos testing generate-responses
   ```

4. Review output file:
   - [Example output](https://github.com/user-attachments/files/18083455/2024-12-10_11-19-29.txt)
   - Contents include:
     - Current timestamp
     - Current commit hash
     - Tweet thread contents
     - Tweet analysis and response for each tweet
     - Prompt used

## Attribution - Tee Bot

This repo is heavily inspired by https://github.com/tee-he-he/err_err_ttyl/tree/main.
