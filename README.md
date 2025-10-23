# Flussonic-Media-Server
Flussonic-Media-Server

**To install Flussonic Media Server on Ubuntu, run the following command in your terminal:**

```bash
curl -sSf https://flussonic.com/public/install.sh | sh
```

This script automatically sets up the repository and installs the server using `apt`. After installation, you’ll need to activate Flussonic by accessing its web interface and entering your license key.

---

### 🧰 Full Installation Guide for Ubuntu

#### ✅ Prerequisites
- Ubuntu 22.04 or 24.04 (amd64 or arm64)
- Port 80 must be free (Flussonic uses it by default)
- Sufficient RAM (swap should be disabled)

#### 🛠️ Install Flussonic
```bash
apt update
apt install curl -y
curl -sSf https://flussonic.com/public/install.sh | sh

```

#### 🔑 Activate Flussonic
1. Start the server:
   ```bash
   service flussonic start
   ```
2. Open your browser and go to:
   ```
   http://your-server-ip/
   ```
3. Enter your license key and set the admin username/password.

> ⚠️ Avoid using special characters like `@`, `;`, `#`, `[`, `\\`, `/`, `=`, `$` in your login or password.

#### 🔄 Manage the Service
```bash
service flussonic start     # Start
service flussonic stop      # Stop
service flussonic restart   # Restart
service flussonic reload    # Reload config without disconnecting clients
```

#### 🔧 Change Admin Password
- **Via config file**:
  Edit `/etc/flussonic/flussonic.conf` and update the `edit_auth` directive.
  Then run:
  ```bash
  service flussonic reload
  ```
- **Via Web UI**:
  Go to **Config → Settings → Access**, enter and confirm your new password, then click **Save**.

---

Let me know if you want a Bash script to automate this setup or integrate it with SN TV or Falcon Cast App. I can also help configure stream inputs like RTMP, SRT, or IP cameras.

Source: [Flussonic Installation Manual](https://flussonic.com/doc/install-media-server/).
