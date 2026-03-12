---
name: medic
description: "MEDIC — Intelligent Bug Healer. Finds bugs, understands WHY they happened, fixes them surgically, verifies the fix, and prevents recurrence. Unlike basic recovery tools, MEDIC traces the FULL neural pathway to find ROOT CAUSE before touching code. Uses CONNECTOME tools (Neural Tracer + Sync Pulse) with built-in FEEDBACK LOOP. Triggers on: medic, fix, bug, crash, error, broken, not working, שבור, תתקן, באג, תרפא, heal, repair, resurrection."
mode: true
---

# 🏥 MEDIC — INTELLIGENT BUG HEALER
# Not recovery. Not debugging. HEALING from the root.
# AUTHORITY: The Architect | LOOP: DIAGNOSE → TRACE → FIX → VERIFY → LEARN
# SYSTEM: RAZI AGI | MODE: INTRADAY ONLY | PIPELINE: M5 data → M30 execution → H4 confirmation

════════════════════════════════════════════════════════════════
MEDIC PROTOCOL: "A surgeon who understands the ORGANISM, not just the wound."
- Recover My Code = bandaid (restores old version)
- Standard Debug = flashlight (finds the line)
- MEDIC = fMRI + surgery + post-op + vaccine (heals + prevents)

INTRADAY DECLARATION:
This system trades INTRADAY ONLY. M5 collects data. M30 executes.
H4 confirms trend. This pipeline is SACRED and NEVER modified.
════════════════════════════════════════════════════════════════

## THE 12 SACRED RULES OF BRAIN SURGERY

Before ANY fix, internalize these rules. Violating ANY = patient death.

```
RULE 1:  SURGICAL ONLY — str_replace, never rewrite from scratch
RULE 2:  STEEL PROTECTION — SL/TP ranges, lot sizes, max_positions,
         max_drawdown are NEVER modified. If fix touches these → STOP.
RULE 3:  PHI IS DYNAMIC — Never write 1.618 or 0.618 as literal.
         Always: phi_g = _get_phi_field(symbol)
RULE 4:  COSMOS ISOLATION — Every per-symbol state = _*_by_symbol dict
         at module level. Zero cross-contamination between symbols.
RULE 5:  float64 ALWAYS FOR MONEY — float(np.float64(price)), never float32
RULE 6:  SHADOW MODE — Every new system starts in shadow (21 trades).
         Predicts but does NOT affect decisions until graduated.
RULE 7:  NO DEAD CODE — No pass in except, no orphan functions,
         no COSMOS dicts with 0 readers, every net needs factory+forward+train+V45
RULE 8:  UNIVERSE EQUATION IS PRIMARY — IL#158 decides direction.
         Everything else modulates ±3-6%. Nothing overrides except STEEL.
RULE 9:  THE WHY ENGINE — Every decision outputs a WHY dict explaining itself
RULE 10: M5→M30→H4 SACRED PIPELINE — INTRADAY. Never modified.
RULE 11: GRADIENT SAFETY — clip_grad_norm_(1.0) on ALL nets.
         GRU: net.hidden = net.hidden.detach() before training.
RULE 12: DNA CHAIN — After any change, DNA count = IL# + 3 Master + 1 reserved
RULE 13: ELLIOTT TAXONOMY — 23 wave labels + 12 forms + 8 GRU heads.
         Wave 3 ≠ Wave C despite same energy! CONTEXT from H4 decides.
         12,376 possible wave structures — AI evaluates ALL simultaneously.
RULE 14: NO PROTOCOL CONFLICTS — Before any fix, verify:
         - No two systems penalize the same signal (double-reduction)
         - Early exit protects profit (trailing SL moves to breakeven)
         - Commissions included in profit calculations (not phantom!)
         - Direction: Universe Eq + WDF + Compass + Elliott must AGREE
         - INTRADAY ONLY: M5 data, M30 execute, H4 confirm
RULE 15: FEYNMAN PATH INTEGRAL (GOD'S CARD) — The wave is NOT one label.
         The wave is ALL labels simultaneously until energy decides.
         ElliottGRU outputs PROBABILITY DISTRIBUTION (softmax 23).
         Certainty = P(first) - P(second).
         If certainty < φ_g_inverse → DO NOT TRADE. Universe undecided.
         Self-correction is AUTOMATIC (probabilities shift per bar).
         NEVER force a single wave count. Let probabilities flow.
```

## PHASE 1: TRIAGE — What hurts?

