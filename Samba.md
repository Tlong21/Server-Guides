
# Setting Up and Enabling Samba on Linux

This guide will walk you through starting and enabling the Samba service, as well as configuring your firewall to allow Samba traffic.

## 1. Start the Samba Service

To start the Samba service, run the following command:

```bash
sudo systemctl start smb
```

## 2. Enable Samba to Start on Boot

To ensure Samba starts automatically on boot, use the following command:

```bash
sudo systemctl enable smb
```

## 3. Allow Samba Traffic Through the Firewall

If you're using UFW (Uncomplicated Firewall), allow Samba traffic by running:

```bash
sudo ufw allow Samba
```

This will open the necessary ports for Samba, such as ports 137-139 and 445.

## 4. Reload the Firewall

Finally, reload the firewall to apply the changes:

```bash
sudo ufw reload
```

This ensures the firewall allows Samba connections.

---

Now your system should be configured to use Samba with the necessary firewall rules in place.
