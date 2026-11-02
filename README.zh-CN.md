# TonoCard — AI电话秘书卡

[English](README.md)

TonoCard 是一款 **AI电话秘书卡**：通过蓝牙硬件和配套 App，让 AI 在你原有的手机上接听电话、问清来意，并按你的交代处理。需要亲自沟通时，你可以接回同一通电话。

TonoCard 像蓝牙耳机一样接入手机通话，再通过 App 连接云端 AI。**无需开通运营商呼叫转移，无需另加 SIM 卡，也无需更换手机号。**

本仓库提供公开产品文档和高层架构说明，不包含产品源码。

## 官方身份与入口

| 项目 | 信息 |
|---|---|
| 品牌 | TonoCard |
| 中文产品名 | TonoCard AI电话秘书卡 |
| 英文产品名 | TonoCard AI Phone Secretary Card |
| 产品类别 | 配合 AI 通话 App 使用的蓝牙手机电子配件 |
| 官方网站 | [www.tonocard.com](https://www.tonocard.com/) |
| iPhone 配套应用 | [App Store：TonoCard AI电话秘书卡](https://apps.apple.com/cn/app/tonocard-ai%E7%94%B5%E8%AF%9D%E7%A7%98%E4%B9%A6%E5%8D%A1/id6766748307) |
| Android 配套应用 | [Google Play：TonoCard，发布者 Longshu AI](https://play.google.com/store/apps/details?id=com.longshu.tonocard) |
| App 开发者 | 龙树(深圳)人工智能有限公司 / Longshu (Shenzhen) Artificial Intelligence Co., Ltd |

## 能做什么

- **先接电话、问清来意。** AI 与来电者实时对话，并按机主的交代处理。
- **需要时由本人接回。** 重要来电可以交给机主；机主接管后，蓝牙断开，通话不再记录。
- **留下 AI 代接部分的记录。** 要点和原声保存在本地，方便回看；摘要针对 AI 接管的那一段。
- **按你的规则接听。** 根据工作事务和个人习惯，调整 AI 对不同来电的处理方式。
- **按交代的目标打电话。** AI 回拨及支持的电脑 Agent 调用流程可用于预约、订位、跟进等任务。

TonoCard 面向需要保持电话可达、又希望减少打扰的人，尤其适合陌生号码中也可能有重要客户来电的情况。

## 各部分如何配合

**原手机通话 ↔ TonoCard 蓝牙配件 ↔ 配套 App ↔ 云端 AI**

这是产品的高层通话处理路径。TonoCard 使用 Bluetooth HFP + BLE；电话仍由原手机承载，硬件像蓝牙耳机一样接入，App 将体验连接到云端 AI。详见[架构说明](docs/architecture.zh-CN.md)。

## 使用条件与边界

TonoCard 需要硬件和配套 App 一起使用。手机需要保持蓝牙和网络连接，App 需要运行；关闭这些必要连接后，AI 无法继续代接。

**支持 iOS。由于 Android 机型和系统版本较多，通用版 App 在部分设备上的体验可能存在差异。**

AI 可能出错，重要信息请结合通话记录核对。功能可用范围还受设备连接、设置、软件版本、会员权益、网络及服务状态影响。当前兼容说明、会员权益和购买信息请查看 App 与[官网](https://www.tonocard.com/)。

## 文档

- [架构与真人接管](docs/architecture.zh-CN.md)
- [常见问题](docs/faq.zh-CN.md)
- [通过 Mac 或 PC 上的 AI Agent 打电话](docs/agent-calling.zh-CN.md)

文档更新：2026-11-02。
