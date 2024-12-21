# Setting Up SOCKS5 Proxy for qBittorrent with NordVPN

This guide explains how to configure a SOCKS5 proxy from NordVPN for qBittorrent to enhance your privacy while downloading torrents.

---

## **Step 1: Obtain Your NordVPN Service Credentials**

1. Log in to your NordVPN account at [Nord Account Dashboard](https://my.nordaccount.com/dashboard/nordvpn/manual-configuration/service-credentials/).
2. Navigate to the "Service Credentials" section.
3. Note down the following:
   - **Username**
   - **Password**

These credentials are separate from your regular NordVPN login details and are specifically used for manual configurations like SOCKS5.

---

## **Step 2: Enable SOCKS5 Proxy in qBittorrent**

1. Open qBittorrent.
2. Go to **Tools > Options**.
3. Select the **Connection** tab.
4. Under **Proxy Server**, configure the following settings:

   - **Type**: `SOCKS5`
   - **Host**: `us.socks.nordhold.net`
   - **Port**: `1080`
   - Check the following boxes:
     - `Use proxy for peer connections`
     - `Authentication`
   - Enter your **NordVPN service username** and **password** from Step 1.

5. Click **OK** to save the changes.

---

## **Step 3: Verify the Proxy Configuration**

1. Visit [ipleak.net](https://ipleak.net/) while qBittorrent is running.
2. Ensure your IP address matches the NordVPN proxy, confirming the proxy is working correctly.

---

## **Additional Notes**

- **Important**: SOCKS5 proxies do not encrypt your traffic. For full encryption, consider using a VPN alongside the proxy.
- If you encounter issues, double-check your credentials and ensure your NordVPN subscription is active.
- Restart qBittorrent after applying the settings to ensure they take effect.

---

This setup enhances your privacy by hiding your IP address during torrenting. For further assistance, refer to the [NordVPN Proxy Setup Guide](https://support.nordvpn.com/hc/en-us/articles/20195967385745-NordVPN-proxy-setup-for-qBittorrent).
