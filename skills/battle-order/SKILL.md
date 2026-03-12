---
name: battle-order
description: "BATTLE ORDER — Multi-Pass Nuclear Fix Protocol. For CRITICAL situations: multiple bugs, system-wide failures, profit bleeding. Executes 4+ PASSES: PASS 1 (Surgical Strike — fix all bugs), PASS 1.5 (Deep Root — 6 investigations beyond the bugs), PASS 2 (Deep Verification — BEFORE vs AFTER proof), PASS 3 (Ralph Loop 5 cycles + Code Review + Docs + Quantum Monolith Push). Triggers on: battle, nuclear, resurrection, critical fix, emergency, multiple bugs, system down, קרב, תקיפה, מפלצת."
mode: true
---

# ⚡ BATTLE ORDER — MULTI-PASS NUCLEAR FIX PROTOCOL ⚡
# When MEDIC is a scalpel, BATTLE ORDER is a surgical battalion.
# AUTHORITY: The Architect | MODE: MAXIMUM AGGRESSION
# SYSTEM: RAZI AGI | INTRADAY ONLY | M5 data → M30 execution → H4 confirmation

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

### Investigation G: Elliott Wave Taxonomy Complete?
```bash
# 23 labels, 12 forms, 8 heads — all present?
grep -c "IMP_W\|DIAG_\|CORR_\|TRI_\|CMPLX_" launchers/start_brain.py
grep -c "FORM_IMPULSE\|FORM_LEADING\|FORM_ENDING\|FORM_ZIGZAG\|FORM_FLAT\|FORM_TRIANGLE" launchers/start_brain.py
# Cross-TF matrix active?
grep -n "cross_tf_matrix\|_build_cross_tf" launchers/start_brain.py | head -5
# Wave drawer pipeline?
grep -n "WAVE_DRAW\|WAVE_CORRECT" launchers/start_brain.py | head -5
```
EXPECTED: 23+ labels, 12 forms, cross-TF matrix, wave drawer.

### Investigation H: Protocol Conflicts — Zero Contradictions!
```bash
# Early exit vs HOLD — do they conflict?
grep -n "early_exit\|protect_profit\|trailing" launchers/start_brain.py | head -10
grep -n "HOLD\|BLOCKED\|CONF_GATE" launchers/start_brain.py | head -10

# Commission handling — not phantom profits?
grep -n "commission\|spread\|slippage" launchers/start_brain.py | head -10

# Direction alignment — all pointing same way?
grep -n "wdf.*direction\|universe.*direction\|compass.*direction\|elliott.*direction" launchers/start_brain.py | head -10

# No double penalties
grep -n "confidence.*\*=.*0\.\|confidence.*-=" launchers/start_brain.py | head -20
```
EXPECTED: Early exit active, commissions included, directions aligned, no stacking.

### Investigation I: Feynman Path Integral — God's Card Active?
```bash
# Does ElliottGRU output PROBABILITY DISTRIBUTION (softmax 23)?
grep -n "softmax.*23\|wave_probabilities\|path_integral" launchers/start_brain.py | head -10

# Is there a certainty gate? P(first) - P(second) > threshold?
grep -n "certainty\|prob_gap\|first.*second\|wave_certainty" launchers/start_brain.py | head -10

# Does self-correction happen automatically (no forced recount)?
grep -n "recount\|force_count\|manual.*count" launchers/start_brain.py | head -10
```
EXPECTED: Full softmax over 23. Certainty gate active. No forced recounts.
THE KEY: If system outputs argmax without certainty check → it's GAMBLING, not TRADING.

### Deep Root Report
```
Investigation A: WORKING / BROKEN → [details]
Investigation B: WORKING / BROKEN → [details]
Investigation C: HEALTHY / WRONG TARGETS → [details]
Investigation D: HEALTHY / ×0 FOUND → [details]
Investigation E: UPDATING / FROZEN → [details]
Investigation F: ALL LEARNING / STUCK: [list] → [details]
Investigation G: TAXONOMY COMPLETE / INCOMPLETE → [details]
Investigation H: ZERO CONFLICTS / [list of conflicts] → [details]
Investigation I: FEYNMAN ACTIVE (probability+certainty) / SINGLE-COUNT (gambling!) → [details]
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

## ADDING NEW IRON LAW — 11-STEP MILITARY CHECKLIST

When BATTLE ORDER includes adding a new Iron Law (IL#196+), follow EVERY step:

```
STEP 1:  CLASS — nn.Module with layers + LayerNorm + Dropout(0.1)
STEP 2:  COSMOS — 5 dicts at module level: net, optimizer, shadow, result, accuracy
STEP 3:  FACTORY — _get_or_create_xxx(symbol) with Adam(lr=0.001, weight_decay=0.001)
STEP 4:  FEATURES — Extract from enriched_features (ZERO price thresholds! Energy only!)
STEP 5:  PROCESS — Called from process_features(). torch.no_grad(). Returns dict with WHY.
STEP 6:  TRAIN — Called from process_trade_result(). backward + clip_grad_norm_(1.0) + step
STEP 7:  WIRE ×3 — Insert into: process_features + make_ultimate_decision + process_trade_result
STEP 8:  V45 SAVE — Add to save_weights: state_dict + optimizer + shadow counter
STEP 9:  V45 LOAD — SYMMETRIC to save! load_state_dict + restore shadow
STEP 10: REGISTRY — Add to registry list + update DNA chain count
STEP 11: DOCS ×6 — CLAUDE.md + VAULT + OMNI + FLIGHT + CORTEX + GOLD

