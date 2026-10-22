# 互動遊戲站（純瀏覽器版）

剪刀石頭布 AI 對戰 + 67 Speed 手臂速度挑戰，部署在 https://iamsigmaeiku.com/games/ 。
全部在瀏覽器端用 MediaPipe 辨識，不需要後端。

- `public/games/index.html` 選單
- `public/games/rps.html` 剪刀石頭布（HandLandmarker，隨機 / 策略 AI）
- `public/games/speed67.html` 67 挑戰（PoseLandmarker，排行榜存在各自裝置的 localStorage）
- `wrangler.jsonc` 獨立 Cloudflare Worker（靜態資產），只接 `/games`，不碰根路徑的 `balancer`

部署：`npx wrangler deploy`
本機測試：`cd public && python -m http.server 8000`，開 http://localhost:8000/games/
鏡頭需要 HTTPS（或 localhost）。
