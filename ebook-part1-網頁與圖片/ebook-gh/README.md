# mnanak na qalang 電子書

繪本電子書（20 頁），每頁有旁白與背景音樂，純靜態網頁，不需要安裝任何東西。

## 使用方式

- 點「開始閱讀」開始播放；之後用左右箭頭、鍵盤方向鍵或手機滑動翻頁。
- 頁面下方可開關「背景音樂」「旁白」，也可開啟「自動翻頁」（旁白播完後自動翻到下一頁）。

## 檔案結構

```
index.html          電子書主頁
images/p0–p19.jpg   各頁插圖（0 為封面）
images/left.jpg, right.jpg, read.jpg   導覽圖示
audio/speech/N.mp3  第 N 頁旁白
audio/music/N.mp3   第 N 頁背景音樂
audio/extra.mp3     尚未使用的額外音檔
```

## 發布到 GitHub Pages

1. 把整個資料夾上傳到一個 GitHub repository。
2. 到 repository 的 Settings → Pages。
3. Source 選 Deploy from a branch，Branch 選 `main`，資料夾選 `/ (root)`，按 Save。
4. 等一兩分鐘，網址會是 `https://<你的帳號>.github.io/<repository 名稱>/`。

要在本機預覽，請在資料夾內執行 `python3 -m http.server`，再用瀏覽器開 `http://localhost:8000`。直接雙擊 `index.html` 也能看圖，但部分瀏覽器會擋住音檔。

## 修改

- 頁數、音量等設定在 `index.html` 最下方的 `<script>` 開頭（`TOTAL`、`MUSIC_VOL`）。
- 要替換某頁的圖片或聲音，直接用同檔名覆蓋即可。
