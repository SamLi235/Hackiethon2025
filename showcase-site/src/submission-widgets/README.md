# BananaStudy

A study application for banana recognition and learning.

## Description

Welcome to BananaStudy! 🍌

BananaStudy is designed to make studying more engaging by rewarding you with loot boxes that contain collectible bananas! The longer you study using the built-in timer, the higher the tier of loot box you earn when you stop the timer. Each loot box contains bananas of varying rarities, making your study sessions more rewarding.

### 🎁 Loot Box Tiers:
* 1 minute → 🥉 Bronze Loot Box
* 2 minutes → 🥈 Silver Loot Box
* 3 minutes → 🥇 Gold Loot Box
* 4 minutes → 💎 Platinum Loot Box

> **Note:** The time thresholds are intentionally short for demonstration purposes. In real-world applications, we would implement longer study periods, such as unlocking higher-tier loot boxes every 30 minutes of focused study.

### 🍌 Banana Rarities:
When you open a loot box, you'll receive a banana of a certain rarity:
* Common 🍌
* Rare 💎
* Epic ✨
* Legendary 🌟

### ⚠️ Stay Focused!
If you leave the window (switching tabs or minimizing), a 30-second countdown will start. If you don't return before the countdown ends, your timer will reset and you won't earn a loot box!

Your goal? Study, collect bananas, and see if you can unlock all 50 bananas!

## Dependencies

To run this application, you'll need to install the following dependencies:

### Server Dependencies
* express
* cors
* fs (built-in)
* path (built-in)

### Client Dependencies
* react
* react-dom
* react-timer-hook

## Installation Instructions

### Step 1: Set up the server

```bash
# Navigate to the server directory
cd showcase-site/src/submission-widgets/server

# Install server dependencies
npm install express cors

# Return to the submission-widgets
cd ..
```

### Step 2: Set up the client

```bash
# Install client dependencies
npm install react react-dom react-timer-hook
npm install -D tailwindcss postcss autoprefixer

# Return to the root directory
cd ..
```

### Step 3: Install development dependencies

```bash
# Install nodemon for development
npm install -D nodemon

# Install concurrently to run multiple commands
npm install -D concurrently
```

### Step 4: Update your package.json scripts
Add these scripts to your root package.json:

```json
"scripts": {
  "dev": "vite",
  "build": "vite build",
  "lint": "eslint .",
  "preview": "vite preview",
  "server": "node src/submission-widgets/server/server.cjs",
  "dev:server": "nodemon src/submission-widgets/server/server.cjs",
  "dev:all": "concurrently \"npm run dev\" \"npm run dev:server\""
}
```

## Running the Application
Once everything is set up, you can run the application with:

```bash
npm run dev:all
```

This will start both the React frontend and Node.js backend concurrently.

## Important Notes
1. Make sure to place your banana images in the `server/data/bananaImagines/` directory.
2. The server runs on port 3001 and the client on port 3000 by default.





