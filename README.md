# Departure display (historical prototype)

Retired ESP32/e-paper and Raspberry Pi Bluetooth Low Energy departure-display experiment. Source and dependency lockfiles are preserved as a historical reference. No hardware or deployment validation was performed during the privacy cleanup; the old transit API and toolchain may need updates before reuse.

## Local configuration

For the ESP32 central sketch, copy `central-esp32/config.example.h` to `central-esp32/config.private.h`, then configure your Wi-Fi credentials, authorized transit API key and BLE peripheral address. The private header is ignored by Git. These values are required; there is no working credential embedded in the repository.

For the Raspberry Pi write example, set `DEPARTURE_PERIPHERAL_ADDRESS` in the environment. Restore Node dependencies from `central-rpi/package-lock.json` with the historical compatible Node/toolchain as needed; generated `node_modules` and native build outputs are no longer versioned.

## Privacy cleanup

Historical Wi-Fi credentials, transit API key, BLE hardware address, private author email and local home-directory paths were removed from rewritten history. Editor caches and installed dependency/native build trees were removed from history because they can embed local paths and binaries. Public upstream source, license notices, dependency manifests and lockfiles remain.

Earlier commits contain deliberately unusable placeholders. Use the current private configuration mechanism for any reuse. Exposed credentials must be rotated by their owner before reuse; this cleanup does not revoke them. Existing clones should be replaced with a fresh clone to avoid reintroducing old history.
