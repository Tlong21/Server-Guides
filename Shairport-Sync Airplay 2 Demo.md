### Debian / Raspberry Pi OS / Ubuntu
```
apt update
apt upgrade
apt install --no-install-recommends build-essential git autoconf automake libtool \
    libpopt-dev libconfig-dev libasound2-dev avahi-daemon libavahi-client-dev libssl-dev libsoxr-dev \
    libplist-dev libsodium-dev libavutil-dev libavcodec-dev libavformat-dev uuid-dev libgcrypt-dev xxd
```
### NQPTP
```
git clone https://github.com/mikebrady/shairport-sync.git
cd shairport-sync
autoreconf -fi
./configure --sysconfdir=/etc --with-alsa \
    --with-soxr --with-avahi --with-ssl=openssl --with-systemd --with-airplay-2
make
make install
```
## 4. Test
At this point, Shairport Sync should be built and installed but not running. If the user you are logged in as is a member of the unix `audio` group, Shairport Sync should run from the command line:
```
shairport-sync
```
* Add the `-v` command line option to get some diagnostics. 
* Add the `--statistics` option to get some infomation about the audio received.

Note: Shairport Sync will run indefinitely -- use Control-C it to stop it.

## 5. Enable and Start Service
Once you are happy that Shairport Sync runs from the command line, you should enable and start the `shairport-sync` service. This will launch Shairport Sync automatically as a background "daemon" service when the system powers up:

### Linux
```
# systemctl enable shairport-sync
```
## 6. Check
Reboot the machine. The AirPlay service should once again be visible on the network and audio will be sent to the default ALSA device.

## 7. Final Notes
A number of system settings can affect Shairport Sync. Please review them as follows:

### Power Saving
If your computer has an `Automatic Suspend` Power Saving Option, you should experiment with disabling it, because your computer has to be available for AirPlay service at all times.
### WiFi Power Management – Linux
If you are using WiFi, you should turn off WiFi Power Management:
```
# iwconfig wlan0 power off
```
or
```
# iw dev wlan0 set power_save off
```

Path to ROOT/ETC/shairport-sync.conf and delete the // and Add the name of the device.