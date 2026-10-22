# 互動遊戲站（純瀏覽器版）

剪刀石頭布 AI 對戰 + 67 Speed 手臂速度挑戰。全部在瀏覽器端用 MediaPipe 辨識，不需要後端，
可直接部署成靜態網站（Cloudflare Pages / GitHub Pages）。

- `index.html` 選單
- `rps.html` 剪刀石頭布（MediaPipe HandLandmarker，支援隨機 / 策略 AI）
- `speed67.html` 67 挑戰（MediaPipe PoseLandmarker，排行榜存在各自裝置的 localStorage）

部署設定：不需 build，輸出目錄設為專案根目錄（`/`）。
鏡頭需要 HTTPS（或 localhost）才能使用。

本機測試：`python -m http.server 8000` 後開 http://localhost:8000
