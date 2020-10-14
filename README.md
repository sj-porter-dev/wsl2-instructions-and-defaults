# Windows Subsystem for Linux (WSL2) Instructions and Defaults

## Updating the distro

Run these two commands to first update the list of available ubuntu packages, and then update all packages with older versions.

It's a best practice to run these commands fairly regularly.

```bash
sudo apt update
sudo apt upgrade
```

## Configuring aliases and other fun stuff

The following commands will:

- Navigate to your home directory
- Create the .bashrc file if it doesn't exist (it likely does)
- Open the .bashrc file with VS Code

```bash
cd ~
touch .bashrc
code .bashrc
```

It is recommended that you paste the contents of the `.bashrc` file in this repo to the end of the (likely) pre-existing `.bashrc` file in your home directory.

## Configuring git

Git needs help authenticating in WSL2. The following command points WSL2 to your credential manager to make it easier to authenticate with git repos.

```bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```
