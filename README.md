<div align="center">

# 🌟 Thoth: ZMK Firmware Configuration for Corne Keyboard

Thoth is a custom ZMK firmware configuration for the Corne keyboard, designed to work with the nice!nano v2 controller and nice!view display. It offers a powerful and flexible typing experience with advanced features and customizations.

<br>

<a href="#-features"><kbd> <br> Features <br> </kbd></a>&ensp;&ensp;
<a href="#-hardware"><kbd> <br> Hardware <br> </kbd></a>&ensp;&ensp;
<a href="#-keymap"><kbd> <br> Keymap <br> </kbd></a>&ensp;&ensp;
<a href="#-building-and-flashing"><kbd> <br> Building & Flashing <br> </kbd></a>&ensp;&ensp;
<a href="#-customization"><kbd> <br> Customization <br> </kbd></a>&ensp;&ensp;
</div>
<br><br>

## 🚀 Features

- 🔢 Custom keymap with 4 layers: Base, Lower, Raise, and Adjust
- 📡 Bluetooth connectivity with support for 5 devices
- 🖥️ Nice!view display support
- 🔋 Power management features including deep sleep
- 🖱️ Mouse emulation support
- 🎵 Media controls

## 🛠️ Hardware

- Board: nice!nano v2
- Shield: Corne (split 3x5_3 layout)
- Display: nice!view

## ⌨️ Keymap

The keyboard uses a 4-layer keymap:

1. 🏠 Base Layer: Standard QWERTY layout with some modifications
2. 🔽 Lower Layer: Numbers, symbols, and some navigation keys
3. 🔼 Raise Layer: Function keys and additional navigation
4. ⚙️ Adjust Layer: Bluetooth controls, media keys, and mouse emulation

![Keymap](/imgs/keymap.svg)

## 🔧 Building and Flashing

This repository is set up with GitHub Actions for automatic firmware building. When changes are pushed, GitHub Actions will build the firmware for both halves of the keyboard.

To flash the firmware to your nice!nano v2:

1. Plug your nice!nano into your computer.
2. Enter the bootloader by double-tapping the reset button. 
   > (Skip this step if you haven't flashed the nice!nano before)
3. Drag and drop the `.uf2` file onto the `NICENANO` drive, or copy it using your terminal.
4. After flashing is complete, the drive will disappear and the nice!nano will reboot.
    > Your computer may report an error when transferring the file, you can likely ignore this.
5. If you haven't already, turn on the power switch by pushing it up on the side of the keyboard.

> [!NOTE]
> The .uf2 files for both halves of the keyboard are automatically generated by GitHub Actions when changes are pushed to this repository.

## 📁 Configuration

The main configuration files are:

- `config/corne.keymap`: Defines the keyboard layers and key mappings
- `config/corne.conf`: Contains various ZMK configuration options

## 🎨 Customization

To customize the firmware:

1. Modify the `config/corne.keymap` file to change key mappings
2. Adjust settings in `config/corne.conf` for behavior changes
3. Update `build.yaml` if you need to change the build configuration

## 🤝 Contributing

Contributions to improve the configuration are welcome. Please submit a pull request with your proposed changes.

## 📄 License

This configuration is released under the MIT License. See the LICENSE file for more details.

## 👏 Acknowledgements

- [ZMK Firmware project](https://zmk.dev/)
- Corne Keyboard design by [foostan](https://github.com/foostan/crkbd)
- nice!nano and nice!view by [nicell](https://nicekeyboards.com/)