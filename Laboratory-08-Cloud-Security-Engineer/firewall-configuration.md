# Firewall Configuration Guide

## Commands Used to Secure the Server

**1. Command used to allow SSH:**
```bash
sudo ufw allow ssh
```

**2. Commands used to set the Default Deny policy:**
```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

**3. Command used to allow Port 8080:**
```bash
sudo ufw allow 8080/tcp
```

### Critical Security Warning
**What happens if you enable the firewall before allowing SSH?**
If you run `sudo ufw enable` before allowing SSH, the firewall will immediately block port 22, permanently locking you out of remote administration.