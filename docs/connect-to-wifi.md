# Connect BeagleBone to WiFi
First, connect the board via usb. Linux must be installed. Connect to the terminal using SSH as follows:

```bash
ssh root@192.168.7.2
```

Then, execute the client for wireless configuration:
```bash
sudo connmanctl
```

Enable WiFi:
```bash
connmanctl> enable wifi
# Enabled wifi
```


```bash
connmanctl> scan wifi
# Scan completed for wifi
```

List available networks
```bash
connmanctl> services
# e.g. *AO TNCAPA97AB9    wifi_506583d4fc5e_544e434150413937414239_managed_psk
```

Connect to the network
```bash
connmanctl> connect wifi_506583d4fc5e_544e434150413937414239_managed_psk
# Passphrase? xxxxxxxxxxx
# connected wifi_506583d4fc5e_544e434150413937414239_managed_psk
```

Back to the terminal.
```bash
connmanctl> quit
```
