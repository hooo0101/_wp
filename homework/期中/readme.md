# NoteAI — AI 智慧筆記平台

> 網頁程式設計期中作業 | 2026/06/14

一個結合 **Node.js REST API** 與 **Claude AI** 的全端筆記應用，讓你邊記筆記，邊用 AI 輔助學習。

## 功能

- 📝 **筆記管理** — 新增、編輯、刪除、搜尋（支援標籤）
- 🤖 **AI 聊天助理** — 整合 Claude API，可針對目前筆記提問
- 💾 **離線備援** — Server 離線時自動切換 localStorage
- ⌨️ **快捷鍵** — Ctrl+S 快速儲存

## 快速開始

```bash
npm install
export ANTHROPIC_API_KEY="你的金鑰"   # 選填，無 key 仍可使用筆記功能
npm start
# 開啟 http://localhost:3000
```

## 技術架構

| 層 | 技術 |
|----|------|
| 後端 | Node.js + Express |
| 前端 | 原生 HTML/CSS/JavaScript |
| 儲存 | JSON 檔案 + localStorage 備援 |
| AI | Anthropic Claude API |

## 專案結構

```
├── server/server.js     # REST API (GET/POST/PUT/DELETE /api/notes)
├── public/index.html    # 前端單頁應用
├── docs/
│   ├── report.md        # 專案報告
│   └── learning-notes.md # 學習筆記
└── package.json
```

## API 文件

| 方法 | 路徑 | 說明 |
|------|------|------|
| GET | /api/notes | 取得所有筆記 |
| POST | /api/notes | 新增筆記 |
| PUT | /api/notes/:id | 更新筆記 |
| DELETE | /api/notes/:id | 刪除筆記 |
| POST | /api/chat | AI 對話（轉發至 Claude API）|