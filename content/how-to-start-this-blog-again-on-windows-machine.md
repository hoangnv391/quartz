---
title: How to start this blog again on a Windows machine
date: 2026-10-09
---
# Step 1: Install Git and Node.js
1. Download and install Git for Windows from https://git-scm.com/ (choose "Next" for default option)
2. Download and install Node.js version >= 22 from https://nodejs.org/ (choose LTS version).
3. Restart the computer.
4. Open **Power Shell** or **Command Prompt**, run below commands to check:
```
git --version
node -v
npm -v
```
Verify: All commands show versions (node -v shall return version >= 22.x.x)

# Step 2: Clone the repo and install libraries
1. Open PowerShell, browse to folder you want to save project, for example:
```
cd D:\Workspace\blog
```
2. Clone branch v5 from your repo:
```
git clone -b v5 https://github.com/hoangnv391/quartz.git
cd quartz
```
3. Install dependent packages:
```
npm install
```
Verify: The result indicates all package installing are success without EBADENGINE error.
# Step 3: Open Vault on Obsidian Windows
1. Download and install Obsidian for Windows from https://obsidian.md/
2. Open **Obsidian** -> Choose **"Open folder as vault"**
3. Browse to the folder, for example:
```
D:\Workspace\blog\quartz
```
# Step 4: Write post and sync on web
## Daily working process
1. Write or modify post in the folder **content/** on Obsidian.
2. Every time you want to publish to the web, open PowerShell in the quartz folder and run:
```
npx quartz sync
```
## Testing on local host
1. Open PowerShell in the quartz folder and run:
```
npx quartz build --serve
```
2. Open your browser and access below address to view the preview:
```
http://localhost:8080
```
