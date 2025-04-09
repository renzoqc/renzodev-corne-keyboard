
# 🧠 Corne Keyboard QMK Configuration - `renzodev_keyboard`

🎉 Welcome! This repository contains my **personal QMK configuration** for the [Corne split keyboard](https://github.com/foostan/crkbd). It includes a custom keymap, configuration header, and a modified font file to personalize your typing experience.

🔗 **GitHub Repo**: [renzodev-corne-keyboard](https://github.com/renzoqc/renzodev-corne-keyboard)

---

## 🚀 Getting Started

Follow these steps to set up QMK firmware and use the configurations from this repository.

---

## 1️⃣ Install QMK Firmware

Make sure you have Python and Git installed, then run:

```bash
python3 -m pip install qmk
qmk setup
```

This will clone the QMK firmware into `~/qmk_firmware`.

---

## 2️⃣ Create a New Keymap

Navigate to your QMK firmware directory and run:

```bash
cd ~/qmk_firmware
qmk new-keymap -kb crkbd/rev1 -km renzodev_keyboard
```

This creates a new keymap folder in:

```bash
~/qmk_firmware/keyboards/crkbd/keymaps/renzodev_keyboard
```

---

## 3️⃣ Replace with Custom Configuration Files

Assuming you've cloned [this repository](https://github.com/renzoqc/renzodev-corne-keyboard) into your `Downloads` folder:

```bash
cp ~/Downloads/renzodev-corne-keyboard/keymap.c ~/qmk_firmware/keyboards/crkbd/keymaps/renzodev_keyboard/keymap.c
cp ~/Downloads/renzodev-corne-keyboard/config.h ~/qmk_firmware/keyboards/crkbd/keymaps/renzodev_keyboard/config.h
cp ~/Downloads/renzodev-corne-keyboard/lib/glcdfont.c ~/qmk_firmware/lib/glcdfont.c
```

---

## 4️⃣ Compile the Keymap

Once the files are in place, compile your new keymap with:

```bash
cd ~/qmk_firmware
qmk compile -kb crkbd/rev1 -km renzodev_keyboard
```

✅ This will produce a `.hex` or `.bin` file ready to flash to your Corne keyboard.

---

## 🎨 Layout Diagram

You can modify this image on DESIGN.txt

![Keymap Layout](https://github.com/user-attachments/assets/2c8f43e1-4b9a-4e38-8130-b1bd082a09ac)


---

## 👤 Author

**RenzoDev**  
🛠️ Custom firmware enthusiast

---

## 📚 Resources

- 📘 [QMK Documentation](https://docs.qmk.fm/)
- 🧩 [Corne Keyboard GitHub](https://github.com/foostan/crkbd)
