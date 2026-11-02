# TonoCard architecture and call takeover

[简体中文](architecture.zh-CN.md) · [Product overview](../README.md)

TonoCard AI Phone Secretary Card is a Bluetooth phone accessory used with a companion app and cloud AI to handle calls on the owner's existing phone. It does not require carrier call forwarding.

## High-level architecture

| Part | Role |
|---|---|
| Existing phone | Receives and places the phone call using its existing number |
| TonoCard hardware | Connects to the phone like a Bluetooth headset; the product uses HFP + BLE |
| Companion app | Supports device setup, call rules, call review, and the connection to cloud AI |
| Cloud AI | Understands and responds to the conversation according to the owner's instructions |
| Phone owner | Sets the rules, reviews important information, and takes over when needed |

The high-level path is **phone call ↔ TonoCard ↔ app ↔ cloud AI**. This overview describes the product's components; it is not a Bluetooth protocol specification or a public API contract.

## Incoming call lifecycle

1. A call reaches the owner's phone.
2. With the required connections and settings active, AI answers through the TonoCard system.
3. AI asks about the caller's purpose and applies the owner's call rules.
4. When the owner needs to speak, the owner can take over the same call. Bluetooth disconnects and recording stops.
5. After the call, the owner can review the summary and original audio from the AI-handled portion locally.

The owner's takeover is a change in who handles the existing call. It does not mean the owner must enable the carrier's call-forwarding service. Once the owner has taken over, that call cannot be handed back to AI.

## What must stay connected

The phone needs Bluetooth and internet access, and the companion app must be running. The app can run in the background; follow the app's permission and notification setup. Closing the app or disabling a required connection prevents AI call handling.

## Local records and cloud processing

TonoCard uses cloud AI for processing. The product's data policy states that cloud data is deleted once processing ends; call records are not stored in the cloud. Key points and original audio from the AI-handled portion are saved locally. Recording stops when the owner takes over.

Local record storage does not mean the AI runs entirely offline. See the current privacy policy linked from the app or official website for the applicable terms.

## Compatibility

Supports iOS. Due to the wide range of Android devices and operating system versions, the experience with the standard app may vary on some devices. Availability also depends on device connection, settings, software version, plan, network, and service status.

Official references: [TonoCard product website](https://www.tonocard.com/) · [Companion app and usage conditions](https://apps.apple.com/cn/app/tonocard-ai%E7%94%B5%E8%AF%9D%E7%A7%98%E4%B9%A6%E5%8D%A1/id6766748307).

Documentation updated: 2026-11-02.
