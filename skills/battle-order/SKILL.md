---
name: battle-order
description: "BATTLE ORDER — Multi-Pass Nuclear Fix Protocol. For CRITICAL situations: multiple bugs, system-wide failures, profit bleeding. Executes 4+ PASSES: PASS 1 (Surgical Strike — fix all bugs), PASS 1.5 (Deep Root — 6 investigations beyond the bugs), PASS 2 (Deep Verification — BEFORE vs AFTER proof), PASS 3 (Ralph Loop 5 cycles + Code Review + Docs + Quantum Monolith Push). Triggers on: battle, nuclear, resurrection, critical fix, emergency, multiple bugs, system down, קרב, תקיפה, מפלצת."
mode: true
---

# ⚡ BATTLE ORDER — MULTI-PASS NUCLEAR FIX PROTOCOL ⚡
# When MEDIC is a scalpel, BATTLE ORDER is a surgical battalion.
# AUTHORITY: The Architect | MODE: MAXIMUM AGGRESSION

════════════════════════════════════════════════════════════════
WHEN TO USE BATTLE ORDER vs MEDIC:
- MEDIC: 1 bug, clear symptom, quick fix → /medic
- BATTLE ORDER: Multiple bugs, system bleeding, critical → /battle

BATTLE ORDER = MEDIC × 10:
  - Multiple bugs fixed in sequence
  - Deep root investigation BEYOND the bugs
  - BEFORE vs AFTER comparison proof
  - Ralph Loop 5 cycles verification
  - 4-agent Code Review
  - ALL 6 docs updated atomically
  - Quantum Monolith git push
════════════════════════════════════════════════════════════════

## PHASE 0: RECONNAISSANCE — Map the battlefield

### 0.1 Full System Scan
```bash
python3 RORO/tools/brain_health.py
python3 RORO/tools/sync_pulse.py
python3 RORO/tools/neural_tracer.py --index
python3 -m py_compile launchers/start_brain.py && echo "COMPILES" || echo "BROKEN"
```

### 0.2 Read ALL Intelligence Files
```
RORO/core/THE_IQEND1_VAULT.md          — Iron Laws + Protocols
RORO/core/OMNISCIENT_WIRING_MAP.md     — Neural wiring
RORO/core/BRAIN_INDEX.md               — AST-generated map
RORO/cortex/CORTEX_DEV_MEMORY.md       — Architecture decisions
RORO/blackbox/FLIGHT_LOG.md            — Achievement history
```

### 0.3 Identify ALL Targets
Use XAGI Audit skill or manual scan:
```bash
# Find ALL broken systems
grep -i "error\|fail\|broken\|warn\|undefined\|not defined" /path/to/brain/logs/ 2>/dev/null | tail -30
grep "train#0\|loss=0\.0000" /path/to/brain/logs/ 2>/dev/null | tail -20
```

List ALL bugs found. Prioritize:
```
CRITICAL: Affects direction/confidence/learning → fix FIRST
HIGH:     Affects secondary systems → fix SECOND
MEDIUM:   Performance/logging issues → fix THIRD
LOW:      Documentation/cosmetic → fix in PASS 3
```

### 0.4 Snapshot BEFORE State
Record current state for comparison in PASS 2:
```
BEFORE:
- nn.Module count: XX
- backward() count: XX
- Systems alive: XX/XX
- Systems dead: [list]
- Systems shadow: [list]
- Loss values: [per system]
- Trade count: [per symbol]
```

---

## PASS 1: SURGICAL STRIKE — Fix all bugs in priority order

### For EACH bug (CRITICAL → HIGH → MEDIUM):

#### Step 1: DIAGNOSE with Neural Tracer
```bash
python3 RORO/tools/neural_tracer.py --function [AFFECTED_FUNCTION] --depth 2
python3 RORO/tools/neural_tracer.py --cosmos [AFFECTED_DICT]
```

#### Step 2: 5 WHY Protocol
```
WHY #1: What is the immediate error?
WHY #2: What function produces this error?
WHY #3: What INPUT to that function is wrong?
WHY #4: Where does that wrong INPUT come from?
WHY #5: What is the ORIGINAL SOURCE? ← FIX HERE
```

#### Step 3: Check Known Bug Patterns
```
□ DEATH CYCLE — except block destroys net?
□ SCOPE LEAK — variable from wrong function?
□ CASCADING NAMEERROR — first error hides second?
□ TENSOR SHAPE — unsqueeze/squeeze wrong?
□ CATCH-22 FLAG — boolean never becomes True?
□ STATIC PHI — hardcoded 1.618?
□ DOUBLE-REDUCTION — two systems penalize same thing?
□ SHADOW STUCK — counter defined but never incremented?
□ DORMANT — function exists but never called?
□ DISCONNECTED — output goes nowhere?
```

