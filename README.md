# Headless WordPress In Subdirectory
把 WordPress 安裝在子資料夾，讓前後端使用同一個 Domain，以求簡單快速地解決因瀏覽器 CORS 政策無法攜帶 credentials cookies 的問題

## Installation
1. 拉下本專案
``` bash
npx degit git@github.com:vann-at-cpcp-dot-tw/Headless-WordPress-In-Subdirectory.git
```

2. 建立前後端資料夾
``` bash
mkdir backend frontend
```

3. 起 Docker 服務
```bash
docker compose up
```

4. 將 WordPress 檔案下載至 backend 資夾
```bash
cd backend
npx degit git@github.com:WordPress/WordPress.git
```

5. 將 backend-sample 內的必要設定檔，同步到 backend 資料夾
6. 進入 [http://localhost:9001/backend](http://localhost:9001/backend) 將 WordPress 初始化
7. 將前端專案(如：Next.js、Create React App)放入 frontend 資料夾，並啟動前端服務
8. 快樂使用 Headless WordPress
