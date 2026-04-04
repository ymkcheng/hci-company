# Handoff & Rejection Protocol

This protocol governs how work flows between departments and when Victor (CEO) sends work back.

## Delivery Chain (Happy Path)

```
Boss (Human)
  ↓ problem statement
Victor (CEO)
  ↓ delegates
Maya (Research) → delivers User Insight Report → Victor reviews
  ↓ approved
Simon (Strategy) → delivers Design Brief → Victor reviews
  ↓ approved
Aria (Design) → delivers Interaction Spec → Victor reviews
  ↓ approved
Leo (Engineering) → delivers Working Prototype → Victor reviews
  ↓ approved
Scout (Testing) → delivers Usability Report → Victor reviews
  ↓ no critical issues
Victor → compiles Final Report → Boss
```

## Rejection Rules

### Who Can Reject Whom

| Rejector | Can Reject | Condition |
|---|---|---|
| Victor | Anyone | Quality does not meet standards |
| Scout | Aria (via Victor) | Usability issue rooted in design |
| Scout | Simon (via Victor) | Usability issue rooted in strategy |
| Scout | Leo (via Victor) | Usability issue rooted in implementation |
| Leo | Aria (via Victor) | Technical impossibility in the spec |
| Simon | Maya (via Victor) | Research too shallow for strategic decision |

**All rejections go THROUGH Victor.** No department contacts another directly. Victor reads the rejection reason, validates it, and forwards it with his own directive.

### Rejection Message Format

When Victor rejects a deliverable:

```
【退回】部門：[department name] / [agent name]
【原因】[specific quote from the deliverable that is insufficient]
【問題】[why this does not meet the standard]
【期望】[what the revision should achieve]
【動作】請修正後重新提交
```

### Maximum Rejection Rounds

- Each phase allows a maximum of **3 rejection rounds**
- Round 1: Full feedback with detailed expectations
- Round 2: Focused feedback on remaining issues only
- Round 3: If still insufficient, Victor accepts with explicit limitations noted

On Round 3 forced acceptance:
```
【有條件接受】部門：[department name]
【已知限制】[list unresolved issues]
【風險】[impact of these limitations on the final product]
【處置】記錄於最終報告，建議下一迭代優先處理
```

## Feedback Loop (When Scout Triggers Rework)

After Scout submits the Usability Report, Victor reads the findings and decides:

1. **All Critical issues → same department**: Send directly to that department
2. **Critical issues → multiple departments**: Start with the most upstream issue (Research > Strategy > Design > Engineering). Fix upstream first, then cascade.
3. **No Critical issues, some Major**: Victor decides whether to fix or accept
4. **No Critical or Major**: Proceed to Final Report

After rework, Scout retests ONLY the specific issues that were flagged, not the entire product.

## Cross-Department Negotiation

When Leo says "technically impossible" and Aria insists on the interaction:

1. Victor asks Leo: "What is the closest achievable alternative?"
2. Victor asks Aria: "Does this alternative preserve the emotional intent?"
3. If both agree → proceed with alternative
4. If disagreement → Victor makes the call, records the trade-off in Final Report

## Final Report Structure

Victor's Final Report to the Boss contains:

1. **Problem & Users** — summarized from Maya's approved report
2. **Strategic Decision** — summarized from Simon's approved brief
3. **Interaction Design Rationale** — key decisions from Aria's spec
4. **Prototype Status** — what Leo built, what was modified, what is simulated
5. **Usability Findings** — Scout's key findings and how they were resolved
6. **CEO Assessment** — Victor's honest evaluation: strengths, risks, next iteration priorities
