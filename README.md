# eBookReader 2.3.1

Windows 電子書閱讀器。[下載 eBookReader.exe](https://github.com/vincentnes/eBookReader/raw/refs/heads/main/eBookReader.exe) 後雙擊啟動，無需安裝。

## 2.3.1 語言與選單顯示

修正 Zoom 的語言切換快取，保持原縮放選擇。下拉選項增加行距，放大地球圖示。首次啟動依 Windows 顯示語言選擇繁體／簡體／英文；其他系統語言預設英文，之後保留手動選擇。選項翻譯、間距、地球尺寸與語言映射測試通過。

## 2.3.0 介面語言

上方選單右側的小地球可切換繁體中文、简体中文與 English，記住選擇。提供選單、工具列、書庫群組、右鍵選項、說明與常用提示的語言文字。不翻譯文件內容、檔名與筆記；Windows 系統對話框按鈕依作業系統語言顯示。三種語言、英文說明、設定恢復與縮放值保持測試寫出通過結果，但測試程序結束等待曾逾時。簡繁字形轉換使用內建 .NET Framework Microsoft.VisualBasic，不依賴 WSH、VBA 或外部翻譯服務。

## 2.2.3 最近閱讀檢視

按左側時鐘會加深背景，並在書庫內只顯示最近閱讀，不再開啟小選單。再按時鐘或書庫圖示恢復 My Favorite → 資料夾 → 最近閱讀。最愛中的資料夾加上小資料夾圖示。檢視切換、選中顏色及恢復操作測試通過。

## 2.2.2 書庫順序與資料夾恢復

書庫固定依 My Favorite → 資料夾 → 最近閱讀 排列。重開程式顯示並展開上次選擇的資料夾；無法存取時保留位置並提示。開啟資料夾時展開書庫。資料夾選取標題移除貼路徑提示。編譯完成；本機 Application Control 阻擋本次回歸測試程序，未完成執行驗證。

## 2.2.1 目前文件轉 PDF

閱讀工具列的「轉成 PDF」針對目前開啟的 Word 文件，直接存到原資料夾並自動開啟。已有同名 PDF 時使用 (2)、(3) 等新檔名，避免覆蓋；非 Word 文件時停用按鈕。按鈕與儲存路徑測試通過。實際 Word 匯出仍有下述測試限制。

## 2.2.0 Word 轉 PDF

檔案 → Word 轉為 PDF 並閱讀，或在書庫對 .doc／.docx／.docm 按右鍵轉換。需要已安裝並啟用的桌面版 Microsoft Word；不引入第三方套件、WSH 或 PowerShell。選擇 PDF 儲存位置後，唯讀開啟文件、停用巨集與開啟時的連結更新，匯出成功後自動以 PDF 閱讀；恢復連結更新設定並關閉此次建立的 Word 實例。
目前只確認編譯完成；本機 Application Control 阻擋 Word 轉換測試程序，尚未完成實際匯出驗證。Office 自動化政策、啟用／登入提示、受保護或加密文件可能使轉換失敗或等待 Word 提示。轉換期間關閉閱讀器會提示等待完成。

## 2.1.7 字體與排版

選單與閱讀工具列採 12pt，書庫 11pt、標題 13pt；下拉選單同步字體並加寬，調整行距與留白。保留正文閱讀字級，窄視窗使用工具列展開選單。字級、版面、主題及窄視窗檢查通過。

## 2.1.6 Word 檔案列表

書庫列出 .docx（可閱讀），以及 .doc／.docm（標示請另存為 .docx）；排除 Word 的 ~$ 暫存鎖定檔。Word 列表與 DOCX 解析回歸測試通過。

## 2.1.5 間距與分隔

中間分隔線改為與其他分隔一致的細線，保留拖曳調整區。選單右移並增加項目間距與上下留白，選單下方加上細線區隔閱讀區。版面與主題測試通過。

## 2.1.4 選單與線條

修正最近閱讀選單關閉時提早釋放 ContextMenuStrip 的錯誤。加深區塊分隔線，書庫與時鐘圖示使用清楚的細線條。選單開關、開啟項目及右鍵選單切換測試通過。

## 2.1.3 書庫與最近閱讀

左側增加書庫與圓形時鐘圖示；書庫收合後仍可展開或開啟最近閱讀。最近閱讀提高至 20 筆，清單可右鍵管理；記住書庫收合狀態。導覽、全螢幕恢復與紀錄上限測試通過。

## 2.1.2 DOCX 文字閱讀

支援 Word .docx 本文文字，包括段落、表格文字、連結文字與換行；無需安裝 Word。不保留原始排版、圖片、頁首頁尾或註腳；不支援舊 .doc、密碼加密檔。可使用既有分頁、Highlight、筆記與閱讀進度功能。解析與損壞檔案測試通過。

## 2.1.1 閱讀工具列

將翻頁、縮放、編碼、筆記本與全螢幕工具列移到右側內容區頂部；左側書庫上移至選單下方。版面、全螢幕恢復與 PDF 捲動測試通過。

## 2.1.0 外觀與主題

整理側欄與淺色介面：增加書庫／書名標題、階層展開箭頭、較寬行距、群組標題與選取色。檢視 → 主題提供淺色、深色、護眼，記住前次選擇；Ctrl+B 可顯示／隱藏書庫。主題、版面與八頁 PDF 連續捲動測試通過。

## 2.0.6 選單

將選單名稱改為「說明」，保留使用說明與關於功能。

## 2.0.5 圖示

採用左右平衡的書頁與右上小折角，保留深色輪廓改善小尺寸辨識；Help 的關於視窗顯示 2.0.5。圖示與視窗載入檢查通過。

## 2.0.4 圖示與 Help

加深圖示上緣並簡化書頁，改善小尺寸辨識。新增 Help 使用說明（F1）與關於視窗，顯示實際版本。圖示、Help 內容、版本與啟動檢查通過。

## 2.0.3 圖示

採用灰藍書封、柔和書頁與陶土色書籤的第二版圖示；嵌入 EXE 與視窗。圖示載入、視窗啟動與關閉檢查通過。

## 2.0.2 修正

修正 PDF／圖片翻頁後圖片本身偏離內容框頂部。先歸零捲動位置再重設圖片座標；八頁連續捲動測試同時驗證捲軸與實際圖片頂端。

## 2.0.1 修正

修正 PDF／圖片滾輪被外層控制項重複處理、頁尾提早翻頁與初始內容區寬度。八頁 PDF 測試確認每頁到達底部後才翻下一頁，頁碼依序 1–8。

## 2.0 更新

改為直接執行的 C#／.NET Framework 程式。啟動時不再解包腳本、不啟動 PowerShell，也不需要執行期間編譯程式碼。

目前未使用可信任的程式碼簽章。此次改寫不保證 Chrome Safe Browsing、SmartScreen 或組織政策解除封鎖；不應僅憑 Defender 掃描結果認定所有警告都是誤報。

## 系統需求

Windows 10／11 與 .NET Framework 4.8。PDF 使用 Windows 內建 PDF API。CHM 由 Windows HTML Help 解壓為文字，不執行其中的網頁腳本。

## 支援格式

- PDB：PalmDOC（TEXtREAd）、舊版 iSilo（ToGoToGo）。
- DOCX、TXT、MD、HTML、RTF、FB2、EPUB、CHM：以文字閱讀，EPUB 不支援加密章節。
- PDF、CBZ、JPG、JPEG、PNG、BMP、GIF、TIF、TIFF：以頁面／圖片閱讀。GIF 與 TIFF 顯示第一個影格。
- 圖片資料夾依檔名自然排序逐頁閱讀。

## 操作

- 檔案選單：開啟檔案、資料夾、圖片資料夾、儲存進度；左側提供實際資料夾樹、My Favorite 與最近二十個檔案。
- Ctrl+O 開啟檔案；Ctrl+Shift+O 開啟資料夾；Ctrl+S 儲存進度；Ctrl+D 加入／移除最愛。
- 資料夾選擇器可貼路徑，記住前次資料夾。
- 樹狀圖按右鍵：開啟所在資料夾、複製路徑、管理最愛或移除最近閱讀連結。
- F11 全螢幕；Esc 離開全螢幕。
- Ctrl+滾輪縮放；一般滾輪、上下鍵與 Page Up／Down 捲動並於邊界翻頁；左右鍵直接翻頁。
- PDF／圖片單擊符合頁寬；雙擊在整頁與頁寬之間切換。
- PDF／圖片放大超出視窗後，按住 Ctrl+滑鼠左鍵拖曳頁面。
- 文字選取後按右鍵 Highlight 或加入筆記；筆記本可編輯、前往原文、刪除與匯出 Markdown。
- PDF／圖片提供頁面筆記，目前沒有文字選取或 OCR。

既有閱讀紀錄沿用 %APPDATA%\PdbReader\state.json；保存進度、最愛、Highlight 與筆記。文字閱讀以固定字數分頁。

## 發行與測試

本 repository 只提供執行檔、說明與 SHA-256 校驗碼；不包含原始碼、測試資料、書籍或個人閱讀紀錄。

2026-10-08：直接針對最終發行組件驗證 PalmDOC／iSilo、PDF 繪製、EPUB、CHM、CBZ、RTF、FB2、TXT、圖片自然排序、閱讀進度、Highlight／筆記、雙擊頁寬／整頁、全螢幕及資料夾選擇器。回歸測試通過。
安全狀態（2026-10-08）：使用者已回報改為 C# 2.0 後，另一台電腦的 Chrome 下載封鎖解除；Windows 仍顯示未簽章／未知發行者提示。這是使用者已確認的結果，不代表每個後續版本或每台公司電腦都已驗證。
開發電腦對 2.0.2 EXE 的 Microsoft Defender 掃描結果為未發現威脅；這只記錄該次本機掃描，不代表使用者電腦的 Defender 結果或企業允許執行。

## 公司電腦相容性

目前依 C# 2.0.2 原始碼檢查；尚未在套用企業政策的電腦全面驗證。

| 元件／政策 | 使用情況與影響 |
| --- | --- |
| WSH（wscript.exe／cscript.exe）、VBScript／JScript | 不使用。停用 WSH 不影響本程式。 |
| 桌面 Word／Office COM 自動化 | 只有 Word 轉 PDF 使用；缺少、未啟用或被公司政策限制時，無法轉換，不影響既有解析器的文字閱讀。 |
| PowerShell、cmd、執行期間編譯器 | 發行版不使用。native/Build.ps1 與測試是開發工具，不隨 EXE 發行。 |
| 未簽章 EXE／AppLocker／WDAC／Smart App Control | 可能直接阻擋啟動；需由 IT 依公司政策核准。Chrome 可下載不代表公司允許執行。 |
| HTML Help（hh.exe）與子程序限制 | 只有 CHM 解壓時使用；若禁止啟動 hh.exe，未快取的 CHM 無法讀取，其他格式不依賴它。 |
| Explorer（explorer.exe）與子程序限制 | 只有「打開所在資料夾」使用；被限制時該功能可能無法開啟。 |
| Shell COM／IFileDialog | 現代資料夾選擇器使用 Windows Shell COM；不是 WSH／ActiveX 網頁腳本。Shell COM 元件受限時可能無法選資料夾，開啟檔案仍可另外嘗試。 |
| .NET Framework | 需要 Windows 的 .NET Framework 4.x；建議 4.8。無需另外安裝 Python、Node、Java 或 PowerShell。 |
| Windows PDF／WinRT API | PDF 使用 Windows.Storage、Windows.Data.Pdf；不需要 Edge、WebView2 或 Adobe Reader。元件缺少或受到限制時可能無法讀取 PDF。 |
| 檔案與 AppData 寫入權限 | 需要讀取書籍，並寫入 %APPDATA%\PdbReader 的設定與 CHM 快取。若寫入被禁止，儲存可能失敗；目前關閉時儲存失敗會提示並取消關閉。 |
| Controlled Folder Access／DLP／分享資料夾權限 | 可能限制書籍存取、複製摘錄、剪貼簿或 Markdown 匯出；影響取決於公司設定。 |
| 網路／代理伺服器 | 閱讀器本身沒有下載、更新、遙測或網路請求。書籍位於網路分享時仍需該分享的存取權限。 |

閱讀不需要系統管理員權限。不會修改系統安全設定，也不會執行 HTML／CHM 內的網頁腳本。CHM 解壓會將書籍副本與內容寫入使用者快取，需有足夠磁碟空間。

公司若封鎖應用程式，請交由 IT 檢視 EXE 校驗碼、AppLocker／Code Integrity／端點防護事件；不要以停用公司安全政策作為相容性處理。

參考：[Microsoft 應用程式控制](https://learn.microsoft.com/en-us/windows/security/application-security/application-control/app-control-for-business/appcontrol)、[受控資料夾存取](https://learn.microsoft.com/en-us/defender-endpoint/controlled-folders)。
