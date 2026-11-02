# TonoCard — AI Phone Secretary Card

[简体中文](README.zh-CN.md)

TonoCard is an **AI Phone Secretary Card**: a Bluetooth hardware accessory and companion app that let AI answer calls on your existing phone, understand the caller's purpose, and follow your call-handling instructions. You can take over the same call when you need to speak yourself.

TonoCard uses the phone you already have. It connects like a Bluetooth headset and works with the app and cloud AI. **It does not require carrier call forwarding, an additional SIM card, or a new phone number.**

This repository contains public product documentation and a high-level architecture overview. It does not contain the product's source code.

## Official identity and links

| Field | Value |
|---|---|
| Brand | TonoCard |
| English product name | TonoCard AI Phone Secretary Card |
| Chinese product name | TonoCard AI电话秘书卡 |
| Product category | Bluetooth phone accessory with an AI call-handling app |
| Official website | [www.tonocard.com](https://www.tonocard.com/) |
| Companion iPhone app | [TonoCard AI电话秘书卡 on the App Store](https://apps.apple.com/cn/app/tonocard-ai%E7%94%B5%E8%AF%9D%E7%A7%98%E4%B9%A6%E5%8D%A1/id6766748307) |
| App developer | 龙树(深圳)人工智能有限公司 / Longshu (Shenzhen) Artificial Intelligence Co., Ltd |

## What TonoCard does

- **Answers and assesses calls.** AI talks with the caller in real time and follows the owner's instructions for handling the conversation.
- **Lets the owner take over.** Important calls can be brought to the owner. When the owner takes over, Bluetooth disconnects and recording stops.
- **Keeps a record of the AI-handled part.** Key points and original audio are saved locally for review. The call summary covers the portion handled by AI.
- **Uses your call rules.** You can adjust how AI responds to callers according to your work and preferences.
- **Makes calls for a stated goal.** AI callbacks and supported computer-agent workflows can help with tasks such as appointments, reservations, and follow-ups.

TonoCard is designed for people who need to remain reachable while reducing interruptions—for example, when unfamiliar numbers may include important customer calls.

## How the parts work together

**Existing phone call ↔ TonoCard Bluetooth accessory ↔ companion app ↔ cloud AI**

This is the product's high-level call-processing path. TonoCard supports Bluetooth HFP + BLE. The phone remains the calling device; the accessory provides a headset-like connection, and the app connects the experience to cloud AI. See the [architecture overview](docs/architecture.md).

## Requirements and boundaries

TonoCard requires both the hardware and companion app. Keep the phone connected to Bluetooth and the internet, with the app running. AI handling is unavailable if these required connections are off.

**Supports iOS. Due to the wide range of Android devices and operating system versions, the experience with the standard app may vary on some devices.**

AI can make mistakes. Review important information in the call record. Feature availability also depends on device connection, settings, software version, plan, network, and service status. Check the app and [official website](https://www.tonocard.com/) for current compatibility, plans, and purchase information.

## Documentation

- [Architecture and call takeover](docs/architecture.md)
- [Common questions](docs/faq.md)
- [Calling from AI agents on a Mac or PC](docs/agent-calling.md)

Documentation updated: 2026-11-02.
