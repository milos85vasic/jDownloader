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

VPN_OVPN_PATH=/absolute/path/to/your/config.ovpn  # e.g., /home/username/vpn/config.ovpn
VPN_USER=your_vpn_username
VPN_PASSWORD=your_vpn_password
```

Replace the placeholders with your actual values. This file should be kept secure and not shared.

Alternatively, set these environment variables directly in your shell before running Docker Compose:

```bash
# ...
export MYJD_EMAIL=your_email@example.com
export MYJD_PASSWORD=your_myjdownloader_password
export MYJD_DEVICE=your_device_name
export VNC_PASSWORD=your_vnc_password
export DOWNLOAD_DIR=/mnt/DATA/Downloads
# ... etc.
```

Run the container:

```bash
docker-compose up -d
```

