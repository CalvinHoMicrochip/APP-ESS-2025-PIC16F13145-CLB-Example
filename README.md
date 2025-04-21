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
* 以下是這個範例的 CLB 設計，與 CLC 完成的 SPI to WS2012 不同的是 SPI 的輸出入可以經由 CLBSWIN0 來控制要經由 PPS 的硬體輸出 (PPS_OUT1 & PPS_OUT2)或是到 WS2812 的控制區塊 SPI_to_WS2812 然後輸出到 PPS_OUT7
<img src="https://github.com/CalvinHoMicrochip/APP-ESS-2025-PIC16F13145-CLB-Example/blob/main/CLB_WS2812_32x8_DISCOVER.png" width="640px">

* 執行的結果被簡化如下 :
  * LED1 顯示紅色、LED2 顯示綠色、LED3 顯示藍色
  * 顯示的順序為 : Red -> Green -> Blue -> Green ，然後一直循環
  * 您可以自行很輕易地修改為自己想要的顯示方式和調色
#  Example-2 : CLB 控制 四線式步進馬達
步進馬達的控制雖並非難事，工程師們也可以在市場上找到許多好用的智能型步進馬達控制IC。此範例是為了展現 CLB 如何使用 MCU 中的 Timer 為時間基準，配合 CLB 的 Timer & Look-Up-Table 來產生步進馬達所需的控制信號，用最簡單的方式來印證 CLB 的彈性及方便性。
<img src="" width="640px">
