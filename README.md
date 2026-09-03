# ONCE 收藏冊 ・ TWICE 入坑指南

粉絲自製的非官方 TWICE 入坑指南，純靜態單頁網站，透過 GitHub Actions 自動部署到 GitHub Pages。

## 結構

```
index.html               全部的 HTML / CSS / JS（無框架、無 build）
img/*.jpg                成員大頭照（正方形，建議 ≤100KB）
img/albums/              專輯封面，檔名對應 ALBUMS 的 cover 欄位
.github/workflows/       GitHub Pages 部署
```

## 怎麼改資料

所有內容都在 `index.html` 的 `<script>` 裡：

- `M`：九位成員（名字、代表色、簡介、物料清單）。`photo` 留空會自動改用插畫頭像。
- `ALBUMS`：歷代專輯與曲目。`yt` 填 YouTube 影片 ID，`lead:1` 標主打歌，`cover` 填 `img/albums/` 內的檔名。
- `KIND`：專輯分類與顏色。篩選按鈕的數量會自動從 `ALBUMS` 算出來。

改完 push 到 `main` 即會自動部署。

## 免責

資料由粉絲整理，最新動態請以 JYP 官方公告為準。
