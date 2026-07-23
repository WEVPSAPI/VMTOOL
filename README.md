## WeVPS Control Installation

Run the following commands as the `root` user:

```bash
wget https://github.com/WEVPSAPI/VMTOOL/raw/refs/heads/main/Tools/WeVPSControl.zip
unzip WeVPSControl.zip
cd WeVPSControl
chmod +x install-bro
bash install-bro
```

If `unzip` is not installed:

```bash
apt update && apt install unzip wget -y
```

After installation, open WeVPS Control in your browser:

```text
http://YOUR_SERVER_IP:789/login
```

### Service Management

Restart the service:

```bash
systemctl restart vmtool.service
```

Check the service status:

```bash
systemctl status vmtool.service --no-pager -l
```

View live logs:

```bash
journalctl -u vmtool.service -f
```
