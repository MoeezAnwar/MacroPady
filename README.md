# MacroPady Macroboard Project

This project is a custom-built **Macroboard** named **MacroPady**, designed to provide extra functionality for various applications. It features rotary encoders, Cherry MX switches, WS2812B NeoPixels, and is programmed using **QMK Firmware** for fully customizable keymaps, macros, and lighting effects.

---

## Features
- **Rotary Encoders** with built-in switches
- **Cherry MX Key Switches** for tactile feedback
- **WS2812B NeoPixels** for customizable RGB lighting
- **Adafruit KB2040** microcontroller for easy programming with QMK Firmware
- **QMK Firmware** support for extensive customization and control

## Bill of Materials (BOM)

| **Qty** | **Value** | **Device**                            | **Parts**                                      | **Description**                              |
|:-------:|:---------:|:-------------------------------------:|:---------------------------------------------:|:--------------------------------------------:|
|   2     |           | ELECTROMECH_ENCODER_PLUS_SWITCH_BOURNS_PEC11 | SW1, SW2                                     | Rotary Encoder with Built-In Switch          |
|  12     |           | DIODESOD-123                         | D1, D2, D3, D4, D5, D6, D7, D8, D9, D10, D11, D12 | Diodes                                       |
|   4     |  0.1µF    | 0.1UF-0603-25V-(+80/-20%)            | C1, C2, C3, C4                               | 0.1µF Ceramic Capacitors                     |
|   1     |   10K     | R-US_R0805                           | R1                                            | Resistor, American Symbol                    |
|   1     |           | 74HCT1G125DBV                        | IC1                                           | Single Bus Buffer Gate with 3-State Output   |
|  12     |           | CHERRY_MX                            | S1, S2, S3, S4, S5, S6, S7, S8, S9, S10, S11, S12 | Cherry MX Keymodule                          |
|   1     |           | KB2040                               | U1                                            | Adafruit KB2040 Microcontroller              |
|   4     |           | WS2812B5050                          | LED1, LED2, LED3, LED4                        | WS2812B NeoPixels                            |


## Folder Structure

- **PCB Folder**: Contains the PCB design files, including Gerber files, PCB schematics (`.sch`), and board layout files (`.brd`).
- **CAD Folder**: Contains the 3D model files, including the **MacroPady** `.step` file for use in CAD software.
- **qmk_firmware Folder**: Contains the QMK firmware keymap and configuration for MacroPady.

---

## Programming the MacroPady

The **MacroPady** uses [QMK Firmware](https://qmk.fm/) for programming. To get started:

1. Clone the QMK Firmware repository:
    ```bash
    git clone https://github.com/qmk/qmk_firmware.git
    ```
2. Navigate to the QMK firmware folder:
    ```bash
    cd qmk_firmware
    ```
3. Place the MacroPady keymap files in the `keymaps` folder under your QMK directory.
4. Build and flash the firmware:
    ```bash
    qmk compile -kb kb2040 -km MacroPady
    qmk flash -kb kb2040 -km MacroPady
    ```

---

## How to Build

1. **Gather Components**: Refer to the Bill of Materials (BOM) above to collect all necessary components.
2. **Assemble the PCB**: Solder the components onto the PCB using the provided schematic and layout files.
3. **Program the KB2040**: Use QMK Firmware to program the Adafruit KB2040 microcontroller.
4. **Customize Keymaps & Macros**: Modify keymaps and macros using QMK as per your preference.

---

## License

This project is licensed under the [MIT License](LICENSE).




git config --global user.name "Moeez Anwar"
   git config --global user.email "moeez@flurryhost.com"