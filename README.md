# jDownloader

Run jDownloader inside the Docker container.

## How to Use

Create an .env file (optional but recommended) in the same directory as your docker-compose.yml:

```bash
# MyJDownloader Account Settings
MYJD_EMAIL=your_email@example.com
MYJD_PASSWORD=your_myjdownloader_password
MYJD_DEVICE=your_device_name

# VNC Password for Web UI Access
VNC_PASSWORD=your_secure_vnc_password

# Download Directory Path on Host
DOWNLOAD_DIR=/mnt/DATA/Downloads

# OpenVPN Settings
VPN_OVPN_PATH=/absolute/path/to/your/config.ovpn  # e.g., /home/username/vpn/config.ovpn

# Make sure that you have this in it:
# auth-user-pass /vpn/vpn.auth <-------------------------------------------------------- !!! 
# ---------------------------------------------------------------------------------------

VPN_USERNAME=your_vpn_username
VPN_PASSWORD=your_vpn_password
```

Replace the placeholders with your actual values. This file should be kept secure and not shared.

Then, run the container:

```bash
./start
```
