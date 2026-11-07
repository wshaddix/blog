---
Title: DotNetUp
Order: 5
---

DotNetUp is a tool manager for the .Net SDK and Runtime that gives a consistent experience across Windows, MacOS and Linux for .Net developers. 

Once installed, all of the .Net SDK versions can be found at the following location

+++ Linux

```bash
~/.local/share/dotnetup
```

+++ MacOS

```bash
"$HOME/Library/Application Support/dotnetup"
```

+++ Windows
```powershell
 "%LOCALAPPDATA%\dotnetup"
```
+++

The `dotnetup` executable can be found at `/home/<username>/.dotnetup/dotnetup`

Official documentation can be found at: https://learn.microsoft.com/en-us/dotnet/core/tools/dotnetup/

## Installation

### Downloading `dotnetup` executable

+++ Linux

```bash
curl -fsSL https://aka.ms/dotnetup/get-dotnetup.sh | bash
```

+++ MacOS

```bash
curl -fsSL https://aka.ms/dotnetup/get-dotnetup.sh | zsh
```
+++ Windows

```powershell
irm https://aka.ms/dotnetup/get-dotnetup.ps1 | iex
```
+++

### Making DotNetUp Available

Once you install `Dotnetup` you have to make it available in your CLI

+++ Linux

```bash
echo 'export PATH="/home/<username>/.dotnetup:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
+++

Now close your terminal and start a new session and `dotnet` along with `dotnetup` will be available.

## Usage

### One Time Initialization

The first time you run `dotnetup` you need to inialize your environment

```bash
dotnetup init
```

### List what .Net SDKs are installed

```bash
dotnetup list
```

### Update installed versions of the .Net SDKs

Each month when service & security updates come out you can keep your workstation up to date easily.

```bash
dotnetup update
```

### Target a specific version of a SDK or Runtime

```bash
dotnetup runtime install aspnetcore@10.0
```

### Installing Preview and Daily builds

You can install preview SDKs side-by-side with your stable setup

```bash
dotnetup sdk install preview
```
or
```bash
dotnetup runtime install daily
```

### Removing SDK and Runtime versions

When you no longer need a tracked channel or exact version, remove that requirement with the corresponding `dotnetup sdk uninstall` or `dotnetup runtime uninstall` command. dotnetup then cleans up the installations that are no longer needed.

### Updating **dotnetup** itself

```bash
dotnetup self update
```

## Uninstall

To remove `dotnetup` and everything that it manages, complete the following steps:

### 1. Find your installation roots

List the installation roots that `dotnetup` is tracking

```bash
dotnetup list
```

Record each installation root that isn't in the dotnetup data directory. You delete these folders in a later step

### 2. Remove the environment configuration

Remove the `PATH` and `DOTNET_ROOT` changes that dotnetup made:

```bash
dotnetup env clear
```

### 3. Delete the installation roots and data directory

Delete each installation root that you recorded in step 1.

Then delete the dotnetup data directory. This directory contains the default installation root, the manifest, the configuration file, and the download cache.

+++ Linux

```bash
rm -rf ~/.local/share/dotnetup
```

+++ MacOS

```bash
rm -rf "$HOME/Library/Application Support/dotnetup"
```

+++ Windows
```powershell
Remove-Item -Path "%LOCALAPPDATA%\dotnetup" -Recurse -Force
```
+++

### 4. Remove the `dotnetup` executable

Delete the directory that contains the dotnetup executable. By default, the download script installs dotnetup in `~/.dotnetup`. If you added this directory to `PATH` manually, remove that entry from your shell profile or from your user environment variables.

```bash
rm -rf ~/.dotnetup
```

Open a new terminal to use the updated environment.
