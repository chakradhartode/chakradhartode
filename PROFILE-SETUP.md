# Install your GitHub profile

This ZIP is a **GitHub profile README**, not a replacement for your FlashKit repository.

## What it contains
- `README.md` — the profile page content
- `assets/chakradhar-banner.svg` — custom original banner
- `PROFILE-SETUP.md` — these publishing instructions

## Publish from Termux

1. Make sure GitHub CLI is logged in as `chakradhartode`:
   ```bash
   gh auth switch --hostname github.com --user chakradhartode
   gh api user -q .login
   ```
   The output must be `chakradhartode`.

2. Extract and enter the folder:
   ```bash
   mkdir -p ~/chakradhar-profile
   cd ~/chakradhar-profile
   unzip -o ~/storage/downloads/chakradhartode-github-profile.zip
   cd chakradhartode-github-profile
   ```

3. Create the special profile repository and publish:
   ```bash
   gh repo create chakradhartode --public --source . --remote origin --push
   ```

GitHub displays the README from a **public repository whose name exactly matches your username** (`chakradhartode`).

## If that repository already exists

Do not create it again. Clone it and copy the files into the clone:

```bash
cd ~
git clone https://github.com/chakradhartode/chakradhartode.git chakradhartode-profile
cp -r ~/chakradhar-profile/chakradhartode-github-profile/. ~/chakradhartode-profile/
cd ~/chakradhartode-profile
git add .
git commit -m "Create personal GitHub profile"
git push
```

If `git commit` says there is nothing to commit, the files are already up to date.

## Customize later

Edit `README.md` to add only tools, skills, and social accounts you actually use. The stats cards are optional third-party services and may sometimes be unavailable.
