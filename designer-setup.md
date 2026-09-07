# Built — New Designer Setup Skill File
# Run this once before your first website build
# Works on Mac and Windows — Claude detects your OS automatically

---

## BEFORE YOU START

You will need:
- Your Claude Code account credentials (provided by Charlie)
- Your GitHub username (provided by Charlie — you should have received an invite to built-osam)
- Your Cloudflare login details (provided by Charlie)
- 15 to 20 minutes

---

## STEP 1 — DETECT OPERATING SYSTEM

Run the following command and tell me the output:

```bash
uname -s
```

- If the output is `Darwin` — you are on a Mac. Follow the Mac steps below.
- If the command fails or returns anything else — you are on Windows. Follow the Windows steps below.

---

## MAC SETUP

### 1. Install Homebrew (Mac package manager)

Check if Homebrew is already installed:
```bash
brew --version
```

If not installed, run:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

This will prompt for your Mac password. Type it and press Enter — you will not see the characters as you type. This takes 5 to 15 minutes on a cold machine as it also installs Xcode Command Line Tools.

After installation, add Homebrew to your PATH:
```bash
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

Verify:
```bash
brew --version
```

### 2. Install GitHub CLI

```bash
brew install gh
```

Verify:
```bash
gh --version
```

### 3. Authenticate with GitHub

```bash
gh auth login
```

When prompted:
- Select: GitHub.com
- Select: HTTPS
- Select: Login with a web browser
- Copy the one-time code shown
- Press Enter — a browser window will open
- Paste the code and authorise

Verify:
```bash
gh auth status
```

You should see `Logged in to github.com as [your username]`

### 4. Verify built-osam access

```bash
gh repo list built-osam --limit 5
```

You should see a list of repositories. If you get a permissions error, tell Charlie — your GitHub invite may not have been accepted or your access level needs updating.

### 5. Install Node.js (if not already installed)

```bash
node --version
```

If not installed:
```bash
brew install node
```

### 6. Install Wrangler

```bash
sudo npm install -g wrangler
```

Enter your Mac password when prompted.

Verify:
```bash
wrangler --version
```

### 7. Authenticate Wrangler with Cloudflare

```bash
wrangler login
```

A browser window will open. Log in with the OSAM Cloudflare account credentials provided by Charlie. Click Allow.

Verify:
```bash
wrangler whoami
```

You should see the OSAM Cloudflare account name.

### 8. Save the skill file URL

Save this URL — it goes at the start of every build prompt:

```
https://raw.githubusercontent.com/built-osam/built-core/main/core-skill.md
```

### 9. Mac Setup — Final Connection Test

Run each of these checks one at a time and confirm each one passes before moving on:

**GitHub CLI:**
```bash
gh auth status
```
Expected: `Logged in to github.com as [your username]`

**built-osam organisation access:**
```bash
gh repo list built-osam --limit 3
```
Expected: A list of repositories. If you see a permissions error, tell Charlie.

**Cloudflare via Wrangler:**
```bash
wrangler whoami
```
Expected: The OSAM Cloudflare account name.

**Node.js:**
```bash
node --version
```
Expected: A version number e.g. `v24.0.0`

**Skill file accessible:**
```bash
curl -s https://raw.githubusercontent.com/built-osam/built-core/main/core-skill.md | head -5
```
Expected: The first few lines of the skill file. If you see a 404 or error, tell Charlie.

**All passing? Run this full check:**
```bash
echo "=== GitHub ===" && gh auth status && echo "=== built-osam access ===" && gh repo list built-osam --limit 3 && echo "=== Cloudflare ===" && wrangler whoami && echo "=== Node ===" && node --version && echo "=== Skill file ===" && curl -s https://raw.githubusercontent.com/built-osam/built-core/main/core-skill.md | head -3 && echo "=== ALL CHECKS PASSED - READY TO BUILD ==="
```

If every section returns a result without errors, setup is complete. Tell Charlie you are ready.
If anything fails, stop and tell Charlie exactly what failed and what the error message said.

---

## WINDOWS SETUP

### 1. Check if GitHub CLI is already installed

Open Command Prompt or PowerShell and run:
```
gh --version
```

If not installed, proceed to step 2. If installed, skip to step 3.

### 2. Install GitHub CLI

Open PowerShell as Administrator and run:
```
winget install --id GitHub.cli
```

If winget is not available, download the installer directly from:
https://github.com/cli/cli/releases/latest

Download the file ending in `_windows_amd64.msi`, run it, and follow the installer steps.

After installation, close and reopen PowerShell, then verify:
```
gh --version
```

### 3. Authenticate with GitHub

```
gh auth login
```

When prompted:
- Select: GitHub.com
- Select: HTTPS
- Select: Login with a web browser
- Copy the one-time code shown
- Press Enter — a browser window will open
- Paste the code and authorise

Verify:
```
gh auth status
```

You should see `Logged in to github.com as [your username]`

### 4. Verify built-osam access

```
gh repo list built-osam --limit 5
```

You should see a list of repositories. If you get a permissions error, tell Charlie.

### 5. Install Node.js (if not already installed)

```
node --version
```

If not installed, download and run the installer from:
https://nodejs.org/en/download

Choose the LTS version. Run the installer with default settings.

After installation, close and reopen PowerShell, then verify:
```
node --version
```

### 6. Install Wrangler

```
npm install -g wrangler
```

Verify:
```
wrangler --version
```

### 7. Authenticate Wrangler with Cloudflare

```
wrangler login
```

A browser window will open. Log in with the OSAM Cloudflare account credentials provided by Charlie. Click Allow.

Verify:
```
wrangler whoami
```

You should see the OSAM Cloudflare account name.

### 8. Save the skill file URL

Save this URL somewhere easy to access — it goes at the start of every build prompt:

```
https://raw.githubusercontent.com/built-osam/built-core/main/core-skill.md
```

### 9. Windows Setup — Final Connection Test

Run each of these checks one at a time and confirm each one passes before moving on:

**GitHub CLI:**
```
gh auth status
```
Expected: `Logged in to github.com as [your username]`

**built-osam organisation access:**
```
gh repo list built-osam --limit 3
```
Expected: A list of repositories. If you see a permissions error, tell Charlie.

**Cloudflare via Wrangler:**
```
wrangler whoami
```
Expected: The OSAM Cloudflare account name.

**Node.js:**
```
node --version
```
Expected: A version number e.g. `v24.0.0`

**Skill file accessible:**
```
curl -s https://raw.githubusercontent.com/built-osam/built-core/main/core-skill.md
```
Expected: The skill file content appears. If you see a 404 or error, tell Charlie.

**All passing? Run this full check:**
```
echo "=== GitHub ===" && gh auth status && echo "=== built-osam access ===" && gh repo list built-osam --limit 3 && echo "=== Cloudflare ===" && wrangler whoami && echo "=== Node ===" && node --version && echo "=== ALL CHECKS PASSED - READY TO BUILD ==="
```

If every section returns a result without errors, setup is complete. Tell Charlie you are ready.
If anything fails, stop and tell Charlie exactly what failed and what the error message said.

---

## IF ANYTHING GOES WRONG

Do not try to fix it yourself. Stop and tell Charlie exactly:
- What step you were on
- What command you ran
- What the error message said

Do not search for workarounds online. Do not install anything that is not listed in this guide.

---

## BUILD PROMPT TEMPLATE

Once setup is complete, every build starts with this prompt in Claude Code:

```
Read the skill file at https://raw.githubusercontent.com/built-osam/built-core/main/core-skill.md then build this website using the following brief:

[paste completed brief here]
```
