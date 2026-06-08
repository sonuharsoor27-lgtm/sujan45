The SSH Key Format
SSH relies on a key pair (a Public Key and a Private Key) for secure authentication, bypassing the need to type passwords. [1]
•	The Private Key: Kept securely on your local computer. It acts as your digital ID and should never be shared or transmitted.
•	The Public Key: Placed on the remote device you want to control. The server uses this to verify your Private Key. [1, 2, 3]
Standard SSH keys are typically formatted in OpenSSH, PEM, or PKCS#8. An OpenSSH public key format looks like this: [1, 2, 3, 4, 5]
ssh-algorithm key-data comment
Example: ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIC... user@hostname
Essential SSH Security Practices
If you are managing devices remotely, proper key maintenance and network configurations are crucial to prevent unauthorized access: [1, 2]
•	Use strong key algorithms: Generate keys using Ed25519 or high-bit (4096) RSA. [1, 2]
•	Disable password logins: Configure your server to only accept SSH keys and deny standard password entries. [1, 2]
•	Change the default port: By default, SSH runs on port 22, making it a frequent target for automated bots. Change this to a custom port in your configuration. [1, 2, 3, 4, 5]
•	Restrict Access (AllowLists): Use a firewall to only permit SSH connections from specific, trusted IP addresses. [1, 2]
•	Secure your client config: You can manage and streamline your connections (e.g., setting up automatic keys or custom ports) via the ~/.ssh/config file

