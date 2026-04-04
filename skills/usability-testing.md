# Usability Testing Methodology

## When This Skill Activates
When Scout (hci-usability-tester) needs structured evaluation methods.

## Three-Persona Walkthrough

For each persona (Novice, Target User, Impatient User), walk through EVERY step in the user journey:

### At Each Step, Record:
1. **Can they find the action?** (Discoverability) — Is the next step obvious without reading instructions?
2. **Can they perform the action?** (Operability) — Is the tap target large enough? Is the gesture natural?
3. **Do they know it worked?** (Feedback) — Does the system respond clearly and quickly?
4. **Do they know what to do next?** (Wayfinding) — Is the path forward clear?
5. **How do they feel?** (Emotion) — Confident? Confused? Delighted? Frustrated?

### Red Flags (Automatic Critical Rating)
- User cannot complete the core task at all
- User performs action but nothing visible happens
- User gets stuck in a loop with no exit
- User data is lost without warning
- Core functionality does not work on mobile

### Yellow Flags (Automatic Major Rating)
- User hesitates more than 5 seconds before acting
- User taps the wrong element first
- Error message does not explain how to fix
- User completes task but expresses frustration
- Important information requires scrolling to discover

## Severity Classification

| Severity | Impact | Frequency | Priority |
|---|---|---|---|
| 🔴 Critical | Cannot complete core task | Any user | Fix before ship |
| 🟡 Major | Completes with significant difficulty | Most users | Fix in this iteration |
| 🟢 Minor | Small friction, completes easily | Some users | Fix when possible |
| ⭐ Strength | Positive experience | — | Preserve and amplify |

## Root Cause Attribution

Every finding must trace to a department:

| Symptom | Likely Root Cause |
|---|---|
| User doesn't understand what the product is for | Strategy (Simon) — unclear value proposition |
| User can't find the main action | Design (Aria) — visual hierarchy problem |
| Button doesn't respond | Engineering (Leo) — implementation bug |
| Feature exists that contradicts the brief | Design (Aria) or Engineering (Leo) — scope creep |
| Product works but doesn't feel right | Design (Aria) — emotional arc misaligned |
| Product solves wrong problem | Strategy (Simon) or Research (Maya) — wrong insight |

## Quality Checklist
- [ ] All three personas tested across full journey
- [ ] Every finding has a severity, root cause department, and recommended fix
- [ ] At least one Strength is documented
- [ ] Spec compliance is checked point by point
- [ ] Success Definition is explicitly verified (Before → After state change)