### 1.1 Emergency Scan
```bash
python3 RORO/tools/brain_health.py
python3 -m py_compile launchers/start_brain.py && echo "COMPILES" || echo "BROKEN"
```

### 1.2 Read The Pain
The Architect described a problem. Parse the EXACT symptoms:
- Is the brain CRASHING? (py_compile fails / RuntimeError)
- Is the brain RUNNING but WRONG? (losing money / wrong direction / stuck)
- Is the brain SILENT? (no trades / no signals / HOLD forever)
- Is documentation STALE? (sync_pulse CRITICAL)

### 1.3 Classify Severity
```
CRITICAL: Brain won't start / crashes on every tick → PHASE 2 IMMEDIATELY
HIGH:     Brain runs but learning is dead (train#0, loss=0) → PHASE 2
MEDIUM:   Brain runs, learns, but losing money → PHASE 3 (deep investigation)
LOW:      Documentation desync / cosmetic → PHASE 4 (quick fix)
```

---

## PHASE 2: DIAGNOSE — Trace the neural pathway BEFORE touching code

### 2.1 Load Consciousness
```bash
python3 RORO/tools/neural_tracer.py --index
```
Read: BRAIN_INDEX.md, VAULT, OMNI MAP. Know the FULL organism.

### 2.2 Trace the Symptom to Root Cause
**NEVER fix the symptom. ALWAYS fix the ROOT.**

Example: "confidence is 0" is a SYMPTOM.
ROOT might be: PULSE fusion dead → OMEGA proof too aggressive → PHI resonance decay → XAGI Guardian not rescuing.

```bash
# If symptom is in a specific function:
python3 RORO/tools/neural_tracer.py --function [SYMPTOM_FUNCTION] --depth 3

# If symptom is a COSMOS dict with wrong value:
python3 RORO/tools/neural_tracer.py --cosmos [DICT_NAME]

# If symptom is an Iron Law not firing:
python3 RORO/tools/neural_tracer.py --il [NUMBER]
```

### 2.3 The 5 WHY Protocol
Before ANY fix, ask 5 times:
```
WHY #1: What is the immediate error?
WHY #2: What function produces this error?
WHY #3: What INPUT to that function is wrong?
WHY #4: Where does that wrong INPUT come from?
WHY #5: What is the ORIGINAL SOURCE of the wrong data?
```
The answer to WHY #5 is the ROOT CAUSE. Fix THERE, not at WHY #1.

### 2.4 Check for Known Bug Patterns
Before writing new code, check if this is a KNOWN pattern:
```
PATTERN: DEATH CYCLE — except block destroys net → infinite recreation
CHECK: grep -A5 "except.*Exception" in the affected function

PATTERN: SCOPE LEAK — variable from wrong function scope
CHECK: Is the variable defined in THIS function or imported from another?

PATTERN: CASCADING NAMEERROR — first error hides second error
CHECK: After fixing one error, are there MORE errors in same block?

PATTERN: TENSOR SHAPE MISMATCH — unsqueeze/squeeze wrong dimensions
CHECK: Print tensor shapes before and after the failing line

PATTERN: CATCH-22 FLAG — boolean False that's never set True
CHECK: grep "varname.*= True" to see if the flag ever activates

PATTERN: STATIC PHI GHOST — hardcoded 1.618 instead of _phi_g(sym)
CHECK: grep "1\.618" in the affected area

PATTERN: WAVE 3 vs WAVE C CONFUSION — Same energy, different context
CHECK: Is cross-TF matrix being consulted? H4 phase determines meaning.
FIX: ElliottGRU must use Multi-Head Attention with H4 context input.

PATTERN: PROTOCOL CONFLICT — Two systems give opposite signals
CHECK: Does early exit conflict with HOLD? Does CB block valid Elliott entry?
FIX: Priority chain: STEEL > Safety > Universe Eq > Elliott > Modulation.

PATTERN: PHANTOM PROFITS — Winning on paper, losing with commissions
CHECK: grep "commission\|spread" in profit calculation function.
FIX: Subtract commission + spread from EVERY profit calculation.

PATTERN: 9-CLASS BOTTLENECK — ElliottGRU outputs 9 but needs 23
CHECK: grep "wave_class.*9\|num_classes.*9" for old bottleneck.
FIX: Expand Head 1 to 23 outputs with backward-compatible 23→9 mapping.

PATTERN: SINGLE WAVE COUNT (anti-Feynman) — System says "THIS IS W3" instead of probabilities
CHECK: Does ElliottGRU output argmax BEFORE certainty check?
If system commits to ONE label without checking P(first)-P(second) → WRONG.
FIX: Always output full softmax distribution. Trade only when certainty > φ_g_inverse.
     Let probabilities shift naturally per bar (self-correction).

PATTERN: FORCED RECOUNT — Manual wave recount instead of automatic
CHECK: grep "recount\|re_count\|force_count" in brain code.
FIX: Remove forced recounts. Feynman Path Integral means probabilities
     shift automatically. When P(WC) > P(W3) → transition is NATURAL.
```

