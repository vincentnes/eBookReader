# eBookReader 2.0.1

Windows 電子書閱讀器。[下載 eBookReader.exe](https://github.com/vincentnes/eBookReader/raw/refs/heads/main/eBookReader.exe) 後雙擊啟動，無需安裝。

## 2.0.1 修正

修正 PDF／圖片滾輪被外層控制項重複處理、頁尾提早翻頁與初始內容區寬度。八頁 PDF 測試確認每頁到達底部後才翻下一頁，頁碼依序 1–8。

## 2.0 更新

改為直接執行的 C#／.NET Framework 程式。啟動時不再解包腳本、不啟動 PowerShell，也不需要執行期間編譯程式碼。

目前未使用可信任的程式碼簽章。此次改寫不保證 Chrome Safe Browsing、SmartScreen 或組織政策解除封鎖；不應僅凭 Defender 掃描結果認定所有警告都是誤報。

## 系統需求

Windows 10／11 與 .NET Framework 4.8。PDF 使用 Windows 內建 PDF API。CHM 由 Windows HTML Help 解壓為文字，不執行其中的網頁腳本。

## 支援格式

- PDB：PalmDOC（TEXtREAd）、舊版 iSilo（ToGoToGo）。
- TXT、MD、HTML、RTF、FB2、EPUB、CHM：以文字閱讀，EPUB 不支援加密章節。
- PDF、CBZ、JPG、JPEG、PNG、BMP、GIF、TIF、TIFF：以頁面／圖片閱讀。GIF 與 TIFF 顯示第一個影格。
- 圖片資料夾依檔名自然排序逐頁閱讀。

## 操作

- 檔案選單：開啟檔案、資料夾、圖片資料夾、儲存進度；左側提供實際資料夾樹、My Favorite 與最近十個檔案。
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
本機 Microsoft Defender 對最終 EXE 掃描未發現威脅。尚未驗證 Chrome 下載封鎖是否解除。
