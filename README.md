# 小智 AI · 桌面版 (ESP32-S3)

> 星火计划 2025 | 基于 **ESP32-S3（非 C3）** 的开源家用电子设备  
> 简洁 · 低成本 · 装配友好 · 声光设计  
![20250802_215243](https://github.com/user-attachments/assets/c0e91b13-aabe-4d31-a724-84d8aa1a7edc)
![20250725_1128002k](https://github.com/user-attachments/assets/a6270f2f-ec11-45cc-b98c-961e6d63e632)
![20250725_144113_1](https://github.com/user-attachments/assets/264c4ed9-1877-4727-a0f3-05b5afbd8477)

## 📖 项目简介

小智 AI 是一个基于 **ESP32-S3** 的开源硬件与软件一体化项目。  
目标是为学习者、创客、教师与学生提供一款 **低成本、易装配、功能完整** 的电子设备。  

核心设计理念：  
1. **ESP32-S3（非 C3）** 主控  
2. **仅 24 个元器件**（降低成本、减少故障点）  
3. **全部 0805 封装**（焊接友好，适合教学与入门）  
4. **面向装配优化**（接口与壳体完美匹配，易于量产）
---

## 🛠️ 硬件设计

![20250831_171503](https://github.com/user-attachments/assets/41c9e7a3-2cdb-4c3d-b012-0bb0746d572f)
![20250831_170543](https://github.com/user-attachments/assets/dccbe2ff-5764-4479-b76f-66dda8b287b7)
![20250831_170558](https://github.com/user-attachments/assets/d452865d-9692-4a5b-b704-b60d35669f6f)
![20250831_170621](https://github.com/user-attachments/assets/9bdb8f0b-c335-4c8c-8185-31bda5bb8583)

### 1. 核心主控
- 选用 **ESP32-S3**（非 C3），支持 Wi-Fi / BLE / AI 指令集  
- 原生 USB 支持，调试与烧录更方便  
- 兼容开源生态（虾哥面包板项目等）  

---

### 2. 电源与接口
- 使用 **TYPEC-300D-BCP16H105**，焊接牢固、形态紧凑  
- 提供稳定的 5V 供电，并通过电源管理电路分配至各模块  

---

### 3. 音频电路
- 集成 **MAX98357AETE+T** 数字音频功放，I2S 接口直连 ESP32-S3  
- 扬声器接口（HC-1.25-2PWT）布局优化至顶部  
- 支持蜂鸣提示与语音播报  

---

### 4. 显示与交互
- 水平嵌入式按钮，兼容 V7 外壳结构  
- 可扩展 OLED / e-Paper 显示（根据需求选配）  
- 交互简单直观，便于上手  

---

### 5. 其他器件
- **全部 0805 封装**，尺寸适中，焊接无压力  
- 电阻、电容等辅助元件布局紧凑，逻辑清晰  

---

## 🧩 PCB 设计与装配
![20250921_132851](https://github.com/user-attachments/assets/ba09dc26-5dc6-466e-9946-589375cc84da)
![20250921_132905_1](https://github.com/user-attachments/assets/5ddc17e0-b3a0-4b5b-af65-655591386811)

- 元件布局面向 3D 外壳优化，减少交叉走线  
- 推荐焊接顺序：Type-C → 主控 → 功放 → 其他器件  
- 装配时需准备 **M2 螺丝 & 10mm 螺丝柱**  
- 推荐使用 **低温焊锡膏 + 加热台**（150°C 以下）  

---

## 💻 软件与固件

