# Headless WordPress In Subdirectory
把 WordPress 安裝在子資料夾，讓前後端使用同一個 Domain，以求簡單快速地解決因瀏覽器 CORS 政策無法攜帶 credentials cookies 的問題

## Installation
1. 建立前後端資料夾
``` bash
mkdir backend frontend
```

2. 起 Docker 服務
```bash
docker compose up
```

3. 將 WordPress 檔案下載至 backend 資夾
```bash
cd backend
npx degit git@github.com:WordPress/WordPress.git
```

4. 將 backend-sample 內的必要設定檔，同步到 backend 資料夾

5. 進入瀏覽器將 WordPress 初始化： [http://localhost:9001/backend](http://localhost:9001/backend)

6. 將前端檔案放進 frontend 資料夾，起 node 服務，快樂使用 Headless WordPress