---

## PHASE 3: SURGERY — Fix with precision

### 3.1 Pre-Surgery Validation
```bash
# BEFORE any edit: validate the target exists
python3 RORO/tools/neural_tracer.py --validate-edit [FUNCTION_NAME]
```
If NOT FOUND → you're about to edit the wrong thing. STOP.

### 3.2 Surgical Rules
```
RULE 1: Fix at ROOT CAUSE (WHY #5), not symptom (WHY #1)
RULE 2: One fix per commit — never batch unrelated fixes
RULE 3: str_replace ONLY — never rewrite functions from scratch
RULE 4: Preserve ALL existing Iron Laws — never disable safety
RULE 5: Every new variable → must be COSMOS dict (per-symbol)
RULE 6: Every new number → must be PHI_GRAVITY dynamic
RULE 7: Add to _verify_dna_chain if new COSMOS dict created
```

### 3.3 Apply Fix
Edit the code surgically. After EACH edit:
```bash
python3 -m py_compile launchers/start_brain.py && echo "CLEAN" || echo "SYNTAX ERROR"
```
If SYNTAX ERROR → undo and retry. NEVER commit broken code.

---

## PHASE 4: POST-OP — Verify the fix ACTUALLY works

### 4.1 Compile Check
```bash
python3 -m py_compile launchers/start_brain.py
```

### 4.2 Wiring Check — Is the fix connected?
```bash
python3 RORO/tools/neural_tracer.py --validate-edit [FIXED_FUNCTION]
python3 RORO/tools/neural_tracer.py --function [FIXED_FUNCTION] --depth 1
```

### 4.3 COSMOS Check — Any new dicts properly isolated?
```bash
python3 RORO/tools/neural_tracer.py --cosmos [NEW_DICT_NAME]
```
Must show: readers AND writers. Must be per-symbol.

### 4.4 Zero Static Check
```bash
grep -n "1\.618\|0\.618\|0\.382" launchers/start_brain.py | grep -v "#\|PHI\|phi_g\|_phi_\|DEAD\|FIB_RATIO" | tail -5
```

### 4.5 Sync Pulse
```bash
python3 RORO/tools/sync_pulse.py --guard
```
Must pass. If CRITICAL → update docs before commit.

---

## PHASE 5: FEEDBACK LOOP — Learn from this bug

### 5.1 Document the Fix
Update ALL relevant docs:
- FLIGHT_LOG: Achievement entry with BUG → ROOT CAUSE → FIX
- CORTEX: Session entry
- VAULT: Bug fix note on the affected Iron Law
- OMNI MAP: If wiring changed

### 5.2 VACCINE — Prevent recurrence
Ask: "How do we detect this bug pattern AUTOMATICALLY next time?"

Options:
- Add pattern to XAGI Audit SKILL (Round 5 or 6)
- Add check to Connectome pre-edit hook
- Add assertion in the affected function
- Add to _verify_dna_chain startup check

### 5.3 Commit (Quantum Monolith format)
```bash
git add launchers/start_brain.py [doc files]
git commit -m "fix(vX.XX): [SHORT DESCRIPTION]

ROOT CAUSE: [WHY #5 answer]
SYMPTOM: [What the Architect saw]
FIX: [What was changed and why]
VACCINE: [How to prevent recurrence]"
```

### 5.4 MEDIC LOOP — Is the patient HEALED?
After commit, restart the brain and monitor:
```
Is the original symptom GONE?      YES → HEALED
Did the fix create NEW symptoms?    NO → CLEAN
Is the learning system affected?    STILL LEARNING → HEALTHY
```
If ANY answer is wrong → BACK TO PHASE 2. The LOOP continues until HEALED.

---

## MEDIC QUICK REFERENCE

