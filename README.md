# Meridian firmware releases

Firmware releases for the Meridian ballistic computer. The source lives elsewhere; this repository only publishes releases.

Each release is tagged `v<version>` and has two assets:

- `manifest.json`: the version, protocol, and the image's size and SHA-256.
- `meridian-<version>.bin`: the firmware image.

The Meridian phone app reads the newest release (`releases/latest/download/manifest.json`), checks the image against the manifest, and sends it to the device over Bluetooth. The device asks for confirmation on its own screen before it accepts anything. A PC can do the same with `ble_client.py ota --release`.

Until secure boot is enabled on the devices, treat every release here as installable on any development device.
