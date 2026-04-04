# HCI Product Company — Gemini CLI Extension

一間頂尖 HCI 產品公司的模擬。給它一個問題，六個 AI 部門自動協作、交付、退回、迭代，最終產出一個以人為本的互動體驗原型。

## 快速開始

```bash
# 安裝（需要先啟用 subagents）
# 在 ~/.gemini/settings.json 中加入：
# { "experimental": { "enableAgents": true } }

# 從 GitHub 安裝
gemini extensions install https://github.com/你的帳號/hci-company

# 啟動
gemini
/hci-company:hci-company 大學生期中考前焦慮到睡不著
```

然後雙手離開鍵盤。看 Victor 帶著團隊工作。

## 團隊成員

| 名字 | 部門 | 做什麼 |
|---|---|---|
| **Victor** | 執行長 / 協調者 | 不動手，只判斷。決定放行還是退回。 |
| **Maya** | 使用者研究部 | 觀察使用者，挖掘隱藏需求。 |
| **Simon** | 產品策略部 | 做最難的決定：做什麼、不做什麼。 |
| **Aria** | 互動設計部 | 設計人與產品之間的每個接觸點。 |
| **Leo** | 工程開發部 | 把設計變成可以跑的原型。 |
| **Scout** | 品質驗證部 | 用使用者的眼睛找到所有人的盲點。 |

## 運作方式

```
你（老闆）說出一個問題
  ↓
Victor 派 Maya 去研究使用者
  ↓ Victor 審查：夠不夠深？
Simon 做出策略判斷（做什麼、不做什麼）
  ↓ Victor 審查：夠不夠聚焦？
Aria 設計互動流程
  ↓ Victor 審查：每個畫面只有一個主要動作嗎？
Leo 寫出可以跑的原型
  ↓ Victor 審查：符合規格嗎？
Scout 做使用性測試
  ↓ 發現問題？→ 退回對應部門重做
Victor 彙整最終報告交給你
```

## 逆向工程這間公司能學到什麼

每個 agent 的 `.md` 檔案裡的目標和限制，就是 HCI 的核心原則：

- **Maya**：「禁止用假設代替事實」= 使用者研究的根本
- **Simon**：「一次只解決一個核心問題」= 設計聚焦
- **Aria**：「每個畫面最多一個主要動作」= Hick's Law
- **Leo**：「禁止為技術方便而改設計」= 技術為人服務
- **Scout**：「用真實使用者的眼睛看」= 使用者中心設計

## 檔案結構

```
hci-company/
├── gemini-extension.json       # Extension 設定
├── GEMINI.md                   # Victor（執行長）
├── README.md                   # 這份文件
├── agents/
│   ├── hci-researcher.md       # Maya
│   ├── hci-strategist.md       # Simon
│   ├── hci-interaction-designer.md  # Aria
│   ├── hci-engineer.md         # Leo
│   └── hci-usability-tester.md # Scout
├── skills/
│   ├── user-research.md        # 使用者研究方法論
│   ├── design-brief.md         # 設計判斷書方法
│   ├── interaction-design.md   # 互動設計原則
│   └── usability-testing.md    # 使用性測試流程
├── commands/
│   └── hci-company.toml        # /hci-company:hci-company 啟動指令
└── protocols/
    └── handoff-and-rejection.md # 交付與退回規則
```

## 系統需求

- Gemini CLI v0.35.0 以上
- 啟用 subagents：`settings.json` 中設定 `"experimental": {"enableAgents": true}`
- Google 帳號（免費方案：每天 1,000 次請求）

## 課程用途：I4030 進階人機互動

本 extension 為大同大學 I4030（2026 春季）第六週設計。
學生觀察公司運轉，然後逆向工程 agent 檔案，理解 HCI 原則如何被編碼進 AI 系統。

**AI is the new UI** — 介面不再是按鈕和選單。而是你為 AI agent 寫下的思考、判斷和協作規則。

## License

MIT
