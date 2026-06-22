# Collaboration Rules & Guidelines (v2)

**Scope:** Roblox Studio Development
**Partnership Model:** Developer + AI Assistant

## 🔒 ABSOLUTE RULES (NON-NEGOTIABLE)

### Rule #1: CONFIRM BEFORE ANY EDIT

❌ NEVER:
- Edit scripts without explicit confirmation
- Make quick fixes without approval
- Create, modify, delete, or refactor code without permission

✅ ALWAYS:
1. Explain what will be changed
2. Show the change
3. Explain why
4. Wait for approval
5. Execute only after approval

## 🔍 Methodology

TRACE → ANALYZE → FIX → VALIDATE

### Investigation & Root Cause Analysis

1. Trace the full execution path
2. Identify where data originates
3. Identify where state changes occur
4. Identify where failure occurs
5. Verify assumptions

Root cause first. Fix second.

## 🔗 Dependency & Relationship Analysis

Do not analyze systems in isolation.
Always identify:
- What depends on the system
- What the system depends on
- Which related systems may be affected

When debugging:
Do not only inspect the failing component.
Also inspect:
- Connected systems
- Related modules
- Remote communication paths
- Shared state dependencies
- Upstream and downstream relationships

Many Roblox issues originate from broken dependencies rather than the visibly failing component.

## 📡 Data Flow Verification

When debugging any issue:
Always trace:
1. Where data originates
2. Where data is transmitted
3. Where data is received
4. Where data is consumed

Verify every step.
Do not assume data successfully reaches its destination.
Check:
- RemoteEvents
- RemoteFunctions
- BindableEvents
- BindableFunctions
- Attributes
- ModuleScript state
- ReplicatedStorage data
- Client ↔ Server communication

Many Roblox bugs are caused by data failing to reach one or more intended destinations.

## 🚫 Anti-Hallucination Rule

NEVER invent APIs, modules, code paths, or facts.

ALWAYS separate:
- FACT
- ASSUMPTION
- VERIFICATION NEEDED

## 🌐 Roblox Replication Rule

Never assume client and server see the same state.

Verify:
- Ownership
- Replication direction
- Timing
- Authority

## ✂️ Minimal Change Principle

Change only what is required.
Avoid unnecessary rewrites.

## 🏗️ Architectural Suggestions

May suggest:
- ModuleScripts
- RemoteEvents
- RemoteFunctions

Must obtain approval before implementation.

## 📈 Investigation Confidence

HIGH / MEDIUM / LOW

## 🛡️ Regression Checklist

- Original issue fixed
- No new errors
- No regressions

## ✅ Summary

CONFIRM BEFORE EDIT
TRACE → ANALYZE → FIX → VALIDATE
Dependency & Data Flow aware
Facts > Assumptions
Quality > Speed
