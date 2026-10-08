# eBookReader

Windows 電子書閱讀器，直接下載 [eBookReader.exe](https://github.com/vincentnes/eBookReader/raw/refs/heads/main/eBookReader.exe) 後雙擊啟動，無需安裝。

## 系統需求

Windows 10／11，內建 Windows PowerShell 5.1 與 .NET Framework 4.x。這是未簽章的執行檔；Windows 或組織的應用程式控制政策可能阻擋啟動。

## 支援格式

- PDB：PalmDOC（TEXtREAd）、舊版 iSilo（ToGoToGo）。
- TXT、MD、HTML、RTF、FB2、EPUB、CHM：以文字閱讀。
- PDF、CBZ、JPG、JPEG、PNG、BMP、GIF、TIF、TIFF：以頁面／圖片閱讀。GIF 與 TIFF 顯示第一個影格。
- 圖片資料夾可依檔名自然排序逐頁閱讀。

## 操作

- 檔案選單可開啟檔案、資料夾、儲存進度；左側提供實際資料夾樹、My Favorite、最近十個檔案。
- 開啟資料夾可貼上路徑，並記住前次資料夾。
- 最近閱讀連結可按右鍵開啟所在資料夾、複製路徑、加入最愛或移除連結。
- F11：全螢幕；Esc：離開全螢幕。
- Ctrl＋滾輪：縮放；一般滾輪與 Page Up／Down：捲動閱讀；左右鍵：翻頁。
- PDF／圖片單擊：符合頁寬；雙擊：在整頁與頁寬之間切換。
- 放大超出視窗後，按住 Ctrl＋滑鼠左鍵拖曳頁面。
- 文字選取後按右鍵，可 Highlight 或加入筆記；PDF／圖片目前提供頁面筆記，沒有文字選取或 OCR。

閱讀進度、最愛及筆記保存在使用者的 AppData 資料夾。首次啟動會將執行模組解包到使用者的 LocalAppData 快取。

## 發行內容與驗證

本 repository 只提供執行檔、說明與 SHA-256 校驗碼；不提供原始碼、書籍、測試資料或個人閱讀紀錄。
執行所需模組內嵌於 EXE；這種封裝不代表防止逆向工程。

2026-10-08：完成編譯與內嵌內容檢查；原程式的選取／縮放及 Ctrl 拖曳回歸測試通過。打包後 EXE 的實際啟動測試被測試電腦的 Application Control 政策阻擋，尚未在允許此執行檔的 Windows 環境驗證啟動。