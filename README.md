# 小智 AI · 桌面版 (ESP32-S3)
> 星火计划 2025 | 基于 **ESP32-S3（非 C3）** 的开源家用电子设备  
> 简洁 · 低成本 · 装配友好 · 声光设计

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE)
![ESP32-S3](https://img.shields.io/badge/ESP32-S3-orange)
![Open Hardware](https://img.shields.io/badge/Open-Source%20Hardware-green)
![0805 SMD](https://img.shields.io/badge/All-0805%20SMD-informational)

- 从设计到制作合集（Bilibili）：https://space.bilibili.com/3494361081842431/lists/5494182?type=season

![20250802_215243](https://github.com/user-attachments/assets/c0e91b13-aabe-4d31-a724-84d8aa1a7edc)
![20250725_1128002k](https://github.com/user-attachments/assets/a6270f2f-ec11-45cc-b98c-961e6d63e632)
![20250725_144113_1](https://github.com/user-attachments/assets/264c4ed9-1877-4727-a0f3-05b5afbd8477)
<img width="1608" height="1191" alt="合集" src="https://github.com/user-attachments/assets/8eceadcd-f24d-4647-a4bf-6d7e63b2989b" />

---

## 📖 项目简介
**小智 AI** 是一款基于 **ESP32-S3（非 C3）** 的开源家用电子设备，面向学习者、创客、教师与学生，目标是提供 **低成本、易装配、功能完整** 的 AI 创意平台。

### 🌟 设计理念
- 🧠 **主控芯片**：ESP32-S3（原生 USB + AI 指令集）
- ⚙️ **结构设计**：仅 **24** 个元器件，全部 **0805** 封装
- 🔌 **装配友好**：接口与外壳匹配，适合教学/量产
- 💡 **教学导向**：支持语音/灯光/音频等课堂项目实践

<img width="2008" height="1127" alt="项目结构" src="https://github.com/user-attachments/assets/99c34f6b-00b0-4150-8862-5e3408dc4666" />

---

## 🛠️ 硬件设计
- PCB 制作：嘉立创
- 焊接技术
- 3D 设计：Fusion

**硬件开源地址**：https://oshwhub.com/chaeng/chaeng_xiaozhiaiv8

![20250831_171503](https://github.com/user-attachments/assets/41c9e7a3-2cdb-4c3d-b012-0bb0746d572f)
![20250831_170543](https://github.com/user-attachments/assets/dccbe2ff-5764-4479-b76f-66dda8b287b7)
![20250831_170558](https://github.com/user-attachments/assets/d452865d-9692-4a5b-b704-b60d35669f6f)
![20250831_170621](https://github.com/user-attachments/assets/9bdb8f0b-c335-4c8c-8185-31bda5bb8583)
![20250831_170640](https://github.com/user-attachments/assets/560ab7d6-1c27-4a7e-8be0-832fd1dcde27)
![20250831_170647](https://github.com/user-attachments/assets/603c79ea-d5ac-4109-8055-3782567c28c6)

### 1️⃣ 核心主控
- **ESP32-S3（非 C3）**，支持 Wi-Fi / BLE / AI 指令集  
- 原生 USB，调试与烧录更方便  
- 完全兼容开源生态（虾哥面包板项目bread-compact-wifi-128x64）

### 2️⃣ 电源与接口
- **Type-C**：TYPEC-300D-BCP16H105，牢固、紧凑  
- 5V 稳定供电，电源管理电路分配至各模块

### 3️⃣ 音频电路
- **MAX98357AETE+T和ICS-43434**的功放麦克风组合
- 扬声器接口 **HC-1.25-2PWT** 顶部连接  

### 4️⃣ 显示与交互
- OLED采用128*64点阵
- 两个水平嵌入式按钮（BOOT+RST）

### 5️⃣ 通用器件
- 大部分器件可直接在立创商城一键下单
- 1.3寸OLED模块_4P购买地址（数量1）：https://item.taobao.com/item.htm?id=720009727823&mi_id=0000lwwGIoQJ-PMLvt2za_NLS8dUZVUfxqcwyf9WN4HTzZY&skuId=5186396874222&spm=tbpc.boughtlist.suborder_itemtitle.1.331e2e8daXgLva
- 2828扬声器购买地址（数量1）：https://item.taobao.com/item.htm?id=923265595732&mi_id=0000oe31REGsTHN4ZFDtmRqpDc1aSUdwOQPN4kJ3I5eMDbg&skuId=5801742476727&spm=tbpc.boughtlist.suborder_itemtitle.1.331e2e8daXgLva
- M2螺丝柱购买地址（数量4）：https://item.taobao.com/item.htm?id=916832099884&mi_id=000031S5TTB2RhL9N-J1vRBbIv8GfbSOQAO8i4VvAXF0MnM&spm=tbpc.boughtlist.suborder_itemtitle.1.331e2e8daXgLva&skuId=5785220608417

---

## 💻 软件与固件

### 🔖 版本历史
| 版本 | 更新内容 | 说明 |
|---|---|---|
| V2 | 屏蔽 OTA 功能 | 提升稳定性 |
| V3 | GPIO48 RGB 灯随麦克风音量变化 | 单色音量反馈 |
| V4 | 增加紫色基色、基础亮度 50%，MCP 语音控制颜色与亮度 | 语音调光/调色 |
| V4.1 | 允许用户彻底关闭灯光 | 更安静的使用场景 |

### 🧩 烧录步骤（快速上手）

📘 **详细教程**  
👉 [飞书文档《固件烧录方法》](https://ccnphfhqs21z.feishu.cn/wiki/Zpz4wXBtdimBrLk25WdcXzxcnNS)

---

## 🎥 装配方法
- [装配篇]([https://space.bilibili.com/3494361081842431/lists/5494182?type=season](https://www.bilibili.com/video/BV15Dp4zCECp/?spm_id_from=333.1387.homepage.video_card.click&vd_source=3ac89604b734514d5955b607a3f43d69))

---

## 👤 作者
**Chaeng**  
开源硬件创作者 ｜ 信息科技教师 ｜ 星火计划 2025  
- 📺 Bilibili：[Chaeng 赛博未来]([https://space.bilibili.com/3494361081842431](https://space.bilibili.com/3494361081842431?spm_id_from=333.1007.0.0) 

- 📌 硬件开源：[Chaeng_xiaozhiAI_V8 @ OSHWHub](https://oshwhub.com/chaeng/chaeng_xiaozhiaiv8)

> “让学生看到创造的乐趣，让创客精神点亮课堂。”

---

## 📝 许可证
本项目基于 **GPL-3.0** 协议开源。  
详见仓库中的 [`LICENSE`](LICENSE) 文件。


