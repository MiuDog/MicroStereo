# MicroStereo

以微立體表面、暖灰配色與獨立分頁 Panel 為特色的 Obsidian 純 CSS 佈景主題。設計源自 [Kallopis](https://github.com/technis-toolbox/Kallopis/tree/main/docs/design-tokens) 的「現代生產力」風格，支援亮色與深色，無需功能外掛。

目前版本：**0.1.31**。

## 下載與安裝

| 平台 | 安裝方式 |
| --- | --- |
| Windows／macOS／Linux | 下方 ZIP 手動安裝 |
| Android | [下載 ZIP、顯示隱藏資料夾並安裝](INSTALL.md#android) |
| iPhone／iOS | [使用 BRAT 從 GitHub 安裝](INSTALL.md#ios) |
| iPad／iPadOS | [使用 BRAT 從 GitHub 安裝](INSTALL.md#ipados) |

[完整跨平台安裝指南](INSTALL.md)。iPhone／iPad 可以下載 ZIP，但系統「檔案」App 無法直接管理隱藏的 `.obsidian`，不能照桌面的解壓步驟操作；手機上的 BRAT 僅協助安裝／更新，主題本身仍是純 CSS。

### 桌面 ZIP 安裝

從 [最新 Release](https://github.com/MiuDog/MicroStereo/releases/latest) 下載 `MicroStereo-0.1.31-install.zip`。

1. 將安裝包直接解壓至 Obsidian **筆記庫根目錄**。
2. 確認檔案位於 `.obsidian/themes/MicroStereo/`。
3. 在「設定 → 外觀 → 佈景主題」選擇 **MicroStereo**。

若主題尚未出現，重新開啟筆記庫。這是手動安裝包，尚未提交至 Obsidian 社群主題目錄。

也可下載 `MicroStereo-0.1.31.zip`，將其中的 `MicroStereo` 資料夾放入 `.obsidian/themes/`。請擇一安裝。

## 風格與設定

- 微立體側欄與主內容區、各自獨立的分頁 Panel。
- 平面選單、實線外框與框內細斜線；Tooltip 使用側欄底色與虛線外框。
- 連結、Tag、文字標記、主要按鈕與輸入框焦點跟隨使用者輔色。
- 紅叉／綠勾正方形開關、2px 軌道內距，按壓不放大。
- 不透明微立體 Callout、保留內部格線的圓角表格。
- 普通內文使用次要文字色，有背景元件保留主文字對比；標題不變、粗體採輔色、斜體採低對比純色。
- 內嵌 Noto Sans TC 與 IBM Plex Mono，無須額外安裝或連線載入字型。

明暗模式沿用 Obsidian「基本佈景主題」。正文全寬由「設定 → 編輯器 → 可讀行寬」控制：開啟限制行寬，關閉使用可用全寬。

極深色為選用片段：將 [extras/MicroStereo-ultra-dark.css](extras/MicroStereo-ultra-dark.css) 放入 `.obsidian/snippets/`，在外觀設定啟用，再切換為深色模式。

## 支援範圍

以桌面端為視覺基準，行動端共用配色、字體、圓角及微立體陰影；iPad 分頁、抽屜／固定側欄、設定與底部導覽已另行適配。行動控制保留 44px 觸控高度，側欄與鍵盤仍由 Obsidian 原生管理。

驗證環境為 Windows 桌面版 Obsidian 1.14.5 及其 Chromium 行動模擬器：涵蓋 iPad 橫直向、手機窄螢幕、明暗及閱讀／編輯模式。模擬器內共用元件的 70 項樣式比較與桌面相同；這不等於實體 iPadOS WebKit／Android 裝置驗收，也不保證不同引擎逐像素相同。第三方外掛未完整驗收。

完整下拉外觀需要引擎支援 `appearance: base-select`；舊引擎保留原生選單。`contrast-color()` 不受支援時，主要按鈕文字使用回退色。Electron 原生文字選取選單不受主題 CSS 控制。iPad／iPhone 的系統選取器保留原生介面；主題只能修改頁面內的下拉控制外觀。

主題不改寫 Markdown 或編輯器邏輯。編輯來源行保留自然行高，不強制壓成閱讀高度；普通段落開頭的 Tab 可能由 Markdown 解析器移除，需保留階層時請使用巢狀清單或程式碼區塊。不保證任意文件、字型、縮放與作用行語法在兩種模式完全一致。

## 開發與授權

執行檔為 `theme.css` 與 `manifest.json`；[架構說明](architecture.md)。程式碼採 Tab 縮排、顯示寬度 2。

主題採 [MIT License](LICENSE)。字型分別遵循 [Noto Sans TC OFL](licenses/OFL-NOTO-SANS-TC.txt) 與 [IBM Plex OFL](licenses/OFL-IBM-Plex.txt)，保留 Kallopis 設計來源及原始著作權聲明。
