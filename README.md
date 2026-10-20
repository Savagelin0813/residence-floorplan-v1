# Residence Studio V1 — 自建住宅 3D 概念設計

可直接以瀏覽器開啟 `index.html` 的離線互動式住宅展示與室內概念配置工具。

## 立即使用

1. 解壓縮 ZIP。
2. 雙擊 `index.html`，以 Chrome、Edge 或 Safari 開啟。
3. 左側切換 1F~5F、開啟「樓層爆炸圖」，拖曳轉動視角、滾輪縮放。
4. 右側點房間，可修改名稱和房間類型，按「套用房間修改」。
5. 使用「儲存瀏覽器」儲存本機設定，或「匯出 JSON」下載模型資料。之後可匯入 JSON。

## 專案檔案

- `index.html`：完整可執行的 HTML、CSS、JavaScript，採原生 Canvas 2D 手工投影 3D 模型，無網路和第三方相依套件。
- `data/building.json`：同一份範例的獨立 JSON，供未來交換資料及程式擴充。網頁已內建對應資料，開檔不必 fetch。
- `README.md`：本說明。

## 功能範圍

- 五樓獨棟住宅模型、全部樓層與個別樓層顯示
- 可視化分層爆炸圖（Animated Exploded View）
- 自由旋轉、縮放、俯視、立面、自動旋轉
- 牆體透明度、房間標籤、家具與基地顯示
- 房間名稱與類型編輯
- JSON 匯入、匯出；本機 localStorage 儲存
- 手機觸控

## V1 限制與已知待改善

1. 原生 Canvas 多邊形投影引擎採 painter's algorithm，透明牆遮擋順序與重疊幾何可能不完全精確，不是 Three.js 真 3D 渲染器。日後可替換 WebGL Three.js 實作並沿用 JSON 資料結構。
2. V1 目前沒有 CAD / DWG / DXF 直接匯入，也沒有拖曳編修房間尺寸／牆壁頂點；目前只能編輯名稱、類型，以及匯入經外部編輯的 JSON。
3. `data/building.json` 供資料交換；直接修改此檔不會自動更新網頁，須使用網頁「匯入 JSON」。
4. 車輛、家具模型僅為基本幾何示意，非精細模型；各房間動線與垂直動線尚需進一步整合。
5. 樓層、面積及入口配置都是示意，沒有依真實地籍或法規檢核，不能當施工圖使用。

## 上 GitHub Pages

在新的 GitHub repository 上傳 `index.html`、`README.md`、`data/` 資料夾；到 Settings > Pages > Build and deployment > Deploy from a branch，選 `main` / `/ (root)`。幾分鐘後就能用 `https://帳號.github.io/專案名稱/` 瀏覽。

## 設計參考與著作權

互動方式參考公開作品 `https://github.com/kv1012tiger/library-3d-floorplan`，但 V1 為重新撰寫的 HTML / CSS / JavaScript，沒有複製該專案程式碼或素材。請注意原作者專案公開不代表自動授權重製。
