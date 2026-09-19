# wifi_qrcode_generator
## Generate a QR code for your WiFi network to let others quickly connect without needing to tell them your long and complicated password.
## Installation
```bash
$ pip install wifi-qrcode-generator
```
## Usage
### CLI interactive mode
```bash
$ wifi-qrcode-generator
```

#!/usr/bin/env python3
import wifi_qrcode_generator

qr_code = wifi_qrcode_generator.generator.wifi_qrcode(
    ssid='ALFRED-MAIN', hidden=False, authentication_type='WPA', password='very very complicated'
)
qr_code.print_ascii()
qr_code.make_image().save('wifi_qr.png')

![QR Code](wifi_qr.png)


## Dependencies
- [Pillow](https://pypi.org/project/Pillow/)
- [qrcode](https://pypi.org/project/qrcode/)
