🔐 **Basic Permission Symbols**

|Symbol|Meaning|
|---|---|
|`r`|Read|
|`w`|Write|
|`x`|Execute|
|`-`|No permission|
### 🧑‍🤝‍🧑 **Permission Groups**

|Group|Applies to|
|---|---|
|`u`|User (owner)|
|`g`|Group|
|`o`|Others (everyone else)|
|`a`|All (`u+g+o`)|
🛠️ **Common `chmod` Usage**
1. **Symbolic Mode**
```
chmod u+x file      # Add execute to user
chmod g-w file      # Remove write from group
chmod o=r file      # Set others to read only
chmod a+rw file     # Add read/write to all
```
2. **Numeric Mode**

| Digit | Binary | Meaning |
| ----- | ------ | ------- |
| 0     | 000    | ---     |
| 1     | 001    | --x     |
| 2     | 010    | -w-     |
| 3     | 011    | -wx     |
| 4     | 100    | r--     |
| 5     | 101    | r-x     |
| 6     | 110    | rw-     |
| 7     | 111    | rwx     |
```
chmod 755 file      # rwxr-xr-x
chmod 644 file      # rw-r--r--
chmod 770 file      # rwxrwx---
chmod 777 file      # Full access to all (not secure)
```

3. **Recursive Option**
```
chmod -R 755 directory  # Applies permissions to directory and contents
```

👑 **Ownership with `chown`**
```
chown user file             # Change owner
chown user:group file       # Change owner and group
chown -R user:group folder  # Recursively change
```

### ➕ **Special Permissions**

|Mode|Meaning|
|---|---|
|`s`|Setuid/Setgid (run as owner/group)|
|`t`|Sticky bit (only owner can delete)|
```
chmod +t /tmp            # Enable sticky bit
chmod g+s shared_folder  # Setgid for group inheritance
```

🧪 **Viewing Permissions**
```
ls -l           # List with permissions
stat file       # Detailed permission info
```