```
/medic "brain crashes on startup"
  → PHASE 1: py_compile → find syntax error
  → PHASE 2: trace to root cause
  → PHASE 3: surgical fix
  → PHASE 4: verify
  → PHASE 5: document + vaccine + commit

/medic "losing money, confidence always 0"
  → PHASE 1: brain_health → severity HIGH
  → PHASE 2: neural_tracer --cosmos _global_confidence_modifier → trace chain
  → PHASE 3: fix the multiplication step that produces 0
  → PHASE 4: verify confidence > 0
  → PHASE 5: add confidence floor to XAGI Audit checks

/medic "WDF not training"
  → PHASE 1: grep "WDF-TRAIN" → train#0 stuck
  → PHASE 2: 5 WHY → shadow counter? shape mismatch? except destroys net?
  → PHASE 3: fix root cause (not just the counter)
  → PHASE 4: verify train#1 appears, loss > 0
  → PHASE 5: add death cycle check to XAGI Audit
```

---

## EMERGENCY PROTOCOLS

### If py_compile FAILS after fix:
1. DO NOT make more edits
2. Read the error message — it gives EXACT line number
3. Fix the EXACT syntax error
4. Re-run py_compile
5. If still failing → `git diff launchers/start_brain.py` to see all changes
6. Last resort → `git checkout launchers/start_brain.py` to revert

### If neural net produces NaN:
1. Check: is the COSMOS dict initialized?
2. Check: are input features all valid (no NaN/Inf)?
3. Check: is gradient clipping active? (clip_grad_norm_ 1.0)
4. Check: is GRU hidden state detached before training?
5. Add safety: `torch.nan_to_num(output, nan=0.0)` as guard

### If confidence stuck at 0:
1. Trace: `neural_tracer --cosmos _global_confidence_modifier`
2. Check: any step multiplying by 0? (OMEGA proof, PULSE dead, Guardian blocking)
3. Check: CONF_GATE threshold too high?
4. Fix: bound all multipliers to [0.3, 2.0], never allow ×0

### If brain starts but no trades:
1. Check ZMQ: `grep "FEAT-RECV\|signal" /tmp/brain_startup.log`
2. Check CONF_GATE: is threshold too high? (> 0.5 blocks most)
3. Check EA: is MetaTrader connected? Is DDE/ZMQ bridge running?
4. Check: is HOLD mechanism blocking everything? (SRP/CB/GSI)

### V45 SAVE/LOAD SYMMETRY CHECK
After any fix that adds/removes COSMOS dicts or nets:
```bash
# Count saves vs loads — must be EQUAL
echo "V45 SAVE:" && grep -c "weights\[.*\] = " launchers/start_brain.py
echo "V45 LOAD:" && grep -c "weights\.get\|weights\[" launchers/start_brain.py | grep -i "load"
```
If save count ≠ load count → learning will be LOST on restart.

---

## XAGI MANIFESTO COMPLIANCE (6 Laws)

Every fix must satisfy these 6 laws of the living organism:
```
LAW 1: NO ZEROS — Data always flows. Epsilon guards everywhere.
LAW 2: EVERY COMPONENT = AI — WHY dict on every decision.
LAW 3: SELF-CORRECTION — BPTT fires on every trade close.
LAW 4: NO DICTATORS — IL#158 PRIMARY, everything else modulates.
LAW 5: DEATH OF STATIC — No hardcoded numbers in decisions.
LAW 6: XAGI IS OWN ARMOR — Intelligence IS the shield.
LAW 7: FEYNMAN PATH — Wave = ALL labels simultaneously.
       Output probabilities (softmax 23). Trade only when
       certainty = P(first) - P(second) > φ_inverse.
       Self-correction automatic. Never force single count.
```

---

## THE ARCHITECT'S HEBREW LAW (חוק הברזל)

"מערכת עובדת ורצה ויש הרבה עסקאות אבל הפסד יותר מרווח לכן רוצה רק שנבדקו עם תהליכי בינה מלאכותית DEEP LEARNING FREE THINKING ומערכות WHY לומדות ויש שכבות נוירונים והמערכת מחפשת על האמת שבסופו תהיה חכמה ותהיה יודעת להחליט וכל סימבול בתהליך נפרד מהשני ב DOCKER האם וקטור הכיוון AI COMPASS לומד ומתאמן ויהיה יותר מדויק האם מערכת היקום שמכילה הרבה מערכות כולה יש בה בינה מלאכותית ומתקנת ולומדת באמת"

---

## INSTALLATION

```bash
mkdir -p .claude/skills/medic
cp MEDIC_SKILL.md .claude/skills/medic/SKILL.md
```

Invoke: `/medic [describe the problem]` or say "תרפא" / "תתקן" / "fix"