**ELLIOTT WAVE EXPANSION (if IL touches Elliott):**
```
STEP E1: Expand wave labels if new pattern discovered (23 → 24+)
STEP E2: Update Energy Signature Matrix (32D vector for new form)
STEP E3: Add cross-TF correlation rule for new wave type
STEP E4: Update Wave Drawer color/style table for new label
STEP E5: Add Human-in-the-Loop training case for new pattern
STEP E6: Verify backward compatibility (23→9 group mapping still works)
STEP E7: Update ELLIOTT_WAVE_UNIVERSE_ENCYCLOPEDIA_V2.md
```

**PROTOCOL CONFLICT CHECK (mandatory for ALL new Iron Laws):**
```
CHECK P1: Does this IL conflict with any existing IL? (grep for same vars)
CHECK P2: Does this IL affect confidence? If yes — bounds check [0.3, 2.0]
CHECK P3: Does this IL affect direction? If yes — must align with IL#158
CHECK P4: Does this IL affect SL/TP? If yes — STEEL protection check
CHECK P5: Does this IL affect INTRADAY pipeline? M5→M30→H4 must stay sacred
CHECK P6: Are commissions/spread considered in any profit calculations?
CHECK P7: Does this IL respect Feynman Path Integral? Wave outputs must be
          PROBABILITY DISTRIBUTIONS (softmax), never single argmax without
          certainty gate. If certainty < φ_g_inverse → system must WAIT.
```
```

**V45 SAVE/LOAD SYMMETRY — The Invisible Killer:**
If save has 5 fields but load reads 4 → one field LOST on restart.
If load expects a field that save doesn't write → crash on restart.
```bash
# Verify symmetry after adding new system:
grep "weights\[.il${NEW_IL}" launchers/start_brain.py | wc -l  # save count
grep "weights.get(.il${NEW_IL}\|_ll_${NEW_IL}" launchers/start_brain.py | wc -l  # load count
# MUST be equal!
```

---

## BRAIN ANATOMY — Current Vital Signs

```
INTRADAY SYSTEM: M5 data collection → M30 trade execution → H4 trend confirmation
Brain:           launchers/start_brain.py (~35,400 lines)
Classes:         38 nn.Module subclasses
Functions:       445+
Iron Laws:       195 (IL#1-195) + 3 Master Laws + 1 reserved = 199 DNA
COSMOS Dicts:    134 (_*_by_symbol per-symbol isolation)
Learning:        27 systems (all BPTT on every trade close)
DL Architectures: 14 (TransformerXL, KAN, Mamba, GNN, RWKV, etc.)
AI Agents:       11 (soft modifiers ±3-5%)
Protocols:       48 (P1-P48)
Symbols:         5 (XAUUSD#, NAS100#, US30#, GBPUSD#, EURUSD#)
```

**3 MOST CRITICAL FUNCTIONS — breaking these kills the organism:**
```
process_features()         → Steps 1-8.5 → enriched_features
make_ultimate_decision()   → IL#158 PRIMARY → signal
process_trade_result()     → 27 learning system updates
```

---

## XAGI MANIFESTO — 6 Laws of the Living Organism

Every BATTLE ORDER fix must satisfy ALL 6:
```
LAW 1: NO ZEROS     — Data always flows. Epsilon guards everywhere.
LAW 2: EVERY = AI   — WHY dict on every decision function.
LAW 3: SELF-CORRECT — BPTT fires on every trade close for ALL 27 systems.
LAW 4: NO DICTATORS — IL#158 PRIMARY, everything else modulates ±3-6%.
LAW 5: DEATH STATIC — No hardcoded 1.618/0.618 in decisions. PHI_GRAVITY dynamic.
LAW 6: XAGI ARMOR   — Intelligence IS the shield. No external safety overrides.
LAW 7: FEYNMAN PATH — The wave is ALL labels simultaneously. Output probabilities,
       not single answers. Trade ONLY when the universe has decided (certainty > φ_inv).
       Self-correction is natural — probabilities shift every bar.
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
