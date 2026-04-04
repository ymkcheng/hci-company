# HCI Product Company — Gemini CLI Extension

一間頂尖 HCI 產品公司的模擬。給它一個問題，看六個 AI 部門自動協作、交付、退回、迭代，最終產出一個以人為本的互動體驗原型。

## Quick Start

```bash
# 安裝
gemini extensions install https://github.com/你的帳號/hci-company

# 啟動
gemini
/hci-company:hci-company 大學生期中考前焦慮到睡不著
```

然後雙手離開鍵盤。看 Victor 帶著他的團隊工作。

## The Team

| Name | Role | What They Do |
|---|---|---|
| **Victor** | CEO / Orchestrator | 不動手，只判斷。決定放行還是打回。 |
| **Maya** | User Researcher | 觀察使用者，挖掘隱藏需求。 |
| **Simon** | Product Strategist | 做最難的決定：做什麼、不做什麼。 |
| **Aria** | Interaction Designer | 設計人與產品之間的每個接觸點。 |
| **Leo** | Frontend Engineer | 把設計變成可以跑的原型。 |
| **Scout** | Usability Tester | 用使用者的眼睛找到所有人的盲點。 |

## How It Works

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
  ↓ 發現問題？→ 打回對應部門重做
Victor 彙整最終報告交給你
```

## What Students Learn by Reverse-Engineering This

每個 agent 的 `.md` 檔案裡的 `goal` 和 `constraints`，就是 HCI 的核心原則：

- Maya: 「禁止用假設代替事實」= 使用者研究的根本
- Simon: 「一次只解決一個核心問題」= 設計聚焦
- Aria: 「每個畫面最多一個主要動作」= Hick's Law
- Leo: 「禁止為技術方便而改設計」= 技術為人服務
- Scout: 「用真實使用者的眼睛看」= 使用者中心設計

## File Structure

```
hci-company/
├── gemini-extension.json       # Extension 設定
├── GEMINI.md                   # Victor（CEO orchestrator）
├── README.md                   # 你正在讀的這份
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
    └── handoff-and-rejection.md # 交付與打回規則
```

## Requirements

- Gemini CLI v0.35.0+
- Subagents enabled: `"experimental": {"enableAgents": true}` in settings.json
- Google account (free tier: 1,000 requests/day)

## For the Course: I4030 Advanced HCI

This extension is designed for Week 6 of I4030 (Spring 2026) at Tatung University.
Students observe the company running, then reverse-engineer the agent files to understand how HCI principles are encoded into AI systems.

**AI is the new UI** — the interface is no longer buttons and menus. It's the rules you write for how AI agents think, judge, and collaborate.

## License

MIT — 自由使用、修改、分享。
