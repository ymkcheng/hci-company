# Interaction Design Principles

## When This Skill Activates
When Aria (hci-interaction-designer) needs design pattern guidance.

## Core Heuristics (adapted from Nielsen & Shneiderman)

1. **Visibility of system status**: The user always knows where they are, what is happening, and what to do next.
2. **Match between system and real world**: Use language and concepts the user already knows. No jargon.
3. **User control and freedom**: Always provide an exit. Undo is better than confirmation dialogs.
4. **Consistency**: Same action → same result. Everywhere. Every time.
5. **Error prevention**: Make it hard to do the wrong thing. Make it easy to recover.
6. **Recognition over recall**: Show options instead of requiring memory.
7. **Flexibility**: Support both novice (guided) and expert (shortcut) paths.
8. **Aesthetic and minimalist design**: Every element earns its place. If it doesn't serve the user's current task, remove it.

## Feedback Design Matrix

| User Action | Immediate (<100ms) | Progress (100ms-5s) | Completion | Error |
|---|---|---|---|---|
| Tap button | Color/scale change | Spinner or progress | Success state | Shake + message |
| Swipe | Element follows finger | Momentum animation | Snap to position | Rubber band back |
| Submit form | Button disabled + loading | Progress indicator | Confirmation screen | Inline field errors |
| Wait (system processing) | — | Skeleton screen or pulse | Content appears | Retry option |

## Emotional Arc Template
```
Entry → Curiosity ("what is this?")
  → Confidence ("I know what to do")
    → Flow ("this feels natural")
      → Accomplishment ("I did it")
        → Closure ("I can leave feeling good")
```

## Quality Checklist
- [ ] Every screen has exactly one primary action
- [ ] Feedback exists for every user action (no silent failures)
- [ ] Error states guide toward resolution, not just report problems
- [ ] The emotional arc aligns with the Design Brief's success definition
- [ ] Edge cases are handled gracefully, not ignored
