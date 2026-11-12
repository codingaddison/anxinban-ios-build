# anxinban-ios-build

Builds the iPhone install file (`.ipa`) of 安心BAN from
[zeroleafx/AnXinBan-Taiwanese-Assitant](https://github.com/zeroleafx/AnXinBan-Taiwanese-Assitant)
on GitHub's macOS machines, so it can be installed from Windows.
This repository holds only the build setup, no app code.

## 做一個新的安裝檔

Actions → **Build iPhone install file** → **Run workflow**，填要編的分支
（預設 `main`）。大約 15 到 30 分鐘，做好後在那一次執行的頁面下方
Artifacts 下載 `AnXinBan-xxxxxxx`（下載下來是 zip，解開就是 `.ipa`）。

## 裝到 iPhone（Windows）

1. 安裝 Apple 官網版 iTunes（不是 Microsoft Store 版）和
   [Sideloadly](https://sideloadly.io/)。
2. iPhone 用線接電腦，在手機上按「信任這部電腦」。
3. 把 `.ipa` 拖進 Sideloadly，輸入你的 Apple ID，按 Start。
   如果說 bundle ID 不能用，在 Advanced options 勾選更改 bundle ID 再試。
4. iPhone：設定 → 隱私權與安全性 → 開發者模式，打開後重新開機。
5. iPhone：設定 → 一般 → VPN 與裝置管理，信任你的 Apple ID。

免費 Apple ID 裝的 App 每 7 天要重新簽一次；Sideloadly 可以設定自動續簽。
App 第一次打開會下載約 1.08 GB 的語音模型，請連 Wi-Fi。
