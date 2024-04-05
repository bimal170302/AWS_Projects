# Accessing EC2 Linux Instance from EC2 Windows Instance.

**Objective: **To establish a connection from an EC2 Windows instance to an EC2 Linux instance for remote access and management.



**Prerequisites:**

- Access to AWS Management Console with appropriate permissions.
- EC2 instances launched and running:
    - EC2 Linux instance (e.g Amazon Linux).
    - EC2 Windows instance (running Windows Server).
**Steps: **

**Configure Security Group:**

- Ensure that the security group associated with the EC2 Windows instance allows inbound Remote Desktop Protocol (RDP) traffic (port 3389) from your IP address or IP range.
**Open Remote Desktop Client:**

- On your local machine, launch the Remote Desktop client application. This is typically available on Windows operating systems as "Remote Desktop Connection" or can be downloaded for other operating systems.
**Provide Credentials:**

- When prompted, enter the username and password associated with the EC2 Windows instance.
    - **Username:** Enter the appropriate username. For Amazon EC2 instances, this is typically `**Administrator**` .
    - **Password:** Enter the password associated with the instance. If you haven't set a custom password, use the password generated during instance launch.
**Open Command Prompt:**

- Now open cmd on windows instance and run a command 
**Connect to Linux Instance:**

- In the SSH client, enter the following command to connect to the EC2 Linux instance:
```
ssh -i"Key.pem"@ip_address
```
**Authenticate Connection:**

- If connecting for the first time, you may be prompted to confirm the SSH fingerprint. Enter `**yes**`  to continue connecting.
1. **Provide Credentials:**
    - Enter the password or SSH key passphrase associated with the specified username to authenticate the connection to the EC2 Linux instance.
2. **Access Linux Instance:**
    - Once authenticated, you will have remote shell access to the EC2 Linux instance from within the EC2 Windows instance.
**Conclusion:** You have successfully established a connection from an EC2 Windows instance to an EC2 Linux instance, allowing remote access and management of the Linux environment from within the Windows environment.

**Notes: **

- Ensure proper security measures are in place, such as using SSH key pairs for authentication and restricting SSH access to specific IP addresses or IP ranges.
- Regularly review and update security group rules to maintain a secure network environment.
- Ensure that RDP access is limited to authorized users and IP addresses through proper security group configuration.
- Regularly review and update security group rules to maintain a secure network environment.
- Use strong passwords and consider implementing multi-factor authentication for enhanced security.


