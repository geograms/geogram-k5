# Geogram UV-K5 Firmware

This firmware brings **Geogram support** to the **Quansheng UV-K5 / UV-K5(8)** radio series, building on the open-source efforts of the UV-K5 firmware community. It transforms the radio into a hybrid digital/analog node capable of interacting with APRS data, NOSTR-based messaging, and Geogram BLE beacons (via Android integration).

**▶️ Watch the demo:**  
[![Watch the demo on YouTube](https://img.youtube.com/vi/1AmZH70CvOg/maxresdefault.jpg)](https://youtu.be/1AmZH70CvOg)



---

## 📡 Features

- 🛰️ **Geogram Packet Transmission**  
  Sends beacon packets over FM voice frequencies using Geogram’s audio-based protocol.

- 📻 **APRS & Digital Beacon Support**  
  Compatible with analog APRS gateways and Geogram mobile app.

- 🔦 **BLE-aware Voice Logging Mode**  
  Responds to Geogram BLE presence packets (when used alongside an ESP32 or T-Dongle node).

- 🌐 **Open Source + Fully Offline Capable**  
  All processing and interactions are done on the radio—no internet required.

---

## 🧱 Hardware Requirements

- **Quansheng UV-K5** or **UV-K5(8)**
- USB-to-Serial flashing cable (or built-in USB in newer models)

---

## 🔧 Build & Flash Instructions

This firmware must be compiled and flashed manually. Use PlatformIO or Docker to build.

### PlatformIO Build

```bash
git clone https://github.com/geograms/uvk5-firmware.git
cd uvk5-firmware
pio run
```

Flash using your preferred serial tool (e.g. `uvtools` or `esptool.py`).

### Docker Build (recommended for size optimization)

```bash
./compile-with-docker.sh
```

Output will be saved in `compiled-firmware/firmware.packed.bin`

> Note: follow the flashing instructions from [UV-K5 Wiki](https://github.com/ludwich66/Quansheng_UV-K5_Wiki/wiki)

---

## 📄 License

Licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)

---

## 📣 Support

- Discussions: https://github.com/orgs/geograms/discussions  
- Issues: https://github.com/geograms/geogram-html/issues

---

## 🤝 Contributors

See [`CONTRIBUTORS.md`](https://github.com/geograms/geogram-html/blob/main/CONTRIBUTORS.md)

**Primary Contributor**  
👤 Max Brito (Portugal/Germany) — 2025–present  
- Geogram audio protocol integration  
- Feature selection for field resilience  
- UX changes and power-aware mods
