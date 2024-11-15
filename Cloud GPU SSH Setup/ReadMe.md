# Connecting to Your Ubuntu SSH Server

This guide will walk you through the steps to connect to the Ubuntu SSH server you have provisioned. Ensure you have the necessary credentials and network access to establish the SSH connection.

## Prerequisites

- **SSH Client**: Ensure you have an SSH client installed. Most Linux and macOS systems come with SSH pre-installed. Windows users can use tools like **PuTTY** or the built-in **OpenSSH** client (available on Windows 10 and later).
- **Server IP Address**: The public IP address or domain name of your Ubuntu server.
- **Username**: The username for the account you’ll use to connect (typically `ubuntu` for cloud provisioned servers).
- **SSH Key or Password**: Either a private key file (recommended) or a password for secure authentication.

## Steps to Connect

### 1. Open Terminal or SSH Client

On macOS or Linux, open the Terminal application. On Windows, either open **Command Prompt**, **PowerShell**, or **PuTTY** (if installed).

### 2. Connect Using SSH

To connect using your username and IP address, run the following command:

```bash
ssh username@your_server_ip
```

Replace `username` with your actual username and `your_server_ip` with the server's IP address. For example:

```bash
ssh ubuntu@192.168.1.10
```

### 3. Using an SSH Key for Authentication (Recommended)

If you are using an SSH key for authentication, add the `-i` flag followed by the path to your private key file:

```bash
ssh -i /path/to/your_private_key username@your_server_ip
```

Example:

```bash
ssh -i ~/.ssh/id_rsa ubuntu@192.168.1.10
```

### 4. Accept the Server's Fingerprint

On your first connection, SSH will ask you to confirm the server's fingerprint. Type `yes` and press **Enter** to add the server to your known hosts file.

```plaintext
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
```

### 5. Enter Password (if applicable)

If you are using password-based authentication, SSH will prompt you to enter the password for the specified user. Type your password and press **Enter**.

> Note: When entering your password, you won't see any characters. This is a security feature.

### 6. Successful Connection

If everything is correct, you will now be connected to your Ubuntu server. You should see a command prompt for the server, which might look something like this:

```plaintext
Welcome to Ubuntu 20.04 LTS (GNU/Linux 5.4.0-26-generic x86_64)
ubuntu@your_server_ip:~$
```

## Additional Tips

- **Use a Config File**: You can simplify your SSH command by setting up an SSH configuration file (`~/.ssh/config`) with your server details. Here’s an example:

  ```plaintext
  Host my-ubuntu-server
      HostName your_server_ip
      User ubuntu
      IdentityFile ~/.ssh/id_rsa
  ```

  Now you can simply connect by typing:

  ```bash
  ssh my-ubuntu-server
  ```

- **Transfer Files Using SCP**: To copy files to or from the server, use `scp` (Secure Copy Protocol). Here’s an example of copying a file from your local machine to the server:

  ```bash
  scp /path/to/local/file username@your_server_ip:/path/to/remote/directory
  ```

- **Exit the SSH Session**: When you’re done, type `exit` and press **Enter** to close the SSH connection.

## Troubleshooting

- **Connection Timeout**: If you can’t connect, ensure the server is running, the IP is correct, and that your network allows SSH connections (port 22 by default).
- **Permission Denied**: This error typically means your username, password, or key file is incorrect. Double-check the credentials.
- **Firewall Settings**: Ensure the server firewall allows inbound SSH connections on port 22.

This guide should help you connect to your Ubuntu SSH server. If you encounter issues, verify each step and consult your server provider’s documentation for further assistance.
