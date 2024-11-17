
# MegaCMD Guide

MegaCMD is a command-line tool for interacting with the Mega.nz cloud storage service. It allows you to manage files, sync data, and interact with your Mega account via a terminal.

## Installation

To install `megacmd` on Linux, follow these steps:

1. **Add the Mega repository**:
   For Ubuntu/Debian-based systems:

   ```bash
   sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 7F6B6119
   sudo add-apt-repository "deb https://mega.nz/linux/MEGAsync/Debian_9.0/ ./"
   sudo apt update
   ```

2. **Install MegaCMD**:

   ```bash
   sudo apt install megacmd
   ```

3. **Verify installation**:

   ```bash
   megacmd --version
   ```

## Basic Commands

### Login

To log in to your Mega account:

```bash
mega-login your-email@example.com your-password
```

### Upload a File

To upload a file to your Mega account:

```bash
mega-put /path/to/local/file /remote/path
```

### Download a File

To download a file from your Mega account:

```bash
mega-get /remote/path /path/to/local/directory
```

### List Files in a Directory

To list files in a remote directory:

```bash
mega-ls /remote/path
```

### Sync Local Folder with Mega

To sync a local directory with your Mega account:

```bash
mega-sync /local/directory /remote/path
```

### Logout

To log out from your Mega account:

```bash
mega-logout
```

## Advanced Commands

### Create a Directory

To create a new directory on Mega:

```bash
mega-mkdir /remote/path/new_directory
```

### Remove a File

To remove a file from Mega:

```bash
mega-rm /remote/path/file
```

### Check Sync Status

To check the sync status:

```bash
mega-sync-status
```

## Help and Documentation

To see a list of available commands and options:

```bash
megacmd --help
```

For more detailed documentation, you can visit the [official MegaCMD page](https://mega.nz/cmd).
