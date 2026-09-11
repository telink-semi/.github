# Welcome to Telink's GitHub!

Telink provides a rich product portfolio, along with software development kits (SDKs), components, libraries, solutions, and tools, to help you accelerate product development.

All of Telink's official software related to the different series of Telink SoC can be found on this GitHub site. To explore all the series of SoCs, please visit the [Telink Product Selection Tool](https://products.telink-semi.cn/#/).

For official documentation, please visit this [link](https://doc.telink-semi.cn/doc/en/). If you have any questions during development, feel free to post them on the [Telink Forum](https://forum.telink-semi.cn/), where our technical support team will help you.

To learn more about Telink's full range of products and services, please visit the [Telink official website](https://www.telink-semi.com/).


## Locate the Right SDK

Telink SDKs support the development of low-power wireless applications on Telink SoCs, with development environments on Windows / Linux / MacOS. Each SDK targets different application scenarios.

Locating the right SDK takes two steps:

1. Determine the SDK type: choose the corresponding SDK family from the table below based on your application scenario.
2. Determine the repository prefix by chip series:
   - TC series (Telink self-developed TC32 core) → `tc_` prefix
   - TL series (RISC-V core) → `tl_` prefix

(Some repositories keep their historical naming, such as `telink_zigbee_sdk`; the supported chips include the TC series and TL series.)

| SDK Type | SDK Repository | Description |
| --- | --- | --- |
| Platform SDK | TL series: [tl\_platform\_sdk](https://github.com/telink-semi/tl_platform_sdk) <br> TC series: [tc\_platform\_sdk](https://github.com/telink-semi/tc_platform_sdk) | Provides fundamental APIs for chip peripherals (PWM / ADC / I2C / SPI / USB / GPIO / PM, etc.), RF, and power management. It is the dependency foundation of all upper-layer protocol stack SDKs. <br> Choose the corresponding standard SDK for the applications based on standard protocols such as Bluetooth (including Mesh), Zigbee, Wi-Fi, and Matter (single-mode or multi-mode); <br> choose the Platform SDK if you want to build everything from the drivers level. |
| Bluetooth LE SDK | TL series: [tl\_ble\_sdk](https://github.com/telink-semi/tl_ble_sdk), [tl\_ble\_mesh](https://github.com/telink-semi/tl_ble_mesh) <br> TC series: [tc\_ble\_sdk](https://github.com/telink-semi/tc_ble_sdk), [tc\_ble\_single\_sdk](https://github.com/telink-semi/tc_ble_single_sdk), [tc\_ble\_simple\_sdk](https://github.com/telink-semi/tc_ble_simple_sdk), [tc\_ble\_mesh](https://github.com/telink-semi/tc_ble_mesh) | Provides Bluetooth LE multi-connection / single-connection protocol stacks + 2.4G proprietary protocols. Supports Bluetooth LE (controller / host / profiles), with reference applications such as the HCI transparent transmission module, remote controls, and HID dongles, and integrates the functions, such as PM, OTA, Flash management, battery voltage detection and so on. <br> **BLE multi-connection**: tl\_ble\_sdk (TL), tc\_ble\_sdk (TC), both with 2.4G proprietary protocol. <br> **BLE single-connection** (TC series only): tc\_ble\_single\_sdk (limited on-chip resources), tc\_ble\_simple\_sdk (extremely limited on-chip resources, e.g., OTP only with no Flash). <br> **Bluetooth Mesh**: supports the latest Bluetooth Mesh standard, remote provisioning, Mesh OTA, directed forwarding, certificate-based provisioning, private beacons, subnet bridging, Opcode aggregation, NLC profiles, etc. |
| Zigbee / 802.15.4 / RF4CE | [telink\_zigbee\_sdk](https://github.com/telink-semi/telink_zigbee_sdk), [telink\_802154\_sdk](https://github.com/telink-semi/telink_802154_sdk), [telink\_rf4ce\_sdk](https://github.com/telink-semi/telink_rf4ce_sdk) | Zigbee, RF4CE, or 802.15.4 MAC SDKs; the Zigbee SDK supports concurrent Zigbee / Bluetooth LE dual-mode connections. |
| Matter | [tl\_matter](https://github.com/telink-semi/tl_matter) | Supports Matter over Thread and Matter over Wi-Fi. |
| Audio SDK | [tl\_bluetooth\_audio\_sdk](https://github.com/telink-semi/tl_bluetooth_audio_sdk) | A multi-mode audio SDK combining Bluetooth Classic audio + LE Audio + 2.4G low-latency audio (TPSLL). Supports single-mode (BT Classic / LE Audio), multi-mode (BT + LE Audio / BT + TPSLL), and dual-pair / concurrent modes, with reference designs such as Headset / TWS, LE Audio Unicast / Auracast, and recording cards. |
| Zephyr | [tl\_zephyr](https://github.com/telink-semi/tl_zephyr) | A multi-protocol development platform based on Zephyr RTOS, for IoT applications such as Matter / Bluetooth. |

**Note**:
> - For the specific chip series supported by each SDK, please refer to each repository's README and the latest Release Notes (Chip Version field). The [Product Selection Tool](https://products.telink-semi.cn/#/) can also help with chip selection.

