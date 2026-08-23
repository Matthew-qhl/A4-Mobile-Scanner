A4 離線文件掃描器 v2
======================

這一版已移除所有 CDN、OpenCV.js、jsPDF 及雲端 API 依賴。
影像校正、去陰影、白紙校正、彩色印章/簽名保護及 PDF 建立全部在手機本機完成。
相片不會上傳伺服器。

新增功能
1. 自動找 A4 / 文件四邊（離線 Sobel + line search），並可拖動四角微調。
2. 去陰影 / 光暗差。
3. 去黃及白紙校正。
4. 彩色印章及簽名保護。
5. 多頁掃描：加入頁面、刪除、上下重新排序、合併多頁 A4 PDF。
6. 自動檔名：A4Scan_YYYYMMDD_HHmm，可自行修改。

其他功能
- 透視/梯形校正
- A4 150 / 200 / 300 dpi
- 彩色 / 灰階 / 黑白 / 只校正
- JPG / 多頁 PDF
- PWA 安裝到 iPhone / Android 主畫面
- Service Worker 離線快取

手機使用
A. PWA（推薦）
1. 把整個 a4_mobile_scanner 資料夾放在任何 HTTPS 靜態網站或公司內聯網 HTTPS 網站。
2. 第一次連線打開 index.html。
3. iPhone Safari：分享 → 加入主畫面；Android Chrome：安裝應用程式。
4. 第一次載入完成後，可切斷 Wi‑Fi / 5G 再開 App，仍可使用全部掃描及 PDF 功能。

B. 完全單檔
index.html 已包含全部程式邏輯，不需要外部 JS。桌面瀏覽器可直接開啟。
在 iOS 上如直接由「檔案」開 HTML，系統可能以預覽器而非 Safari 執行，因此 PWA 方式較可靠。

注意
- 自動找紙邊是本機演算法，背景與紙張顏色太接近時仍可能需要手動拉四角。
- 300 dpi 多頁文件會使用較多記憶體；舊手機如一次處理大量頁面，建議改用 200 dpi。
- 本版不做 OCR，所以「自動檔名」以日期/時間產生，不會從文件文字判斷公司名或文件類別。


v4.1 adds Ultra HD mode, fold/crease attenuation, glare/backlight suppression, stronger local illumination correction and text sharpening.
