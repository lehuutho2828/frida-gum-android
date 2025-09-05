# Frida Gum Devkit (Android)

[![Update Frida Gum Devkit](https://github.com/YOUR_USERNAME/frida-gum-android/actions/workflows/update-frida.yml/badge.svg)](https://github.com/YOUR_USERNAME/frida-gum-android/actions/workflows/update-frida.yml)

This repository provides prebuilt **Frida Gum Devkit** packages for **Android** architectures:

- android-arm
- android-arm64
- android-x86
- android-x86_64

The content is automatically downloaded from the official Frida releases and extracted into this repository.

---

## 📂 Repository Structure

frida-gum-android/
├── android-arm/
│   ├── include/   # Header files
│   └── lib/       # Prebuilt libraries
├── android-arm64/
│   ├── include/
│   └── lib/
├── android-x86/
│   ├── include/
│   └── lib/
├── android-x86_64/
│   ├── include/
│   └── lib/

---

## 🚀 Usage

### 1. As Git Submodule
Add this repo as a submodule in your project:

    git submodule add https://github.com/YOUR_USERNAME/frida-gum-android external/frida-gum
    git submodule update --init --recursive

Then include headers in your CMake project:

    include_directories(${CMAKE_SOURCE_DIR}/external/frida-gum/android-arm64/include)
    link_directories(${CMAKE_SOURCE_DIR}/external/frida-gum/android-arm64/lib)

    target_link_libraries(
        main
        frida-gum
    )

### 2. Manual Download
Alternatively, download this repo as ZIP and extract the required architecture:

    wget https://github.com/YOUR_USERNAME/frida-gum-android/archive/refs/heads/main.zip

---

## 🔄 Auto Update
This repo is kept up-to-date automatically using GitHub Actions.  
Each Sunday, the workflow checks for the latest Frida release and updates the devkits if necessary.

---

## 📜 License
This project only redistributes **official Frida binaries**.  
See Frida License for details.