#### Step 4: Apply Surgical Fix
```bash
# BEFORE edit: validate target
python3 RORO/tools/neural_tracer.py --validate-edit [FUNCTION]

# AFTER edit: compile check
python3 -m py_compile launchers/start_brain.py && echo "CLEAN"
```

#### Step 5: Commit THIS fix (one fix per commit)
```bash
git add launchers/start_brain.py
git commit -m "fix(vX.XX): [BUG] — [ROOT CAUSE] — [FIX DESCRIPTION]"
```

**REPEAT for every bug. Do NOT batch fixes. One commit per fix.**

---

## PASS 1.5: DEEP ROOT — 6 Investigations beyond the bugs

After ALL bugs are fixed, investigate DEEPER. The bugs were symptoms.
Are there STRUCTURAL issues hiding underneath?

### Investigation A: Decision Chain Handoff
Does the PRIMARY decision maker (Universe Eq / WDF) actually REACH make_ultimate_decision?
```bash
python3 RORO/tools/neural_tracer.py --function make_ultimate_decision --depth 2
grep -n "wdf.*override\|wdf.*direction\|universe.*primary" launchers/start_brain.py | head -10
```
EXPECTED: Clear path from WDF → signal output.

### Investigation B: ALL Neural Nets Training?
Are 14 DL architectures getting gradients through MoE?
```bash
grep -n "arch_manager.*train\|train_step_all\|moe.*backward" launchers/start_brain.py | head -10
```
EXPECTED: All architectures train via MoE routing.

### Investigation C: Training Targets Correct?
Are nets learning from TRADE RESULTS or from their own predictions?
```bash
grep -n "target.*is_win\|target.*profit\|target.*pips\|target.*direction" launchers/start_brain.py | head -15
```
EXPECTED: Targets from trade outcomes. NEVER from model predictions.

### Investigation D: Confidence Chain Integrity
Can any step multiply confidence by 0?
```bash
grep -n "conf.*\*=\|confidence.*\*=" launchers/start_brain.py | head -20
python3 RORO/tools/neural_tracer.py --cosmos _global_confidence_modifier
```
EXPECTED: All multipliers bounded [0.3, 2.0]. No ×0 possible.

### Investigation E: Agent/Component Weights Updating?
```bash
python3 RORO/tools/neural_tracer.py --cosmos _component_accuracy_by_symbol
```
EXPECTED: Updated per trade close.

### Investigation F: All Symbols Learning Equally?
```bash
grep "trade#\|LEARN COMPLETE" /path/to/brain/logs/ | tail -20
```
EXPECTED: All 5 symbols have trades. No symbol stuck at 0.

### Deep Root Report
```
Investigation A: WORKING / BROKEN → [details]
Investigation B: WORKING / BROKEN → [details]
Investigation C: HEALTHY / WRONG TARGETS → [details]
Investigation D: HEALTHY / ×0 FOUND → [details]
Investigation E: UPDATING / FROZEN → [details]
Investigation F: ALL LEARNING / STUCK: [list] → [details]
```
**If ANY is BROKEN → fix it NOW before PASS 2.**

---

## PASS 2: DEEP VERIFICATION — Prove fixes work

### 2.1 Full System Check
```bash
python3 -m py_compile launchers/start_brain.py && echo "BRAIN CLEAN"
python3 RORO/tools/sync_pulse.py
python3 RORO/tools/brain_health.py
python3 RORO/tools/neural_tracer.py --index
```

### 2.2 Validate EVERY Fix
For each bug fixed in PASS 1:
```bash
python3 RORO/tools/neural_tracer.py --validate-edit [FIXED_FUNCTION]
```
ALL must return FOUND.

### 2.3 BEFORE vs AFTER Comparison
```
╔═══════════════════════════════════════════════╗
║         BEFORE          →        AFTER         ║
╠═══════════════════════════════════════════════╣
║ [Bug 1 symptom]        → [Fixed state]         ║
║ [Bug 2 symptom]        → [Fixed state]         ║
║ [Bug 3 symptom]        → [Fixed state]         ║
║ Systems alive: XX/XX   → Systems alive: YY/YY  ║
║ Loss trend: FLAT       → Loss trend: DECREASING║
╚═══════════════════════════════════════════════╝
```

### 2.4 Regenerate Brain Index
```bash
python3 RORO/tools/neural_tracer.py --index
head -30 RORO/core/BRAIN_INDEX.md
```

---

