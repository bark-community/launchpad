# Creating a New Hardhat Project

This guide will help you set up a new Hardhat project, a development environment to compile, deploy, test, and debug your Ethereum software. It's designed for Ethereum developers of all skill levels, though some basic knowledge of Ethereum contracts and Node.js is helpful.

## Getting Started with Hardhat

Hardhat is a flexible, extensible framework that helps developers manage and automate the recurring tasks inherent to the process of building smart contracts and dApps.

### Prerequisites

- Node.js (v14.x or newer)
- npm (version 7 or higher recommended)

Ensure Node.js and npm are installed by running `node -v` and `npm -v` in your terminal. If not, [install Node.js](https://nodejs.org/en/download/) which includes npm.

### Step 1: Setting Up The Project

1. **Create a New Directory**

    Open your terminal and run the following commands to create a new directory and navigate into it:

    ```sh
    mkdir hardhat-test
    cd hardhat-test
    ```

2. **Initialize an npm Project**

    Initialize a new npm project by running:

    ```sh
    npm init
    ```

    You'll be prompted to answer some questions about the project. For a quick setup, you can press `Enter` to accept the default answers.

### Step 2: Install Hardhat

Now, install Hardhat in your project directory as a development dependency:

```sh
npm install --save-dev hardhat
```

### Step 3: Initialize Your Hardhat Project

In the same directory, initialize your Hardhat project:

```sh
npx hardhat init
```

Select `Create an empty hardhat.config.js` by navigating with your keyboard and hit `Enter`.

### Hardhat's Architecture

- **Tasks:** Hardhat operates through tasks. For example, `npx hardhat compile` runs the compile task. You can list all available tasks with `npx hardhat`.
- **Plugins:** Hardhat’s functionality is extended via plugins. By default, Hardhat comes with bare minimum functionality. Features are added by installing and requiring plugins.

### Step 4: Install Recommended Plugins

For development, the `@nomicfoundation/hardhat-toolbox` plugin is recommended as it includes a variety of tools:

```sh
npm install --save-dev @nomicfoundation/hardhat-toolbox
```

### Step 5: Configure Hardhat

Modify your `hardhat.config.js` to include the installed plugins and set the Solidity version:

```javascript
require("@nomicfoundation/hardhat-toolbox");

module.exports = {
  solidity: "0.8.24",
};
```

### Running Hardhat

To verify your setup, run:

```sh
npx hardhat
```

This command will list available tasks, indicating Hardhat is correctly installed.