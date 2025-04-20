# APP-ESS-2025-PIC16F13145-CLB-Example
APP-ESS-2025 PIC16F13145 MCU CLB 的範例，包含電路圖以及範例程式
* APP-ESS-2025 是Microchip Taiwan 為了 2025 Microchip 科技論壇所開發的一款多功能實驗板，旨在於提供簡單並實用的開發工具，讓廣大的 Microchip 之友們可以用最精及實惠的方式，來體驗 Microchip 新型 MCU 的強大功能。
* APP-ESS-2025 EVB 上面預置的兩個 MCU 為 PIC32CM5164JH01048 以及 PIC16F13145
* PIC16F13145 具備許多新款的周邊設計，CLB ( Configurable Logic Block) 就是其中的一個重點
  * CLB 的重要參數如下
    * 32 個基本邏輯元件(Basic Logic Element)的互連結構
      *  Each BLE contains one 4-input Look-Up Table (LUT) and one flip-flop
      *  Schematically programmable using MPLAB Code Configurator
    * Dedicated 3-bit hardware counter
#  Example-1 : CLB 控制 WS2812 RGB LED
Microchip 的 DISCOVER 有 WS2812 的範例程式，可以控制 32*8 的 LED 矩陣
* [Microchip DISCOVER WS2812 範例連結](https://mplab-discover.microchip.com/v2/item/com.microchip.code.examples/com.microchip.ide.project/com.microchip.subcategories.modules-and-peripherals.communication.spi/com.microchip.mcu8.mplabx.project.pic16f13145-spi-ws2812-mplab-mcc/1.2.0?view=about&dsl=CLB)

