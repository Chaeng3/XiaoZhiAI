# 小智 AI · 桌面版 (ESP32-S3)

> 星火计划 2025 | 基于 **ESP32-S3（非 C3）** 的开源家用电子设备  
> 简洁 · 低成本 · 装配友好 · 声光设计
> 从设计到制作合集：https://space.bilibili.com/3494361081842431/lists/5494182?type=season
> 
![20250802_215243](https://github.com/user-attachments/assets/c0e91b13-aabe-4d31-a724-84d8aa1a7edc)
![20250725_1128002k](https://github.com/user-attachments/assets/a6270f2f-ec11-45cc-b98c-961e6d63e632)
![20250725_144113_1](https://github.com/user-attachments/assets/264c4ed9-1877-4727-a0f3-05b5afbd8477)
<img width="1608" height="1191" alt="合集" src="https://github.com/user-attachments/assets/8eceadcd-f24d-4647-a4bf-6d7e63b2989b" />

## 📖 项目简介

小智 AI 是一个基于 **ESP32-S3** 的开源硬件与软件一体化项目。  
目标是为学习者、创客、教师与学生提供一款 **低成本、易装配、功能完整** 的电子设备。  

核心设计理念：  
1. **ESP32-S3（非 C3）** 主控  
2. **仅 24 个元器件**（降低成本、减少故障点）  
3. **全部 0805 封装**（焊接友好，适合教学与入门）  
4. **面向装配优化**（接口与壳体完美匹配，易于量产）
---
<img width="2008" height="1127" alt="项目结构" src="https://github.com/user-attachments/assets/99c34f6b-00b0-4150-8862-5e3408dc4666" />


## 🛠️ 硬件设计

使用硬件技术： 
1. **PCB设计**（嘉立创）
2. **焊接技术**
3. **3D设计**  （Fusion）

**硬件开源地址：https://oshwhub.com/chaeng/chaeng_xiaozhiaiv8**

![20250831_171503](https://github.com/user-attachments/assets/41c9e7a3-2cdb-4c3d-b012-0bb0746d572f)
![20250831_170543](https://github.com/user-attachments/assets/dccbe2ff-5764-4479-b76f-66dda8b287b7)
![20250831_170558](https://github.com/user-attachments/assets/d452865d-9692-4a5b-b704-b60d35669f6f)
![20250831_170621](https://github.com/user-attachments/assets/9bdb8f0b-c335-4c8c-8185-31bda5bb8583)
![20250831_170640](https://github.com/user-attachments/assets/560ab7d6-1c27-4a7e-8be0-832fd1dcde27)
![20250831_170647](https://github.com/user-attachments/assets/603c79ea-d5ac-4109-8055-3782567c28c6)

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

## 💻 软件与固件
- V2：屏蔽OTA功能
- V3：位于GPIO48的RGB灯可根据麦克风检测的音量大小而明暗变化（单色）
- V4：增加基础颜色为紫色和基础亮度为50%，并使用MCP实现语音控制颜色和亮度
- V4.1：允许用户彻底关闭灯光
