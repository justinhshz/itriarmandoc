# 📱 AR Holeplate Manual Installation and Usage Instructions

[![Unity Version](https://img.shields.io/badge/Unity-2022.3.42f1-blue?logo=unity)](https://unity.com/releases/editor/whats-new/2022.3.42)
[![Android](https://img.shields.io/badge/Android-Supported-success?logo=android&logoColor=white)](https://developer.android.com)
[![iOS](https://img.shields.io/badge/iOS-Supported-success?logo=apple)](https://developer.apple.com)

Welcome to the **AR Holeplate Manual**, an augmented reality (AR) instructional application specifically developed for the **Industrial Technology Research Institute (ITRI)**. This document provides comprehensive installation steps and user guidance to help you deploy and interact with the application effectively across Android and iOS platforms.

## 📄 Table of Contents

* 🧭 [Project Overview](#-project-overview)
* 📚 [Developer Notes](#-developer-notes)
* 📋 [System Requirements](#-system-requirements)
* 🔧 [Installation Guide](#-installation-guide)
    * 🤖 [Android – Manual Installation via APK](#-android--manual-installation-via-apk-not-via-google-play)
    * 🍏 [iOS – Manual Installation via Xcode](#-ios--manual-installation-via-xcode-not-via-app-store)
* 🔍 [User Guide](#-user-guide)
    * [1. Launching the App and Selecting a Mode](#1-launching-the-app-and-selecting-a-mode)
    * [2. Placing the Holeplate Model in AR](#2-placing-the-holeplate-model-in-ar)
    * [3. Interacting with the Holeplate (Both Modes)](#3-interacting-with-the-holeplate-both-modes)
    * [4. Navigating back to the Home and Accessing the Option Menu](#4-navigating-back-to-the-home-and-accessing-the-option-menu)
* 💬 [Feedback & Support](#-feedback--support)

---

## 🧭 Project Overview

The **AR Holeplate Manual** is an educational tool that leverages AR technology to provide an intuitive, step-by-step guide for demonstrating the use and structure of Holeplates. Designed primarily for internal training and external demonstrations, the app overlays interactive 3D animations onto the real world through the user's device camera.

### 🎯 Key Features

* Interactive AR-based 1:1 real-world-scale visualization of Holeplate components
* Step selection for direct navigation within tutorial sequences
* Step-by-step animated instruction with speed control
* Real-time toggle of hole labels and object deletion
* Support for both Android and iOS platforms

This application is built using Unity and AR Foundation to ensure a consistent and responsive cross-platform experience.

---

## 📚 Developer Notes

This project is developed based on the official **Unity AR Mobile Template**, which provides a robust starting point for mobile AR projects.

The AR Mobile Template includes pre-configured components for camera access, AR session management, permission handling, touch input, plane detection, and UI overlays. It is particularly useful if you're exploring how Unity structures a minimal but functional AR setup.

If you encounter any of the following challenges, this quick-start guide may be especially helpful:

* Not knowing what each component in the [example scene](https://docs.unity3d.com/Packages/com.unity.template.ar-mobile@1.0/manual/index.html#sample-scene-hierarchy-overview) is for (e.g., AR Session Origin, AR Camera)
* Not knowing how to use the [simulated XR environment](https://docs.unity3d.com/Packages/com.unity.template.ar-mobile@1.0/manual/index.html#xr-simulation) in the Unity Editor to preview AR interactions without deploying to a physical device

Refer to the [official Unity AR Mobile Template documentation](https://docs.unity3d.com/Packages/com.unity.template.ar-mobile@1.0/manual/index.html) for clarification and implementation guidance.

---

## 📋 System Requirements

* **Android**: Android 11.0 or later
* **iOS**: iOS 12.0 or later

---

## 🔧 Installation Guide

### 🤖 Android – Manual Installation via APK (not via Google Play)

1. Visit the [GitHub Releases page](https://github.com/justinhshz/itriarmanual/releases) using a browser on your computer or Android device, and download the latest APK file (`arhpmanual-android.apk`).
2. If you downloaded the APK on your computer, transfer it to your Android device using a USB cable (e.g., into the Downloads folder).
3. On your Android device, open **Settings > Apps > Special app access > Install unknown apps** (this is the default path on stock Android, such as Pixel devices running Android 13 or newer. On some devices, the path may be slightly different, such as under **Security & Privacy**).
4. Locate and tap the app (e.g., Chrome or your file manager), and enable **Allow from this source**.
5. Use your file manager to open the downloaded APK file and confirm installation when prompted.
6. If a warning appears about unknown apps, confirm and proceed. On newer Android versions (e.g., Android 13+), you may need to grant additional permission to install unknown apps during this process.
7. Once installation is complete, open the app from your application drawer.

> [!CAUTION]
> Because Android system settings may change across versions or device brands, some menu names or paths may look slightly different. If you have difficulty locating the correct setting, refer to your device manufacturer’s support site for help with enabling installation from unknown sources.

### 🍏 iOS – Manual Installation via Xcode (not via App Store)

#### 1. Pre-requisites

1. Ensure the latest version of Xcode is installed on your Mac from the Mac App Store.
2. Connect your iPhone to the Mac via a USB cable and ensure the device is unlocked.
3. Visit the [GitHub Releases page](https://github.com/justinhshz/itriarmanual/releases) and download the Xcode project zip file (`arhpmanual-ios-xcodeproj.zip`).
4. Unzip the project to a local folder.

#### 2. Open and Configure the Xcode Project

1. Launch Xcode and open the project using **File > Open...**, selecting `Unity-iPhone.xcodeproj` from the unzipped folder.
2. In the left panel, open the **Project Navigator** (press `⌘ Command + 1` if it’s hidden).
3. Click the top-level blue project icon (typically named `Unity-iPhone`) to open the project settings view in the main editor panel.
4. Under **TARGETS**, select the `Unity-iPhone` target.
5. Navigate to the **Signing & Capabilities** tab and configure the following:
    * **Automatically Manage Signing**\
        Enable the **Automatically manage signing** checkbox to have Xcode handle provisioning and code signing.
    * **Team**
        * If you already have an Apple ID configured:
            1. Select your Apple ID from the list.
            2. Choose the appropriate team if you belong to one.
            3. Xcode will automatically manage provisioning profiles and code signing.
        * If you don't have an Apple ID configured:
            1. Click **Add an Account...**
            2. In the dialog that appears, choose the **Apple ID** tab.
            3. Click the **+** button and enter your Apple ID credentials.
            4. Select your Apple ID and click **Choose**.
            5. Xcode will enable free provisioning for basic deployment (7-day expiration) or full provisioning if you're enrolled in the Apple Developer Program.
    * **Bundle Identifier**\
        Set a unique bundle identifier (e.g., `com.itri.arhpmanual`).
6. In the top toolbar, ensure your iPhone is selected as the run destination (do not leave it as the default "Any iOS Device").

#### 3. Build and Run the App

1. Click the **⏵ Run** button in the top left of Xcode, or press `⌘ Command + R` as a shortcut.
2. Xcode will compile the project, install the app on your device, and launch it.
3. The first time you install an app manually, your iPhone may block it as "untrusted":
    1. Go to **Settings > General > VPN & Device Management**.
    2. Under **Developer App**, tap the associated Apple ID and tap **Trust**.
4. Return to the Home Screen and tap the app icon to open it.
5. Tap **Allow** when the "AR Holeplate Manual Would Like to Access the Camera" alert appears on first launch to enable camera access required for AR functionality.

![Xcode Signing Configuration](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dev/xcode_signing_configuration.png)

> [!TIP]
> Sign up for a free Apple ID at [appleid.apple.com](https://appleid.apple.com) and enroll in the Developer Program at [developer.apple.com/programs](https://developer.apple.com/programs) to access additional features.

> [!IMPORTANT]
> Apps installed with a free developer account will expire after 7 days. For full access and distribution options, use a paid Apple Developer account.

---

## 🔍 User Guide

This section describes how to interact with the AR Holeplate Manual application step-by-step, depending on the selected mode.

### 1. Launching the App and Selecting a Mode

When the application starts, a prompt will appear asking you to select one of two modes:

* **Display Mode** – for basic viewing and interaction
* **Tutorial Mode** – for step-by-step guided animation playback

Tap your desired mode to proceed.

![Mode Selection Flow - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/mode_selection_flow.png#gh-light-mode-only)
![Mode Selection Flow - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/mode_selection_flow.png#gh-dark-mode-only)

### 2. Placing the Holeplate Model in AR

When you reach this step, a sequence of on-screen hints will guide you:

* **Scan Surfaces** – move your device around to detect a horizontal plane.
* **Tap to Place** – tap the screen to position the Holeplate model in AR.

> [!NOTE]
> Virtual Holeplate is rendered at a 1:1 scale, matching real-world dimensions exactly.

Once placed, use the following gestures to interact with the model:

1. **Move Object** – drag with one finger to reposition the model.
2. **Scale Object** – pinch with two fingers to resize the model.
3. **Rotate Object** – twist with two fingers to rotate the model.

![Gesture Hints - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/gesture_hints.png#gh-light-mode-only)
![Gesture Hints - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/gesture_hints.png#gh-dark-mode-only)

### 3. Interacting with the Holeplate (Both Modes)

Once a model is placed and selected (tap to select; tap elsewhere to deselect), it will be highlighted with a different color to indicate selection:

* **Selected color**: ![#7a7afa](https://placehold.co/15x15/7a7afa/7a7afa.png) `#7a7afa` (light purple)
* **Unselected color**: ![#89929a](https://placehold.co/15x15/89929a/89929a.png) `#89929a` (cool gray)

![Selected vs Unselected Colors - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/selected_vs_unselected_colors.png#gh-light-mode-only)
![Selected vs Unselected Colors - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/selected_vs_unselected_colors.png#gh-dark-mode-only)

In addition to this visual change, a bottom navigation panel will appear with the following controls:

* ⏯️ **Play/Pause Animation** – Start or pause the animation of the Holeplate assembly.
* 🏷️ **Toggle Holeplate Number Labels** – Show or hide numeric labels on the model's holes.
* ⏱️ **Adjust Animation Speed** – Open a slider panel (range 1–20) to modify playback speed.
* 🧩 **Step Selection (Tutorial Only)** – Reveal a swipeable list of steps and tap anyone to jump directly to that stage of the tutorial.
* 🗑️ **Delete Holeplate Object** – Remove the currently placed model from the AR scene.

These controls appear only after selecting a model.

Additionally, in **Tutorial Mode**, the name of the current step will be displayed above the bottom navigation panel, helping you keep track of your progress.

![Display vs Tutorial Modes - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/display_vs_tutorial_modes.png#gh-light-mode-only)
![Display vs Tutorial Modes - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/display_vs_tutorial_modes.png#gh-dark-mode-only)

![Controls Preview - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/controls_preview.png#gh-light-mode-only)
![Controls Preview - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/controls_preview.png#gh-dark-mode-only)

### 4. Navigating back to the Home and Accessing the Option Menu

![Home & Option Buttons - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/home_option_buttons.png#gh-light-mode-only)
![Home & Option Buttons - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/home_option_buttons.png#gh-dark-mode-only)

The app provides two persistent buttons for navigation and accessing additional tools:

* 🏠 **Home button** (top-left corner) – Return to the mode selection screen at any time.
* ⚙️ **Option button** (top-right corner) – Open a modal window containing the following tools:
    * 💡 **Show Interaction Hints** – Display brief guidance overlays to assist with model interaction.
    * 📡 **Visualize Surfaces** – Toggle visualization of detected AR planes to aid in model placement.
    * 🧹 **Remove All Objects** – Clear all Holeplate objects currently placed in the scene.
    * 🧪 **AR Debug Menu** – Access technical AR session information for advanced diagnostics.

These features are available in both Display and Tutorial modes.

![Visualize Surfaces Toggle - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/visualize_surfaces_toggle.png#gh-light-mode-only)
![Visualize Surfaces Toggle - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/visualize_surfaces_toggle.png#gh-dark-mode-only)

> [!TIP]
> If no controls appear after placement, ensure the model is selected by tapping on it once in the AR scene.

---

## 💬 Feedback & Support

🙏 Thank you for using **AR Holeplate Manual**. We welcome your feedback to continue improving the app experience. For support or inquiries, please contact the project maintainers or submit an issue via the repository.
