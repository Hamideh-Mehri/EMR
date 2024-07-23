### Creating EC2 key pair

An Amazon EC2 key pair is a set of security credentials that you use to prove your identity when connecting to an Amazon EC2 instance. EC2 key pairs consist of a public key and a private key. Here's how they work:

* Creation: When you create a key pair using AWS, the system generates a public key and a private key. The public key is stored on AWS, and you are given the private key, which you must save securely. The private key file is provided in a .pem format for Linux-based instances or .ppk format for Windows-based instances.

* Public Key: This key is automatically installed in any EC2 instance you launch that specifies the key pair. The public key is stored in the .ssh/authorized_keys directory on a Linux/UNIX instance, enabling the matching private key holder to access the instance.

* Private Key: You keep this key to yourself and use it to access the instance. For security, the private key is not retrievable if lost. It's used with SSH (Secure Shell) for Linux or macOS or with PuTTY for Windows to securely access instances.

* Security: It's crucial to keep your private key secure. If someone else obtains your private key, they can launch and access instances in your account. Similarly, if you lose the private key, you cannot access the instance through SSH.

* Use Case: When you want to log into your instance, you use an SSH client configured with your private key. The client uses this key to authenticate with the instance, which has the corresponding public key.

The key pair is fundamental for securely managing access to your instances, ensuring that only those with the proper private key can connect to them.
