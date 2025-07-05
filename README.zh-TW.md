# 📱 AR Holeplate Manual 安裝與使用說明

[![Unity Version](https://img.shields.io/badge/Unity-2022.3.42f1-blue?logo=unity)](https://unity.com/releases/editor/whats-new/2022.3.42)
[![Android](https://img.shields.io/badge/Android-Supported-success?logo=android&logoColor=white)](https://developer.android.com)
[![iOS](https://img.shields.io/badge/iOS-Supported-success?logo=apple)](https://developer.apple.com)
[![Language: English](https://img.shields.io/badge/Language-English-orange?logo=googletranslate&logoColor=white)](README.md)
[![License: Limited Use](https://img.shields.io/badge/License-Limited%20Use-red.svg?logo=github)](LICENSE)

> 🌐 本文件的英文版可以參考[這裡](README.md)。

歡迎使用 **AR Holeplate Manual**，這是一款專為 **工業技術研究院 (ITRI)** 開發的擴增實境 (AR) 教學應用程式。本文件提供了詳細的安裝步驟和使用指南，協助您在 Android 和 iOS 平台上順利部署和操作。

## 📄 目錄

* 🧭 [專案簡介](#-專案簡介)
* 📚 [開發筆記](#-開發筆記)
* 📋 [系統需求](#-系統需求)
* 🔧 [安裝指南](#-安裝指南)
    * 🤖 [Android – APK 手動安裝](#-android--apk-手動安裝不透過-google-play)
    * 🍏 [iOS – Xcode 手動安裝](#-ios--xcode-手動安裝)
* 🔍 [使用說明](#-使用說明)
    * [1. 啟動應用程式與選擇模式](#1-啟動應用程式與選擇模式)
    * [2. 在 AR 中放置 Holeplate 模型](#2-在-ar-中放置-holeplate-模型)
    * [3. 與 Holeplate 模型互動（兩種模式皆適用）](#3-與-holeplate-模型互動兩種模式皆適用)
    * [4. 回到首頁與選單功能](#4-回到首頁與選單功能)
* 💬 [意見回饋](#-意見回饋)

---

## 🧭 專案簡介

**AR Holeplate Manual** 是一款運用 AR 技術，提供直覺式、逐步教學的教育工具，旨在展示 Holeplate 的結構與操作方式。主要適用於內部訓練與外部展示，透過行動裝置的鏡頭將 3D 動畫互動式地疊加於現實環境中。

### 🎯 主要特色

* AR 互動式 1:1 真實比例 Holeplate 模型
* 支援步驟選擇，直接導航至各教學流程
* 動畫逐步教學與播放速度控制
* 實時切換孔號標籤可見度與物件刪除功能
* 直覺式操作介面，適合各年齡層使用
* 同時支援 Android 與 iOS 平台

本應用程式以 Unity 與 AR Foundation 為核心打造，確保跨平台體驗一致且流暢。

## 📚 開發筆記

本專案以官方 **Unity AR Mobile Template** 為基礎，它預設整合了相機存取、AR Session 管理、權限請求、觸控輸入、平面偵測與操作介面等功能，非常適合作為開發 AR 行動裝置應用程式的參考。

如果您在開發過程中遇到以下任何相關問題：

* 不知道 [範例場景](https://docs.unity3d.com/Packages/com.unity.template.ar-mobile@1.0/manual/index.html#sample-scene-hierarchy-overview) 中各元件（如 AR Session Origin、AR Camera）的用途？
* 不知道如何在 Unity Editor 中使用 [XR 模擬環境](https://docs.unity3d.com/Packages/com.unity.template.ar-mobile@1.0/manual/index.html#xr-simulation) 預覽 AR 效果？

請參考 [Unity AR Mobile Template 官方說明文件](https://docs.unity3d.com/Packages/com.unity.template.ar-mobile@1.0/manual/index.html) 以獲得更詳細的實作指引。

---

## 📋 系統需求

* **Android**：Android 11.0 (API level 30) 或更高版本
* **iOS**：iOS 12.0 或更高版本

---

## 🔧 安裝指南

### 🤖 Android – APK 手動安裝（不透過 Google Play）

1. 使用電腦或 Android 裝置的瀏覽器前往 [GitHub Releases 頁面](https://github.com/justinhshz/itriarmandoc/releases)，下載最新的 APK 檔案 (`arhpmanual-android.apk`)。
2. 如果您使用電腦下載，請透過 USB 傳輸將 APK 檔案複製到 Android 裝置（例如放入「下載」資料夾）。
3. 在 Android 裝置上，前往 **設定 > 應用程式 > 特殊應用程式存取權 > 安裝未知應用程式**（這是原生 Android 13 或更新版本的預設路徑，部分廠牌可能在 **安全性與隱私權** 下）。
4. 找到對應的應用程式（例如 Chrome 或您的檔案管理器），並啟用 **允許來自此來源的安裝**。
5. 使用檔案管理器找到剛剛下載的 APK 檔案，點擊並按照指示進行安裝。
6. 如果出現任何安裝警告，請按照畫面中的指示操作即可。新版 Android（如 13 以上）可能會要求您確認額外的安全性設定。
7. 安裝完成後，您可以在應用程式列表中找到本應用程式，點擊啟動。

> [!CAUTION]
> 不同品牌或 Android 版本的系統設定名稱可能略有差異，如果找不到上述設定路徑，請參考您的手機品牌官方支援網站，查詢「安裝未知來源應用程式」的方法。

### 🍏 iOS – Xcode 手動安裝（不透過 App Store）

#### 1. 前置準備

1. 確保您的 Mac 上已安裝最新版本的 Xcode，您可以從 Mac App Store 下載。
2. 將 iPhone 透過 USB 線連接到 Mac，並確保裝置已解鎖。
3. 前往 [GitHub Releases 頁面](https://github.com/justinhshz/itriarmandoc/releases) 下載最新的 Xcode 專案壓縮檔 (`arhpmanual-ios-xcodeproj.zip`)。
4. 將下載的壓縮檔解壓縮到本地資料夾。

#### 2. 開啟並設定 Xcode 專案

1. 開啟 Xcode，點擊 **File > Open...**，選擇解壓縮後的資料夾中的 `Unity-iPhone.xcodeproj`。
2. 在 Xcode 中，打開左側的 **Project Navigator**（如果沒出現可以按鍵盤快速鍵 `⌘ Command + 1`）。
3. 點擊頂部的藍色專案圖示（通常為 `Unity-iPhone`），主面板會切換到專案設定頁。
4. 在 **TARGETS** 下，選擇 `Unity-iPhone`。
5. 切換到 **Signing & Capabilities** 分頁並設定：
    * **Automatically Manage Signing**\
        啟用 **Automatically manage signing**，讓 Xcode 自動處理簽名與憑證。
    * **Team**
        * 如果您已經登入 Apple ID：
            1. 從列表中選擇您的 Apple ID。
            2. 如果您屬於某個團隊，選擇相應的團隊。
            3. Xcode 將自動管理簽名與憑證。
        * 如果您尚未登入 Apple ID：
            1. 點擊 **Add an Account...**。
            2. 在彈出對話框中，選擇 **Apple ID** 分頁。
            3. 點擊 **+** 按鈕，輸入您的 Apple ID 帳號與密碼。
            4. 選擇您的 Apple ID，然後點擊 **Choose**。
            5. Xcode 會自動根據您的帳號類型，啟用免費（有效期限 7 天）或付費（如果您已註冊 Apple 開發者計畫）的完整部署權限。
    * **Bundle Identifier**\
        設定專屬的 Bundle Identifier（例如 `com.itri.arhpmanual`）。
6. 在上方工具列中，選擇您的實體 iPhone 作為目標裝置（請勿選擇預設的 Any iOS Device）。

#### 3. 建置與執行 App

1. 點擊左上角的 **⏵ Run** 按鈕或使用鍵盤快速鍵 `⌘ Command + R`。
2. Xcode 會開始編譯專案並部署到您的 iPhone 上。
3. 如果是第一次部署，iPhone 會以「不受信任的開發者」擋下：
    1. 前往 iPhone 的 **設定 > 一般 > VPN與裝置管理**。
    2. 在 **開發者 App** 下，點擊對應的 Apple ID 並選擇 **信任**。
4. 回到主畫面，點擊 App 圖示啟動應用程式。
5. 首次啟動時，可能會要求您允許相機存取權限，請點擊 **允許** 以啟用 AR 功能。

![Xcode Signing Configuration](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dev/xcode_signing_configuration.png)

> [!TIP]
> 可以到 [appleid.apple.com](https://appleid.apple.com) 申請免費的 Apple ID，或是在 [developer.apple.com/programs](https://developer.apple.com/programs) 中加入開發者計畫以獲得更多功能與資源。

> [!IMPORTANT]
> 如果您使用免費的 Apple ID，請注意每 7 天需要重新部署一次應用程式，否則將無法在 iPhone 上繼續使用。如果需要完整部署與發佈功能，建議使用付費的 Apple Developer 帳號。

---

## 🔍 使用說明

本章節將介紹如何在 AR Holeplate Manual 應用程式中使用各項功能。

### 1. 啟動應用程式與選擇模式

啟動應用程式後，會跳出模式選擇畫面。您可以選擇以下兩種模式：

* **瀏覽模式（Display Mode）**：適合展示 Holeplate 的結構與功能，提供基本的瀏覽與互動。
* **教學模式（Tutorial Mode）**：提供詳細的逐步教學，適合新手培訓與操作。

點擊所需模式後，應用程式將進入相應的操作介面。

![Mode Selection Flow - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/mode_selection_flow.png#gh-light-mode-only)
![Mode Selection Flow - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/mode_selection_flow.png#gh-dark-mode-only)

### 2. 在 AR 中放置 Holeplate 模型

在選擇模式後，會提示您：

* **掃描平面**：緩慢移動裝置以偵測水平平面。
* **點擊放置**：在偵測到的平面上點擊以放置 Holeplate 模型。

> [!NOTE]
> 虛擬 Holeplate 模型預設以 1:1 真實比例顯示，與實體尺寸完全相同。

放好模型後，您可以使用以下手勢進行互動：

* **移動物體**：單指拖曳移動模型。
* **縮放物體**：雙指捏合縮放模型。
* **旋轉物體**：雙指旋轉轉動模型。

![Gesture Hints - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/gesture_hints.png#gh-light-mode-only)
![Gesture Hints - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/gesture_hints.png#gh-dark-mode-only)

### 3. 與 Holeplate 模型互動（兩種模式皆適用）

系統會以不同顏色標示模型的被選取狀態（點一下模型以選取；點其他地方以取消選取）：

* **選取中**：![#7a7afa](https://placehold.co/15x15/7a7afa/7a7afa.png) `#7a7afa`（淡紫色）。
* **未選取**：![#89929a](https://placehold.co/15x15/89929a/89929a.png) `#89929a`（冷灰色）。

![Selected vs Unselected Colors - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/selected_vs_unselected_colors.png#gh-light-mode-only)
![Selected vs Unselected Colors - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/selected_vs_unselected_colors.png#gh-dark-mode-only)

除此之外，畫面下方會出現控制面板（僅在模型被選中時顯示）：

* ⏯️ **播放/暫停動畫**：控制 Holeplate 的動畫播放與暫停。
* 🏷️ **切換孔號標籤**：顯示或隱藏 Holeplate 孔洞上的數字標籤。
* ⏱️ **調整動畫速度**：打開滑桿面板（範圍 1–20）以調整播放速度。
* 🧩 **步驟選擇（僅限教學模式）**：顯示可滑動的步驟列表，點擊任意步驟可直接跳轉到該教學階段。
* 🗑️ **移除當前物件**：從 AR 場景中移除當前放置的 Holeplate 模型。

在教學模式下，控制面板上方會顯示目前步驟的名稱，方便您隨時掌握進度。

![Display vs Tutorial Modes - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/display_vs_tutorial_modes.png#gh-light-mode-only)
![Display vs Tutorial Modes - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/display_vs_tutorial_modes.png#gh-dark-mode-only)

![Controls Preview - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/controls_preview.png#gh-light-mode-only)
![Controls Preview - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/controls_preview.png#gh-dark-mode-only)

> [!TIP]
> 如果在放置模型後未顯示控制面板，請再次點擊 Holeplate 模型以選取它。

### 4. 回到首頁與選單功能

![Home & Option Buttons - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/home_option_buttons.png#gh-light-mode-only)
![Home & Option Buttons - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/home_option_buttons.png#gh-dark-mode-only)

在畫面的左上角與右上角分別設有兩個常駐按鈕：

* 🏠 **首頁按鈕**：隨時返回模式選擇畫面。
* ⚙️ **選單按鈕**：開啟功能選單，內含：
    * 💡 **顯示互動提示**：顯示操作說明視窗。
    * 📡 **平面可視化**：切換顯示/隱藏 AR 平面。
    * 🧹 **移除所有物件**：移除所有已放置的模型。
    * 🧪 **AR 偵錯選單**：顯示進階 AR Session 資訊。

以上所有功能均可在任何模式下使用，方便您隨時返回首頁或調整設定。

![Visualize Surfaces Toggle - Light](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/light/visualize_surfaces_toggle.png#gh-light-mode-only)
![Visualize Surfaces Toggle - Dark](https://raw.githubusercontent.com/justinhshz/itriarmandoc/main/images/dark/visualize_surfaces_toggle.png#gh-dark-mode-only)

---

## 💬 意見回饋

🙏 感謝您使用 **AR Holeplate Manual**。歡迎提供您的寶貴意見，以幫助我們持續優化使用體驗。如需協助或有任何問題，請聯絡專案維護者或直接在本專案頁面提交 Issue 跟我們反應！