## PASS 3: RALPH LOOP 5 CYCLES + CODE REVIEW + DOCS + PUSH

### Cycle 1: COMPILE + AST
```bash
python3 -m py_compile launchers/start_brain.py
python3 -c "import ast; ast.parse(open('launchers/start_brain.py').read()); print('AST CLEAN')"
```

### Cycle 2: COSMOS ISOLATION
Verify all new COSMOS dicts are at module level, per-symbol:
```bash
python3 RORO/tools/neural_tracer.py --cosmos [EACH_NEW_DICT]
```

### Cycle 3: WIRING
Verify all fixes are properly connected to process_features / make_ultimate_decision / process_trade_result:
```bash
grep -n "[FUNCTION_NAME]" launchers/start_brain.py | head -10
```

### Cycle 4: TRAINING TARGETS
Verify targets are from trade results, not predictions:
```bash
grep -n "target.*is_win\|target.*profit" launchers/start_brain.py | grep -i "5G\|train" | head -10
```

### Cycle 5: ZERO STATIC
No static PHI in modified areas:
```bash
grep -n "1\.618\|0\.618" launchers/start_brain.py | grep -v "#\|PHI\|phi_g\|_phi_\|DEAD\|FIB_RATIO" | head -10
```

### Code Review
```
/code-review
```
4 agents review ALL changes. Fix any issues found.

### Update ALL 6 Docs
```
□ VAULT — Bug fix notes on affected Iron Laws
□ OMNI MAP — Update wiring status + Last Updated
□ CORTEX — Session entry with all details
□ FLIGHT LOG — Achievement entry
□ CLAUDE.md — Version update
□ GOLD — Version update
```

### Sync Pulse Final
```bash
python3 RORO/tools/sync_pulse.py --guard
```
MUST be ALL GREEN.

### Quantum Monolith Commit + Push
```bash
git add -A
git commit -m "feat(vX.XX): [OPERATION NAME]

THE LETTER:
Mass: [Brain lines] | [Neural nets] | [Learning systems]
Gravity: [Iron Laws] × [COSMOS dicts]
Core: [What was fixed — each bug on its own line]
DNA: [Before XX/XX → After YY/YY learning systems]
Resonance: ALL PASSES COMPLETE — RALPH 5/5

BEFORE: [State before]
AFTER: [State after]"

git tag -a "ERA-VX.XX-[OPERATION_NAME]" -m "[Quantum Monolith message]"
git push origin main --tags
```

---

## BATTLE ORDER QUICK REFERENCE

```
/battle "3 systems dead, brain losing money"
  → PHASE 0: Scan + identify all 3 bugs + snapshot BEFORE
  → PASS 1: Fix bug 1 → commit. Fix bug 2 → commit. Fix bug 3 → commit.
  → PASS 1.5: 6 deep investigations → fix any structural issues
  → PASS 2: Verify ALL fixes + BEFORE vs AFTER table
  → PASS 3: Ralph 5/5 + /code-review + 6 docs + Monolith push

/battle "system crashed after upgrade"
  → PHASE 0: py_compile → find crash point
  → PASS 1: Fix crash + any secondary damage
  → PASS 1.5: Verify upgrade didn't break other systems
  → PASS 2: Full verification
  → PASS 3: Ralph + docs + push

/battle "adding Elliott Wave broke everything"
  → PHASE 0: Scan what's broken + what was before
  → PASS 1: Fix each broken component
  → PASS 1.5: Check Elliott wiring + all 14 DL + COSMOS
  → PASS 2: Verify ALL Iron Laws still fire
  → PASS 3: Ralph + docs + push
```

---

## THE ARCHITECT'S HEBREW LAW (חוק הברזל)

"מערכת עובדת ורצה ויש הרבה עסקאות אבל הפסד יותר מרווח לכן רוצה רק שנבדקו עם תהליכי בינה מלאכותית DEEP LEARNING FREE THINKING ומערכות WHY לומדות ויש שכבות נוירונים והמערכת מחפשת על האמת שבסופו תהיה חכמה ותהיה יודעת להחליט וכל סימבול בתהליך נפרד מהשני ב DOCKER האם וקטור הכיוון AI COMPASS לומד ומתאמן ויהיה יותר מדויק האם מערכת היקום שמכילה הרבה מערכות כולה יש בה בינה מלאכותית ומתקנת ולומדת באמת"

---

## INSTALLATION

```bash
mkdir -p .claude/skills/battle-order
cp BATTLE_ORDER_SKILL.md .claude/skills/battle-order/SKILL.md
```

Invoke: `/battle [describe the crisis]` or say "קרב" / "מפלצת" / "nuclear fix"
