# 山野是一所學校 — 期刊網站

## 資料夾結構

```
shanye/
├── index.html          ← 首頁（不需修改）
├── viewer.html         ← 閱讀器（不需修改）
├── issues.json         ← 期刊設定檔（每次更新只改這裡）
└── issues/
    ├── 2025-03/        ← 每期一個資料夾
    │   ├── page-01.jpg
    │   ├── page-02.jpg
    │   └── ...
    └── 2024-09/
        ├── page-01.jpg
        └── ...
```

---

## 圖片命名規則

每頁圖片請依序命名：

```
page-01.jpg
page-02.jpg
page-03.jpg
...
page-10.jpg
page-11.jpg
```

支援格式：`jpg`、`jpeg`、`png`、`webp`

---

## 新增一期的步驟

1. **建立新資料夾**，例如 `issues/2025-09/`

2. **把圖片放進去**，命名為 `page-01.jpg`、`page-02.jpg`……

3. **編輯 `issues.json`**，在最前面加一筆：

```json
[
  {
    "vol": "Vol.2 No.1",
    "date": "2025 年 9 月",
    "pages": 24,
    "folder": "2025-09",
    "description": "本期簡介文字（可留空）"
  },
  ...（舊的保留在後面）
]
```

4. **Push 到 GitHub** → 網站自動更新

---

## 封面縮圖（可選）

如果想在首頁顯示封面圖片，在 `issues.json` 加上 `"cover"` 欄位：

```json
{
  "vol": "Vol.2 No.1",
  "date": "2025 年 9 月",
  "pages": 24,
  "folder": "2025-09",
  "cover": "page-01.jpg",
  "description": "本期簡介"
}
```

---

## 部署到 GitHub Pages

1. 在 GitHub 建立新的 Repository（名稱自訂）
2. 把所有檔案 Push 上去
3. 進入 Repository → Settings → Pages
4. Source 選 `Deploy from a branch`，Branch 選 `main`，資料夾選 `/ (root)`
5. 儲存後等 1–2 分鐘，網址會出現在 Pages 設定頁面

---

## 閱讀器操作

| 操作 | 功能 |
|------|------|
| 點擊頁面邊緣 | 翻頁 |
| 拖曳頁角 | 翻頁 |
| ← → 方向鍵 | 翻頁 |
| 底部按鈕 | 上一頁 / 下一頁 |
