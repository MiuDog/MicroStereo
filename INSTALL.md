# MicroStereo 跨平台下載與安裝

本指南適用已發布的 **v0.1.29**。Android、iPhone 與 iPad 使用同一份主題檔案；安裝方式因系統的檔案存取限制而不同。尚未提交至 GitHub 的本機開發變更，不會透過 Release 或 BRAT 取得。

| 平台 | 建議方式 | 入口 |
| --- | --- | --- |
| Android | 解壓主題 ZIP，放入筆記庫的 themes 資料夾 | [Android 步驟](#android) |
| iPhone／iOS | BRAT 從 GitHub 安裝，不必操作隱藏資料夾 | [iPhone 步驟](#ios) |
| iPad／iPadOS | BRAT 從 GitHub 安裝 | [iPad 步驟](#ipados) |
| Windows／macOS／Linux | 將安裝 ZIP 解壓至筆記庫根目錄 | [桌面步驟](#desktop) |

MicroStereo 尚未收錄至 Obsidian 社群主題目錄，無法直接在「外觀 → 管理」搜尋安裝。以下方式皆安裝主題，不匯入或覆寫筆記庫設定。

<a id="android"></a>
## Android

1. 在手機瀏覽器下載 [MicroStereo-0.1.29.zip](https://github.com/MiuDog/MicroStereo/releases/download/v0.1.29/MicroStereo-0.1.29.zip)。
2. 使用檔案管理器解壓，找到包含 `theme.css`、`manifest.json`、`LICENSE`、`licenses` 的 **MicroStereo 資料夾**。若外層還有以 ZIP 檔名命名的資料夾，請使用內層 MicroStereo。
3. 在檔案管理器中啟用「顯示隱藏檔案」，找到 Obsidian 實際開啟的筆記庫。
4. 將整個 MicroStereo 資料夾複製到該筆記庫的 `.obsidian/themes/`；若 `themes` 不存在，可建立它。
5. 完整關閉並重新開啟該筆記庫，進入「設定 → 外觀」，在**已安裝主題的下拉選單**選擇 **MicroStereo**。

如果檔案管理器沒有顯示隱藏檔案的功能，可改用支援該功能的檔案管理器，或使用下方的 [BRAT 方式](#brat)，不用手動複製。

正確層級如下，不應多包一層同名資料夾：

```text
筆記庫/
	.obsidian/
		themes/
			MicroStereo/
				theme.css
				manifest.json
				LICENSE
				licenses/
```

Android 隱藏設定資料夾的處理方式見 [Obsidian 官方說明](https://obsidian.md/help/configuration-folder)。使用 Files by Google 時，可參考其[解壓說明](https://support.google.com/files/answer/9048509)。

<a id="ios"></a>
## iPhone／iOS

iOS 可以下載及解壓 ZIP，但內建「檔案」App 沒有預設方式存取 `.obsidian`。因此建議直接使用 [BRAT 安裝流程](#brat)，不需要先下載 ZIP。

若不使用社群外掛，可採用 [支援隱藏檔案的手動方式](#ios-manual)。

<a id="ipados"></a>
## iPad／iPadOS

iPadOS 與 iOS 有相同的隱藏資料夾限制，使用下方相同的 [BRAT 安裝流程](#brat)。安裝時請先開啟你要套用主題的筆記庫，每個筆記庫各自管理主題。

<a id="brat"></a>
## BRAT 安裝流程：Android／iPhone／iPad

1. 在 Obsidian 開啟目標筆記庫。
2. 進入「設定 → 社群外掛」。若尚未啟用社群外掛，先依畫面啟用，再點「瀏覽」。
3. 搜尋 **BRAT**，安裝並啟用。
4. 開啟 Obsidian 的命令面板，搜尋 BRAT 的主題命令 **Grab a beta theme for testing from a GitHub repository**。不同版本可能加上 `Themes:` 前綴；請選擇 **theme**，不是 plugin 的安裝命令。
5. 在提示框輸入：`https://github.com/MiuDog/MicroStereo`。
6. 確認安裝並等待完成。BRAT 會下載主題並切換套用；若尚未切換，進入「設定 → 外觀」選擇 **MicroStereo**。

已安裝並啟用 BRAT 時，也可以使用以下 URI，交由 Obsidian／BRAT 處理：

```text
obsidian://brat?theme=https://github.com/MiuDog/MicroStereo
```

BRAT 是安裝／更新工具，MicroStereo 本身仍只有 CSS，沒有主題功能外掛。BRAT 從 GitHub 主題檔案安裝；更新可使用 BRAT 的 theme 更新命令，不會取得只存在開發者電腦上的變更。

操作依據：[BRAT 作者指南](https://tfthacker.com/brat-quick-guide)、[主題檔案與更新機制](https://tfthacker.com/brat-themes)、[安裝 URI](https://tfthacker.com/brat-protocol)。

<a id="ios-manual"></a>
## iPhone／iPad 手動安裝：不使用 BRAT

1. 下載 [MicroStereo-0.1.29.zip](https://github.com/MiuDog/MicroStereo/releases/download/v0.1.29/MicroStereo-0.1.29.zip)，不要使用隱藏資料夾結構的 install ZIP。
2. 在「檔案」App 點一下 ZIP 解壓，找到內層 MicroStereo 資料夾。
3. 使用能查看／編輯隱藏檔案的檔案管理工具，開啟目標筆記庫。可參考 Obsidian 官方列出的工具；內建「檔案」App 本身不提供這項存取能力。
4. 將 MicroStereo 複製至 `.obsidian/themes/`，保留其內 `theme.css`、`manifest.json` 與授權檔案。
5. 重新開啟筆記庫，在「設定 → 外觀」選擇 MicroStereo。

[Apple ZIP 解壓說明](https://support.apple.com/en-is/102532)、[Obsidian iOS／iPadOS 設定資料夾說明](https://obsidian.md/help/configuration-folder)。

<a id="desktop"></a>
## Windows／macOS／Linux

1. 下載 [MicroStereo-0.1.29-install.zip](https://github.com/MiuDog/MicroStereo/releases/download/v0.1.29/MicroStereo-0.1.29-install.zip)。
2. 解壓至筆記庫根目錄，讓主題位於 `.obsidian/themes/MicroStereo/`。
3. 重新開啟筆記庫，在「設定 → 外觀」選擇 MicroStereo。

<a id="troubleshooting"></a>
## 找不到主題時

- 確認放入的是 Obsidian 目前開啟的筆記庫；手機與電腦可能使用不同筆記庫或設定資料夾。
- 確認不是把 ZIP 本身放進 themes；Obsidian 需要解壓後的 `theme.css` 與 `manifest.json`。
- 確認沒有變成 `themes/MicroStereo/MicroStereo/` 或 `themes/MicroStereo/.obsidian/themes/…`。
- 關閉並重新開啟 Obsidian 後再查看外觀下拉選單。
- 若你使用自訂設定資料夾，請以該資料夾取代 `.obsidian`。

目前主要外觀驗證環境仍是 Windows 桌面版 Obsidian 1.14.5。此文件提供行動裝置的安裝方法，不代表 Android、iOS 或 iPadOS 的全部畫面已經過實機視覺驗收。

## 更新至 0.1.29

此版補上行動端微立體、配色與 iPad 橫直向版型。已安裝者以 BRAT 更新 `MiuDog/MicroStereo`，或重新下載本頁新版 ZIP 並覆蓋主題資料夾，然後重新啟動 Obsidian。主題仍為純 CSS，不需新增功能外掛。

行動視覺以桌面為基準；觸控控制保留 44px 高度。已用 Obsidian 行動模擬器檢查，尚未完成實體 iPad／Android 裝置驗收。
