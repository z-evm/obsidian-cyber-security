## 1. Install OpenSSH Server (on Ubuntu VM)
- [ ] Update package lists
  ```bash
  sudo apt update
  ```
- [ ] Install OpenSSH server
  ```bash
  sudo apt install openssh-server -y
  ```
- [ ] Enable and start SSH service
  ```bash
  sudo systemctl enable ssh
  sudo systemctl start ssh
  ```
- [ ] Verify SSH is running
  ```bash
  ps aux | grep sshd
  ```

---

## 2. Get the VM IP Address
- [ ] Check IP addresses
  ```bash
  ip a
  ```
- [ ] Identify Host-Only Adapter IP (e.g., `192.168.56.x`)

---

## 3. Connect from Host (Windows PowerShell)
- [ ] SSH into VM
  ```powershell
  ssh username@192.168.56.x
  ```

---

## 4. Set Up SSH Key Authentication (Recommended)
- [ ] Generate key pair on Windows host
  ```powershell
  ssh-keygen -t ed25519 -C "yourname@host"
  ```
- [ ] Copy public key to VM
  ```powershell
  type $env:USERPROFILE\.ssh\id_ed25519.pub | ssh username@192.168.56.x "mkdir -p ~/.ssh && chmod 700 ~/.ssh && cat >> ~/.ssh/authorized_keys && chmod 600 ~/.ssh/authorized_keys"
  ```
- [ ] Test login without password
  ```powershell
  ssh username@192.168.56.x
  ```

---

## 5. Configure ssh-agent on Windows (to avoid typing passphrase each time)

- [ ] Enable ssh-agent Service (Run as Administrator)
```powershell
sc.exe config ssh-agent start= auto
net start ssh-agent
```

- [ ] Add your key (Normal PowerShell)
```powershell
ssh-add $env:USERPROFILE\.ssh\id_ed25519
ssh-add -l   # verify key is loaded
```

> ✅ You will now only need to enter your key passphrase once per boot.

---

## 6. Harden SSH Configuration (on Ubuntu VM)
- [ ] Edit SSH daemon config
  ```bash
  sudo nano /etc/ssh/sshd_config
  ```
  Set these options:
  ```
  PasswordAuthentication no
  PermitRootLogin no
  ```
- [ ] Reload SSH service
  ```bash
  sudo systemctl reload ssh
  ```

---

## 7. Quality-of-Life Enhancements
- [ ] Install tmux for persistent sessions
  ```bash
  sudo apt install tmux -y
  ```
- [ ] Use `scp` for file transfer
  ```powershell
  # From host to VM
  echo "*.*    @192.168.56.20:514" > C:\Users\$USER\Documents\syslog-config.conf
  scp C:\Users\$USER\Documents\syslog-config.conf $USER@192.168.56.20:/home/$USER/
  
  # From VM to host
  scp $USER@192.168.56.20:/etc/hosts C:\Users\$USER\Documents\.
  ```

---

✅ You now have a secure and efficient SSH setup for your Ubuntu server on VirtualBox, with ssh-agent handling your key passphrase on Windows.
