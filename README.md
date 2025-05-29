# MTOS Boot Theme for Plymouth

A modern and clean boot animation theme for Plymouth boot splash.

## Features
- Clean, minimalist design
- Animated logo with fade effect
- Progress bar showing boot progress
- Smooth animations

## Requirements
- Plymouth
- Linux system with Plymouth support
- Root access for installation

## Installation

1. First, create the theme directory:
```bash
sudo mkdir -p /usr/share/plymouth/themes/mtos-boot
```

2. Copy the theme files:
```bash
sudo cp mtos-boot.plymouth /usr/share/plymouth/themes/mtos-boot/
sudo cp mtos-boot.script /usr/share/plymouth/themes/mtos-boot/
sudo cp *.png /usr/share/plymouth/themes/mtos-boot/
```

3. Install the theme:
```bash
sudo plymouth-set-default-theme -R mtos-boot
```

## Customization

You can customize the theme by:
1. Replacing the logo.png with your own logo
2. Modifying the progress_box.png and progress_bar.png with your own design
3. Adjusting colors and animations in the script file

## Note
Make sure to create the following image files:
- logo.png (recommended size: 256x256)
- progress_box.png (recommended size: 400x20)
- progress_bar.png (recommended size: 396x16)

## Troubleshooting

If the theme doesn't appear:
1. Verify Plymouth is installed: `plymouth --version`
2. Check if the theme is listed: `plymouth-set-default-theme --list`
3. Ensure all required files are in the correct location
4. Rebuild the initramfs if needed: `sudo update-initramfs -u` 