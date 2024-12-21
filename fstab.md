# How to Mount and Configure Drives in Linux using `fstab`

This guide provides step-by-step instructions on how to mount drives and configure them using the `fstab` file in Linux.

---

## 1. Identifying Drives

Before mounting a drive, you need to identify its partition details. Use the following command:

```bash
lsblk -o NAME,UUID,MOUNTPOINT,SIZE
```

Example output:

```plaintext
NAME        UUID                                 MOUNTPOINT   SIZE
sda                                                           1.8T
└─sda1      1bbd44e6-0dcc-4753-9cf6-99344978eee9              1.8T
sdb                                                         111.8G
└─sdb1      065cfc69-dfe6-4099-bcc2-615d135b72e8            111.8G
sdc                                                           3.6T
└─sdc1      c99bb4c1-63ae-4773-9e1a-2f976a3bdf52              3.6T
nvme0n1                                                     238.5G
├─nvme0n1p1 92b3e2e3-9074-4b3c-8aab-e6c2ed0e25e3 /          237.5G
├─nvme0n1p2                                                     1K
└─nvme0n1p5 40fa2465-13d1-4b2a-9ea9-370aa00cac15 [SWAP]       976M
```

---

## 2. Creating Mount Points

Create directories where the drives will be mounted:

```bash
sudo mkdir -p /mnt/2TB
sudo mkdir -p /mnt/120GBStorage
sudo mkdir -p /mnt/4tb
```

---

## 3. Mounting the Drives

Test mounting the drives to ensure they work correctly:

```bash
sudo mount /dev/sda1 /mnt/2TB
sudo mount /dev/sdb1 /mnt/120GBStorage
sudo mount /dev/sdc1 /mnt/4tb
```

Verify the mounts by running:

```bash
df -h
```
---

## 4. Configuring `fstab` for Permanent Mount

To automatically mount the drives on boot, edit the `fstab` file:

```bash
sudo nano /etc/fstab
```

Add the following lines at the end of the file:

```plaintext
UUID=1bbd44e6-0dcc-4753-9cf6-99344978eee9 /mnt/2TB          ext4    defaults  0  2
UUID=065cfc69-dfe6-4099-bcc2-615d135b72e8 /mnt/120GBStorage ext4    defaults  0  2
UUID=c99bb4c1-63ae-4773-9e1a-2f976a3bdf52 /mnt/4TB          ext4    defaults  0  2
```

- **`UUID`**: The UUID of the drive (find it using `lsblk -f` or `blkid`).
- **`/mnt/<mount-point>`**: The directory where the drive will be mounted.
- **`ext4`**: The file system type.
- **`defaults`**: Default mount options (adjust if needed).
- **`0 2`**: Dump and fsck options.

### Example Entry

```plaintext
UUID=1234-ABCD /mnt/data ext4 defaults 0 2
```

Save the file and exit (Ctrl+O, Enter, Ctrl+X).

---

## 5. Testing the `fstab` Configuration

To test the configuration without rebooting:

```bash
sudo mount -a
```

Check if the drives are mounted:

```bash
df -h
```

If there are errors, verify the syntax and details in `/etc/fstab`.

---

## 6. Final Steps

Before putting the device back into a production environment or a network rack, reboot the system to confirm the mounts persist:

```bash
sudo reboot
```

---

## 7. Additional Notes

- **Backup `fstab`**: Always back up the `fstab` file before making changes:

  ```bash
  sudo cp /etc/fstab /etc/fstab.bak
  ```

- **Unmounting**: To unmount a drive:

  ```bash
  sudo umount /mnt/<mount-point>
  ```

- **Permissions**: Adjust ownership and permissions of the mount point as needed:

  ```bash
  sudo chown <user>:<group> /mnt/<mount-point>
  ```

  ```bash
  sudo chmod 755 /mnt/<mount-point>
  ```

---

This document is intended to simplify drive mounting and `fstab` configuration for Linux users. If you encounter any issues, consult the Linux `man` pages or community forums.
