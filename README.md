# Linux Server Hardening on AWS EC2

## Project Overview
This project demonstrates practical Linux server security hardening on an AWS EC2 Ubuntu server. It focuses on reducing unauthorized access, strengthening SSH configuration, enabling firewall protection, and reviewing system security.

## Environment
- **Cloud Platform:** AWS EC2
- **Operating System:** Ubuntu 26.04.1 LTS
- **Firewall:** UFW
- **Remote Access:** SSH
- **Security Framework:** AppArmor

## Security Tasks Performed
- Updated available system packages and rebooted after kernel updates.
- Enabled automatic package updates.
- Enabled UFW with default incoming traffic denied and outgoing traffic allowed.
- Restricted SSH access to a configured source IP.
- Disabled SSH root login and password authentication.
- Kept public-key authentication enabled.
- Disabled X11, TCP, and agent forwarding.
- Reviewed user accounts, privileged access, and important file permissions.
- Checked listening ports, system services, and SSH login records.
- Validated SSH configuration and saved a security audit report.

## Verification
The following checks were performed:
- `sudo ufw status verbose`
- `sudo systemctl is-enabled unattended-upgrades`
- `sudo systemctl is-active ssh`
- `sudo sshd -t`
- `sudo ss -tulnp`
- `sudo aa-status`

## Outstanding Review Items
- Investigate one SSH login source that has not been confirmed.
- Review AppArmor profiles running in complain mode.
- Recheck packages deferred due to phased updates.

## Key Learning
Hands-on practice with Linux administration, SSH security, firewall configuration, package updates, access control, and system auditing on AWS EC2.

## Disclaimer
This is a learning project, not a certification of complete server security. The server configuration and outstanding review items should be assessed before production use.
