# Accessing Private GitHub Repositories from Another Machine

When a GitHub repository is set to **private**, anonymous clones and simple password authentication are rejected. You must authenticate your identity before Git will allow cloning, pulling, or pushing.

Below are the three standard ways to access your private repositories on another machine.

---

## Method 1: Using the GitHub CLI (`gh`) — Easiest & Fastest

Recommended for desktops, laptops, and developer workstations.

### 1. Install `gh` (if not already installed)
- **Debian / Ubuntu / Pop!_OS:** `sudo apt install gh`
- **Arch Linux:** `sudo pacman -S github-cli`
- **macOS:** `brew install gh`
- **Windows:** `winget install --id GitHub.cli`

### 2. Authenticate
```bash
gh auth login
```
- Select: **GitHub.com**
- Protocol: **HTTPS**
- Authenticate Git with your GitHub credentials? **Yes**
- How to authenticate: **Login with a web browser**
- Enter the one-time 8-character verification code in your browser and authorize.

### 3. Clone Your Repos
Once logged in, `gh` handles git credentials automatically:
```bash
gh repo clone gimpysticks/binfiles
gh repo clone gimpysticks/Zets
gh repo clone gimpysticks/Prompt_library
```

---

## Method 2: Using an SSH Key — Best for Servers & Headless Machines

Recommended for remote servers, VPS instances, or machines without a web browser.

### 1. Generate an SSH Key Pair
Run on the target machine:
```bash
ssh-keygen -t ed25519 -C "gimpysticks@gmail.com"
```
*(Press `Enter` to accept default path `~/.ssh/id_ed25519` and set an optional passphrase)*

### 2. View and Copy the Public Key
```bash
cat ~/.ssh/id_ed25519.pub
```

### 3. Add Key to GitHub
1. Navigate to: **[https://github.com/settings/keys](https://github.com/settings/keys)**
2. Click **New SSH key**.
3. Set a descriptive title (e.g. `Laptop`, `Workstation`, `Server-01`).
4. Paste the key content and click **Add SSH key**.

### 4. Clone via SSH
```bash
git clone git@github.com:gimpysticks/binfiles.git
git clone git@github.com:gimpysticks/Zets.git
```

---

## Method 3: HTTPS with Personal Access Token (PAT)

Standard Git HTTPS clones do **not** accept your GitHub account password. Instead, use a Personal Access Token:

1. Go to: **[https://github.com/settings/tokens](https://github.com/settings/tokens)**
2. Click **Generate new token (classic)**.
3. Check the **`repo`** scope (Full control of private repositories).
4. Copy the generated token (`ghp_...`).
5. When running:
   ```bash
   git clone https://github.com/gimpysticks/binfiles.git
   ```
   - **Username:** `gimpysticks`
   - **Password:** *Paste your Personal Access Token (PAT)*

To avoid typing the token repeatedly:
```bash
git config --global credential.helper cache
# Or store permanently in ~/.git-credentials:
# git config --global credential.helper store
```

---

## Summary Reference Table

| Method | Best For | Pros | Setup Effort |
| :--- | :--- | :--- | :--- |
| **`gh auth login`** | Personal laptops / desktops | Fast browser sign-in; auto-configures Git | 1 minute |
| **SSH Key** | Servers, Raspberry Pi, VPS | Key-based authentication; no web prompt needed | 2 minutes |
| **HTTPS + PAT** | Restricted environments | Works when SSH/CLI cannot be installed | 2 minutes |
