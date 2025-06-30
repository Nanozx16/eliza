# eliza

 Features
🛠️ Full-featured Discord, Twitter and Telegram connectors
🔗 Support for every model (Llama, Grok, OpenAI, Anthropic, etc.)
👥 Multi-agent and room support
📚 Easily ingest and interact with your documents
💾 Retrievable memory and document store
🚀 Highly extensible - create your own actions and clients
☁️ Supports many models (local Llama, OpenAI, Anthropic, Groq, etc.)
📦 Just works!
Video Tutorials
AI Agent Dev School

🎯 Use Cases
🤖 Chatbots
🕵️ Autonomous Agents
📈 Business Process Handling
🎮 Video Game NPCs
🧠 Trading
🚀 Quick Start
Prerequisites
Python 2.7+
Node.js 23+
pnpm
Note for Windows Users: WSL 2 is required.

Use the Starter (Recommended)
git clone https://github.com/elizaos/eliza-starter.git
cd eliza-starter
cp .env.example .env
pnpm i && pnpm build && pnpm start
Once the agent is running, you should see the message to run "pnpm start:client" at the end. Open another terminal and move to same directory and then run below command and follow the URL to chat to your agent.

pnpm start:client
Then read the Documentation to learn how to customize your Eliza.

Manually Start Eliza (Only recommended if you know what you are doing)
# Clone the repository
git clone https://github.com/elizaos/eliza.git

# Checkout the latest release
# This project iterates fast, so we recommend checking out the latest release
git checkout $(git describe --tags --abbrev=0)
# If the above doesn't checkout the latest release, this should work:
# git checkout $(git describe --tags `git rev-list --tags --max-count=1`)
Start Eliza with Gitpod
Open in Gitpod

Edit the .env file
Copy .env.example to .env and fill in the appropriate values.

cp .env.example .env
Note: .env is optional. If you're planning to run multiple distinct agents, you can pass secrets through the character JSON

Automatically Start Eliza
This will run everything to set up the project and start the bot with the default character.

sh scripts/start.sh
Edit the character file
Open packages/core/src/defaultCharacter.ts to modify the default character. Uncomment and edit.

To load custom characters:

Use pnpm start --characters="path/to/your/character.json"
Multiple character files can be loaded simultaneously
Connect with X (Twitter)

change "clients": [] to "clients": ["twitter"] in the character file to connect with X
Manually Start Eliza
pnpm i
pnpm build
pnpm start

# The project iterates fast, sometimes you need to clean the project if you are coming back to the project
pnpm clean
Additional Requirements
You may need to install Sharp. If you see an error when starting up, try installing it with the following command:

pnpm install --include=optional sharp

