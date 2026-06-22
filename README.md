# ESP功率计
### 编译说明
- 系统环境：Ubuntu 22.04
- 安装esp-idf：https://docs.espressif.com/projects/esp-idf/zh_CN/release-v5.1/esp32c3/get-started/linux-macos-setup.html
- 选择配置
    - XT60：`cp sdkconfig.esp32c3 sdkconfig`
    - XT30：`cp sdkconfig.esp32c2 sdkconfig`
- 执行`idf.py build`编译
- 执行`idf.py flash`烧录
### 功能说明
- 实时显示电压、电流、功率
- 显示电流/功率历史曲线
- 累计电量统计，单位 mWh
- 过流、欠压报警
- 低压保护 / 过流保护
- 蜂鸣器提示功能
- 电压、电流、零点校准
- 保存设置和校准数据到 NVS
- 支持 OLED 或 1.47 寸 LCD 显示（可选）
- 支持 INA226 / INA238 电流传感器
- 支持 ESP32C3 内置温度传感器读取芯片温度
- 可选 ESC 模式支持

### 硬件说明
- 使用 ESP32C3 主控
- 使用 INA226 或 INA238 采样芯片
- DCDC + LDO 供电，带反接保护
- XT60 接口
- 1.29寸 OLED 或 1.47寸 LCD 屏幕
- 输入电压：5~30V（80V 模式可选）
- 电流范围：1mA~60A
### 硬件开源地址
- https://oshwhub.com/qwiaoei/xt60-powermeter
