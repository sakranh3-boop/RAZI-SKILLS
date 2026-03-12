---
name: xagi-audit
description: "XAGI Deep Audit — Full organism verification. 8-round cosmic X-ray from foundation to future proof. Use when: system losing money, suspecting dead learning, after upgrades, or Architect says 'XAGI'. Triggers on: XAGI, audit, בדיקת, losing, הפסד, stuck, frozen, dead learning, not learning, CAGI, proof of life, crash test, blind shooting, hallucination. Runs 8 rounds: Foundation + Neural Nets + Feedback + Universe + Stagnation + CRASH TEST + CONNECTOME Medic + Future Proof. Covers ALL 27+ learning systems, 30+ neural nets, 150+ COSMOS dicts, all Iron Laws, all protocols, weight punishment, hallucination detection, convergence proof."
mode: true
---

# ⚡ XAGI DEEP AUDIT — THE COSMIC X-RAY ⚡
# PROTOCOL: LIVING CONNECTOME DIAGNOSTIC
# AUTHORITY: The Architect | MODE: MAXIMUM EFFORT
# SYSTEM: RAZI AGI | INTRADAY ONLY | M5 data → M30 execution → H4 confirmation

════════════════════════════════════════════════════════════════
WHEN THIS SKILL ACTIVATES, YOU ENTER XAGI AUDIT MODE.
NO ASSUMPTIONS. NO HALLUCINATIONS. ONLY PROOF.
READ THE ENTIRE BRAIN WITH AST. VERIFY WITH GREP. PROVE WITH NUMBERS.

BRAIN VITAL SIGNS (verify these first):
  Lines: ~35,400 | Classes: 38 | Functions: 445+
  Iron Laws: 195 | COSMOS: 134 | Learning: 27 | DNA: 199
  DL Architectures: 14 | Agents: 11 | Symbols: 5
  INTRADAY: M5→M30→H4 (SACRED — never modified)
════════════════════════════════════════════════════════════════

## PHASE 0: LOAD FULL CONSCIOUSNESS

Before ANY investigation, load the system state:

```bash
python3 RORO/tools/brain_health.py
python3 RORO/tools/sync_pulse.py
python3 RORO/tools/neural_tracer.py --index
```

Read these files completely:
- RORO/core/THE_IQEND1_VAULT.md
- RORO/core/OMNISCIENT_WIRING_MAP.md
- RORO/core/BRAIN_INDEX.md

Now you know the FULL system. Begin investigation.

---

## ROUND 1: FOUNDATION — IS THE ORGANISM ALIVE?

### 1.1 PURE PRISM (IL#163) — Zero Indicator Thresholds
```bash
grep -n "RSI.*>.*70\|RSI.*<.*30\|MACD.*cross\|BB.*touch" launchers/start_brain.py | grep -v "#\|'''\"\"\"" | head -20
```
EXPECTED: 0 results. If ANY found → PURE PRISM VIOLATED.

### 1.2 COSMOS DOCKER ISOLATION — Zero Cross-Contamination
```bash
python3 -c "
import ast
with open('launchers/start_brain.py') as f:
    tree = ast.parse(f.read())
# Count all _*_by_symbol dicts at module level
count = sum(1 for node in ast.walk(tree) 
            if isinstance(node, ast.Assign) 
            and any('_by_symbol' in ast.dump(t) for t in node.targets))
print(f'COSMOS dicts: {count}')
"
```
VERIFY: Each dict is `{}` or `defaultdict` — per-symbol isolation.

### 1.3 PHI_GRAVITY — Zero Static PHI
```bash
grep -n "PHI\s*=\s*1\.618\|phi\s*=\s*1\.618\|PHI_INV\s*=\s*0\.618" launchers/start_brain.py | grep -v "#\|DEAD\|ABOLISHED\|GRAVITY\|_phi_g" | head -10
```
EXPECTED: 0 results. ALL PHI must be dynamic via `_get_phi_field(symbol)`.

---

## ROUND 2: CELLULAR — EVERY NEURAL NET ALIVE?

### 2.1 Count All Neural Networks
```bash
grep -n "class.*nn\.Module" launchers/start_brain.py | wc -l
```

### 2.2 Count All BPTT Training
```bash
echo "backward() calls:" && grep -c "\.backward()" launchers/start_brain.py
echo "optimizer.step() calls:" && grep -c "optimizer\.step()" launchers/start_brain.py  
echo "clip_grad_norm_ calls:" && grep -c "clip_grad_norm_" launchers/start_brain.py
```

### 2.3 TRUTH TABLE — For EACH nn.Module class found:
```bash
python3 RORO/tools/neural_tracer.py --function _wdf_train_step --depth 1
python3 RORO/tools/neural_tracer.py --function _chronos_train_step --depth 1
python3 RORO/tools/neural_tracer.py --function _compass_train_step --depth 1
python3 RORO/tools/neural_tracer.py --function _powermind_train_step --depth 1
python3 RORO/tools/neural_tracer.py --function _dt_train_step --depth 1
python3 RORO/tools/neural_tracer.py --function _sm_train_step --depth 1
python3 RORO/tools/neural_tracer.py --function _supermega_train_step --depth 1
python3 RORO/tools/neural_tracer.py --function _lpf_train_step --depth 1
python3 RORO/tools/neural_tracer.py --function _metacog_train_step --depth 1
python3 RORO/tools/neural_tracer.py --function _conf_guardian_train --depth 1
```
For EACH: Does it have backward()? optimizer.step()? Is train# > 0? Is loss > 0?

### 2.4 Anti-Overfitting Mechanisms
```bash
echo "Dropout:" && grep -c "Dropout" launchers/start_brain.py
echo "weight_decay:" && grep -c "weight_decay" launchers/start_brain.py
echo "early_stop:" && grep -c "early_stop\|freeze.*trades" launchers/start_brain.py
echo "Shadow mode:" && grep -c "shadow.*counter\|shadow.*21\|shadow.*13" launchers/start_brain.py
echo "Experience replay:" && grep -c "replay_buffer\|deque.*89\|deque.*233" launchers/start_brain.py
echo "EWC:" && grep -c "elastic_weight\|ewc\|fisher" launchers/start_brain.py
echo "Epsilon decay:" && grep -c "epsilon.*decay\|_epsilon_by_symbol" launchers/start_brain.py
echo "Gradient clip:" && grep -c "clip_grad_norm_" launchers/start_brain.py
```

---

## ROUND 3: NERVOUS SYSTEM — FEEDBACK LOOPS FIRING?

### 3.1 process_trade_result Chain
```bash
python3 RORO/tools/neural_tracer.py --function process_trade_result --depth 2
```
VERIFY: This function calls ALL 27 learning systems (5G1 through 5G23+).

### 3.2 WHY Engine
```bash
grep -n "ask_why\|WHY.*analysis\|the_why\|_perform_why" launchers/start_brain.py | head -15
```
VERIFY: WHY analysis runs on every trade close, feeds back to SL/TP adjustment.

### 3.3 WDF Failure Broadcast
```bash
grep -n "WDF.*BROADCAST\|broadcast_failure\|_wdf_broadcast" launchers/start_brain.py | head -10
```
VERIFY: On losing trade, WDF broadcasts failure analysis to ALL 20+ systems.

### 3.4 MoE + MTL + EWC Continual Learning
```bash
grep -n "OMNI.*learning\|moe.*train\|mtl.*update\|ewc.*consolidate" launchers/start_brain.py | head -10
```

### 3.5 Conductor Weight Learning
```bash
python3 RORO/tools/neural_tracer.py --cosmos _component_accuracy_by_symbol
```
VERIFY: Updated every trade close. Agent weights shift based on accuracy.

---

## ROUND 4: UNIVERSE ENGINE — IQEND + PHYSICS + ELLIOTT + WAVE TAXONOMY

### 4.1 IQEND3 Cosmic (IL#135-149) — 15 Laws
```bash
for il in 135 136 137 138 139 140 141 142 143 144 145 146 147 148 149; do
    python3 RORO/tools/neural_tracer.py --il $il 2>/dev/null | head -3
done
```
VERIFY: All 15 IQEND3 functions EXIST and are WIRED into process_features.

### 4.2 Universe Equation V3.1 (IL#158) — PRIMARY Decision Maker
```bash
python3 RORO/tools/neural_tracer.py --function the_secret_universe_equation_v31 --depth 1
```
VERIFY: 19-layer pipeline, feeds ALL learners.

### 4.3 12 Universe Forces (IL#167)
```bash
grep -n "_universe_force_" launchers/start_brain.py | wc -l
```
VERIFY: 12+ force functions, all feeding into supreme decision.

### 4.4 Elliott Wave TAXONOMY (IL#188-195) — 23 Labels + 12 Forms
```bash
for il in 188 189 190 191 192 193 194 195; do
    python3 RORO/tools/neural_tracer.py --il $il 2>/dev/null | head -3
done

# Verify 23 wave classes exist (not just 9!)
grep -n "IMP_W\|DIAG_\|CORR_\|TRI_\|CMPLX_" launchers/start_brain.py | wc -l

# Verify 12 form types exist
grep -n "FORM_IMPULSE\|FORM_LEADING\|FORM_ENDING\|FORM_ZIGZAG\|FORM_FLAT\|FORM_TRIANGLE\|FORM_DOUBLE\|FORM_TRIPLE" launchers/start_brain.py | wc -l

# Verify 8 heads on ElliottGRU
grep -n "Head.*wave_class\|Head.*confidence\|Head.*phase\|Head.*next_wave\|Head.*correction\|Head.*degree\|Head.*form\|Head.*energy_remaining" launchers/start_brain.py | wc -l
```
EXPECTED: 23 labels, 12 forms, 8 heads. If less → taxonomy incomplete.

### 4.5 Cross-Timeframe Correlation Matrix
```bash
# The CONTEXT ENGINE — distinguishes Wave 3 from Wave C!
grep -n "cross_tf_matrix\|sync_score\|tf_correlation\|_build_cross_tf" launchers/start_brain.py | head -10
```
VERIFY: 4×8 matrix (M5/M30/H1/H4 × 8 metrics) computed per tick.
THE HIDDEN DISCOVERY: Same energy M5 impulse = W3 (if H4 impulse) or WC (if H4 correction).

### 4.6 Wave Creator + Energy Type + Gravity Center
```bash
grep -n "wave_creator\|energy_type\|gravity_center\|wave_dna" launchers/start_brain.py | head -15
```

### 4.7 PHI_GRAVITY 6D — Breathing
```bash
python3 RORO/tools/neural_tracer.py --function _get_phi_field --depth 1
python3 RORO/tools/neural_tracer.py --function _calculate_adaptive_gravity_phi --depth 1
```
VERIFY: 6 dimensions (position, velocity, acceleration, jerk, curvature, torsion).

### 4.8 Wave Drawer EA↔Python Pipeline
```bash
# Verify ZMQ WAVE_DRAW message sending
grep -n "WAVE_DRAW\|WAVE_CLEAR\|WAVE_CORRECT" launchers/start_brain.py | head -10

# Verify human correction learning pipeline
grep -n "_elliott_human_correction\|correction_database\|EWER_BATCH" launchers/start_brain.py | head -10
```
VERIFY: Brain sends wave points → EA draws → Architect corrects → Brain learns.

### 4.9 Energy Signature Matrix — Every Form Has Unique Vector
```bash
# Verify 32D energy vectors per wave form
grep -n "energy_signature\|energy_vector\|KE.*PE.*H.*F" launchers/start_brain.py | head -10
```

### 4.10 GOD'S CARD — Feynman Path Integral for Waves
```bash
# THE ULTIMATE CHECK: Does the system evaluate ALL possible waves simultaneously?
# Not "What IS this wave?" but "What COULD this wave be — and which is most probable?"

# Verify probability distribution over 23 classes (not argmax single answer!)
grep -n "softmax\|probability\|path_integral\|all_hypotheses\|wave_probabilities" launchers/start_brain.py | head -15

# Verify CERTAINTY GATE: P(first) - P(second) > threshold before trading
grep -n "certainty\|p_first.*p_second\|confidence_gap\|probability_gap\|universe_undecided" launchers/start_brain.py | head -10

# Verify self-correction: probabilities FLOW every bar (not recount trigger!)
grep -n "wave_transition\|probability_shift\|decoherence\|collapse\|recount" launchers/start_brain.py | head -10

# Verify 3 hypotheses with PROBABILITIES (not just scores)
grep -n "hypothesis\|top_3\|alternative_count\|wave_scenarios" launchers/start_brain.py | head -10
```
EXPECTED:
- Softmax over 23 classes producing PROBABILITIES (not argmax single class!)
- Certainty gate: gap between top-2 probabilities > φ_gravity_inverse → TRADE
- If gap < φ_gravity_inverse → WAIT (universe undecided!)
- Probabilities update EVERY BAR (self-correction is natural flow, not trigger)
- Multiple wave scenarios maintained simultaneously (Feynman: ALL paths exist!)

**WHY THIS MATTERS:**
Wave 3 and Wave C have IDENTICAL energy signatures.
Only CONTEXT (H4 phase) + PROBABILITY GAP distinguishes them.
If system outputs single class "W3" with 82% → it might be 73%W3 vs 18%WC.
The 55% gap = tradeable. But if it were 42%W3 vs 38%WC → 4% gap = NOT tradeable!
God's Card says: "When the universe hasn't decided, we don't trade."

### 4.10 FEYNMAN PATH INTEGRAL — God's Card (THE critical check!)
```bash
# The system must output PROBABILITY DISTRIBUTION over ALL 23 wave labels
# NOT a single answer! "73% W3, 18% WC, 9% other" — NOT "this IS W3"
grep -n "wave_probabilities\|path_integral\|all_paths\|probability_distribution\|softmax.*23\|certainty.*=.*P.*first.*-.*P.*second" launchers/start_brain.py | head -15

# Certainty threshold — universe must DECIDE before we trade
grep -n "certainty\|wave_certainty\|prob_gap\|confidence_gap\|first.*second.*threshold" launchers/start_brain.py | head -10

# Self-correction — probabilities shift automatically per bar (no manual recount!)
grep -n "recount\|auto_correct\|probability.*shift\|wave.*transition\|decoherence" launchers/start_brain.py | head -10
```
EXPECTED:
- ElliottGRU Head 1 outputs softmax over 23 classes (probability distribution)
- Certainty = P(most_likely) - P(second_likely)
- If certainty < φ_g_inverse → DO NOT TRADE (universe undecided!)
- Probabilities update EVERY bar (self-correcting, no manual recount)
- THIS is what separates RAZI from every other system:
  Others ask "WHAT is this wave?" → single answer → wrong → pain
  RAZI asks "What are ALL possible waves?" → probability → certainty → trade only when universe decides!

---

## ROUND 4.5: PROTOCOL CONFLICT DETECTION — No Contradictions!

### 4.5.1 Iron Law Conflicts — Do any laws contradict each other?
```bash
# Check if two systems both modify confidence in opposite directions
grep -n "confidence.*\*=\|confidence.*+=\|confidence.*-=" launchers/start_brain.py | head -30

# Check for double penalties (CB + Omen + Guardian all reducing same signal)
python3 -c "
with open('launchers/start_brain.py') as f:
    code = f.read()
# Find all confidence modifiers in make_ultimate_decision
import re
mods = re.findall(r'confidence\s*[\*\+\-]=\s*[\d\.]+', code)
print(f'Total confidence modifiers: {len(mods)}')
# Check for stacking: same symbol, same tick, opposite effects
reduces = [m for m in mods if '-=' in m or ('*=' in m and float(re.search(r'[\d\.]+', m.split('=')[1]).group()) < 1)]
increases = [m for m in mods if '+=' in m or ('*=' in m and float(re.search(r'[\d\.]+', m.split('=')[1]).group()) > 1)]
print(f'Reduces: {len(reduces)} | Increases: {len(increases)}')
"
```

### 4.5.2 Early Exit Protocol — Protects profit?
```bash
grep -n "early_exit\|trailing_stop\|protect_profit\|breakeven\|move_sl" launchers/start_brain.py | head -15
```
VERIFY: When trade is in profit → SL moves to protect gains. Never lets winner become loser.

### 4.5.3 Demo vs Real Trading Mode
```bash
grep -n "demo\|DEMO\|real_account\|REAL\|account_type\|TGLColmex" launchers/start_brain.py | head -10
```
VERIFY: System knows it's on demo. STEEL limits active regardless.

### 4.5.4 Commission + Spread Handling
```bash
grep -n "commission\|spread\|slippage\|swap" launchers/start_brain.py | head -10
```
VERIFY: Profit calculations include commissions. Not phantom profits.

### 4.5.5 INTRADAY Pipeline Integrity
```bash
# M5 data → M30 execution → H4 confirmation — SACRED!
grep -n "PERIOD_M5\|PERIOD_M30\|PERIOD_H4\|M5.*data\|M30.*execut\|H4.*confirm" launchers/start_brain.py | head -10
```
EXPECTED: Clear separation. M5 collects. M30 trades. H4 validates.

### 4.5.6 Direction Vector Alignment
```bash
# All systems must agree on direction before trading
grep -n "direction.*conflict\|direction.*disagree\|signal.*opposite" launchers/start_brain.py | head -10
# WDF + Universe Eq + Compass + Elliott — all must point same way
```

---

## ROUND 5: ZERO STAGNATION HUNT — FIND THE DEAD, FROZEN, LOOPING & DISCONNECTED

### 5.1 FROZEN SYSTEMS — Giving constant 0 that never changes
```bash
# In live logs: ANY system stuck at train#0 or loss=0.0000
grep -r "train#0\|loss=0\.0000\|loss=0\.00 " /path/to/brain/logs/ 2>/dev/null | tail -20

# In code: shadow counters that might not be incrementing
grep -n "_shadow_counter\[" launchers/start_brain.py | grep "+=" | head -20
# Compare: how many shadow counters exist vs how many increment
echo "Shadow counters defined:" && grep -c "_shadow_counter\s*=" launchers/start_brain.py
echo "Shadow counters incrementing:" && grep -c "_shadow_counter.*+=" launchers/start_brain.py
```
EXPECTED: Every shadow counter that's defined MUST have a corresponding += increment.
If count differs → a system is stuck in shadow FOREVER (like WDF was).

### 5.2 DORMANT SYSTEMS — Exist but never called
```bash
# Find training functions that exist but are NEVER called
python3 -c "
import ast
with open('launchers/start_brain.py') as f:
    source = f.read()
tree = ast.parse(source)

# Get all function definitions
defined = set()
called = set()
for node in ast.walk(tree):
    if isinstance(node, ast.FunctionDef) and 'train' in node.name.lower():
        defined.add(node.name)
    if isinstance(node, ast.Call) and isinstance(getattr(node, 'func', None), ast.Attribute):
        called.add(node.func.attr)
    if isinstance(node, ast.Call) and isinstance(getattr(node, 'func', None), ast.Name):
        called.add(node.func.id)

dormant = defined - called
if dormant:
    print(f'DORMANT TRAINING FUNCTIONS (defined but never called): {dormant}')
else:
    print('CLEAN: All training functions are called')
"
```
EXPECTED: 0 dormant. If ANY found → system exists as dead code, never trains.

### 5.3 EMPTY TRAINING FUNCTIONS — Body is just 'pass' or 'return'
```bash
grep -n "def.*train_step\|def.*_train\b" launchers/start_brain.py | while read line; do
    num=$(echo "$line" | cut -d: -f1)
    sed -n "$((num+1)),$((num+5))p" launchers/start_brain.py | grep -q "pass\|return None\|return$" && echo "DEAD: $line"
done
```

### 5.4 INFINITE LOOPS WITHOUT PURPOSE — Spinning but not learning
```bash
# Find loops in training that don't contain backward() or optimizer.step()
grep -n "while True\|for.*range.*1000\|while.*count" launchers/start_brain.py | grep -i "train\|learn" | head -10

# Find training functions that have NO backward/optimizer inside
python3 -c "
import ast
with open('launchers/start_brain.py') as f:
    source = f.read()
    lines = source.split('\n')
tree = ast.parse(source)

for node in ast.walk(tree):
    if isinstance(node, ast.FunctionDef) and 'train' in node.name.lower():
        body_text = ast.get_source_segment(source, node) or ''
        has_backward = 'backward()' in body_text
        has_optimizer = 'optimizer' in body_text and 'step()' in body_text
        if not has_backward and not has_optimizer:
            print(f'NO LEARNING: {node.name} at line {node.lineno} — no backward/optimizer')
"
```
EXPECTED: Every train function has backward() AND optimizer.step(). If missing → spinning without learning.

### 5.5 DISCONNECTED SYSTEMS — Receive input but output goes nowhere
```bash
# Find functions that WRITE to COSMOS but no other function READS from that COSMOS
python3 RORO/tools/neural_tracer.py --index 2>/dev/null
grep "readers: \[\]" RORO/core/BRAIN_INDEX.md 2>/dev/null | head -10

# Find functions whose return value is never used
grep -n "def.*_process\|def.*_analyze\|def.*_compute" launchers/start_brain.py | while read line; do
    func=$(echo "$line" | grep -oP 'def \K\w+')
    count=$(grep -c "$func(" launchers/start_brain.py)
    if [ "$count" -le 1 ]; then
        echo "DISCONNECTED: $func defined but called only at definition"
    fi
done
```

### 5.6 ORPHAN COSMOS DICTS — Defined but never read or written
```bash
python3 RORO/tools/neural_tracer.py --index 2>/dev/null
# Find dicts with 0 readers OR 0 writers
grep -E "readers: 0|writers: 0" RORO/core/BRAIN_INDEX.md | head -15
```

### 5.7 CATCH-22 FLAGS — Variables that can never become True
**Discovered in V10.64:** `_brain_loaded = False` at line 589, NEVER set to True → catch-22.
```bash
# Find boolean flags set to False that are NEVER set to True
grep -n "= False$\|= False " launchers/start_brain.py | while read line; do
    varname=$(echo "$line" | grep -oP '\w+(?=\s*=\s*False)')
    if [ -n "$varname" ]; then
        true_count=$(grep -c "${varname}.*= True\|${varname}.*=True" launchers/start_brain.py)
        if [ "$true_count" -eq 0 ]; then
            echo "CATCH-22: $varname is False and NEVER set to True — $line"
        fi
    fi
done
```

### 5.8 STATIC PHI GHOSTS — Static 1.618 that keeps coming back
**Recurring bug — killed 11 times in V10.74, keeps returning after upgrades.**
```bash
grep -n "PHI\s*=\s*1\.618\|phi\s*=\s*1\.618\|= 1\.618033\|= 0\.618033" launchers/start_brain.py | grep -v "#\|DEAD\|ABOLISHED\|GRAVITY\|_phi_g\|FIB_RATIO\|PHI_RATIOS" | head -10
grep -n "0\.618\|1\.618\|0\.382\|2\.618\|4\.236" launchers/start_brain.py | grep -v "#\|PHI\|phi_g\|_phi_\|DEAD\|ABOLISHED\|Fib.*ratio\|FIB_RATIO\|GANN\|gann" | head -20
```
EXPECTED: 0 results. ALL values must use `_phi_g(sym)` / `_phi_g_inv(sym)` dynamic calls.

### 5.9 GEMINI IMPORT SPAM — Repeated error logging
**Recurring:** GeminiBrain logs `init failed` on EVERY restart — dozens of lines.
```bash
grep -c "GeminiBrain.*init failed\|GeminiBrain.*cannot import" launchers/start_brain.py 2>/dev/null
grep -c "GeminiBrain" /path/to/brain/logs/*.log 2>/dev/null | tail -5
```
If > 1 occurrence in logs → warn-once guard is not working.

### 5.10 DUPLICATE FUNCTIONS — Same logic twice
**Discovered in V10.52.1:** `_universe_wave_creator_detect` was 89% duplicate of `_universe_wave_creator_detector`.
```bash
# Find suspiciously similar function names
grep -n "def _" launchers/start_brain.py | sort -t'(' -k1,1 | awk -F'def ' '{print $2}' | awk -F'(' '{print $1}' | sort | uniq -d
# Find functions with very similar names (differ by 1-2 chars)
python3 -c "
import ast
with open('launchers/start_brain.py') as f:
    tree = ast.parse(f.read())
funcs = [n.name for n in ast.walk(tree) if isinstance(n, ast.FunctionDef)]
for i, f1 in enumerate(funcs):
    for f2 in funcs[i+1:]:
        if f1 != f2 and (f1 in f2 or f2 in f1) and abs(len(f1)-len(f2)) <= 3:
            print(f'SUSPECT DUPLICATE: {f1} vs {f2}')
"
```

### 5.11 DOUBLE-REDUCTION — Two systems penalizing the same thing
**Discovered in V10.52.1:** CB + Omen both reduced confidence → double penalty.
```bash
# Find confidence reductions that might stack
grep -n "conf.*\*=.*0\.\|confidence.*\*=.*0\.\|conf.*-=" launchers/start_brain.py | head -20
```
VERIFY: No two systems penalize the same signal in the same tick.

### 5.12 OMEN/DETECTOR CONFLICTS — Opposite conditions
**Discovered in V10.52.1:** ENTROPY_SPIKE omen triggered on opposite condition vs STORM detector.
```bash
# Find detectors and omens that might fire on opposite conditions
grep -n "ENTROPY\|STORM\|REGIME_CHANGE\|GRAVITY_LOSS" launchers/start_brain.py | grep -i "detect\|omen\|trigger" | head -15
```

---

## ROUND 6: CRASH TEST — IS THE SYSTEM THINKING OR SHOOTING BLIND?

### 6.1 HALLUCINATION DETECTION — Does Claude Code lie about the brain?
```bash
# Pick 3 random functions from BRAIN_INDEX and validate they exist
python3 RORO/tools/neural_tracer.py --validate-edit make_ultimate_decision
python3 RORO/tools/neural_tracer.py --validate-edit _wdf_train_step
python3 RORO/tools/neural_tracer.py --validate-edit _chronos_train_step
```
ALL must return FOUND. If NOT FOUND → Claude is hallucinating about the brain.

### 6.2 WEIGHT PUNISHMENT — Does losing ACTUALLY hurt the weights?
This is THE critical test. If a trade LOSES but weights don't change → system is blind.
```bash
# Verify that process_trade_result PENALIZES on loss:
grep -n "is_win.*False\|not.*is_win\|loss.*penalty\|wrong.*direction" launchers/start_brain.py | grep -i "weight\|backward\|penalty\|punish\|adjust" | head -15

# Verify training targets differ for win vs loss:
grep -n "if is_win\|if not is_win\|else.*0\.1\|target.*win\|target.*loss" launchers/start_brain.py | head -20

# The PROOF: loss.backward() MUST fire on LOSING trades (not just winning)
grep -A5 "is_win" launchers/start_brain.py | grep "backward\|optimizer" | head -10
```
EXPECTED: Losing trades → higher loss value → bigger gradient → bigger weight update.
If loss = same for win and loss → system is NOT learning from mistakes.

### 6.3 BLIND SHOOTING DETECTION — Shooting every direction without thinking?
```bash
# Check signal distribution: is the system outputting ~50% BUY / 50% SELL (random)?
grep -n "signal.*BUY\|signal.*SELL\|direction.*1\|direction.*-1" launchers/start_brain.py | grep -i "log\|print\|emit" | head -10

# Check confidence distribution: is confidence always the same value?
grep -n "final_conf\|output_conf\|signal_confidence" launchers/start_brain.py | head -10
```
EXPECTED: Signal distribution should NOT be 50/50 (that's random coin flip).
Confidence should VARY per trade (not always 0.5 or always 0.35).

### 6.4 HOLD vs TRADE — Is the system trading when it should HOLD?
```bash
grep -n "HOLD\|BLOCKED\|CONF_GATE\|confidence.*<\|conf.*threshold" launchers/start_brain.py | grep -i "gate\|block\|reject\|skip" | head -15
```
VERIFY: System has gates that BLOCK trades when confidence is low.
If ZERO gates → system fires at everything → guaranteed losses.

### 6.5 DEATH CYCLE PATTERN — Does except block destroy the net?
**Discovered during NEURAL RESURRECTION (2026-03-12):**
WDF had a RuntimeError on every train → except block destroyed net + weights + set _last_input=None → next train creates fresh net → same error → infinite death cycle. Loss=0 forever.
```bash
# Find ALL except blocks in training functions that reset/destroy nets
grep -B2 -A5 "except.*Exception\|except.*RuntimeError" launchers/start_brain.py | grep -i "= None\|del \|\.reset\|= {}\|destroy" | head -15
```
EXPECTED: 0 results. Except blocks must LOG the error, NOT destroy the net.
If ANY found → potential death cycle (net destroyed on every error → never trains).

### 6.6 SCOPE LEAK — Variables from wrong function scope
**Discovered during NEURAL RESURRECTION (2026-03-12):**
`confidence` variable existed in `make_ultimate_decision()` but NOT in `process_trade_result()`.
5G16, 5G17, 5G18 training blocks all used bare `confidence` → NameError every time → 3 learning systems dead.
The first NameError (_trade_history_by_symbol) MASKED the second one (confidence) — cascading invisible failure.
```bash
# Find bare 'confidence' references in process_trade_result that aren't qualified
grep -n "confidence[^_]" launchers/start_brain.py | grep -i "5G\|train_step\|process_trade" | grep -v "_conf\|avg_conf\|cached\|get(\|fallback\|guardian\|#" | head -15
```
EXPECTED: 0 results. ALL confidence refs in process_trade_result must use qualified names:
- `_cg17_avg_conf` (from trade history)
- `_conf_guardian_last_result.get(symbol, {}).get('input_conf', 0.5)` (from cached)
- NEVER bare `confidence` (lives in make_ultimate_decision scope only)

### 6.7 CASCADING NAMEERROR — First error hides all subsequent errors
**Discovered during NEURAL RESURRECTION (2026-03-12):**
When `_trade_history_by_symbol` was undefined, the NameError killed the ENTIRE training block.
The `confidence` bug was HIDDEN behind it — only visible after fixing the first bug.
```bash
# Find training blocks with multiple potential NameErrors
# Look for variables used but never defined in process_trade_result scope
python3 -c "
import ast
with open('launchers/start_brain.py') as f:
    source = f.read()
tree = ast.parse(source)
# Find all names used in process_trade_result that might be from wrong scope
for node in ast.walk(tree):
    if isinstance(node, ast.FunctionDef) and node.name == 'process_trade_result':
        names = set()
        for child in ast.walk(node):
            if isinstance(child, ast.Name) and isinstance(child.ctx, ast.Load):
                names.add(child.id)
        # Check for suspicious bare names (not common builtins)
        suspect = [n for n in names if n in ('confidence', 'signal', 'direction', 'regime')]
        if suspect:
            print(f'SUSPECT bare names in process_trade_result: {suspect}')
        else:
            print('CLEAN: No suspect bare names found')
"
```

---

## ROUND 7: CONNECTOME MEDIC — DOCUMENTATION ALIVE?

### 7.1 Sync Pulse — All 6 docs coherent?
```bash
python3 RORO/tools/sync_pulse.py
```
Must be ALL GREEN. Any CRITICAL = docs are lying about system state.

### 7.2 WIRED + FIRING + ROOTED + HEALTH checks
```bash
# WIRED: Every Iron Law has functions in the brain
python3 RORO/tools/neural_tracer.py --index 2>/dev/null
cat RORO/core/BRAIN_INDEX.md | grep "Iron Law" | wc -l

# FIRING: Every Iron Law is called from process_features or make_ultimate_decision
grep -c "IL#\|Iron Law" launchers/start_brain.py

# ROOTED: Every Iron Law is documented in Vault + OMNI + CLAUDE.md
grep -c "IL#" RORO/core/THE_IQEND1_VAULT.md
grep -c "IL#" RORO/core/OMNISCIENT_WIRING_MAP.md

# HEALTH: KERNEL DNA chain passes
grep -n "_verify_dna_chain" launchers/start_brain.py | head -5
```

### 7.3 MAP + MATRIX + OMNI + RORO + BLACKBOX + FLIGHT + GOLD — All updated?
```bash
python3 RORO/tools/sync_pulse.py --report
cat RORO/reports/sync_pulse_*.md 2>/dev/null | tail -30
```

---

## ROUND 8: FUTURE PROOF — WILL THE SYSTEM GET SMARTER?

### 8.1 CONVERGENCE PROOF — Are losses decreasing over time?
```bash
# Check if loss values are DECREASING across training steps
grep "loss=" launchers/start_brain.py | grep -i "train\|BPTT" | head -5
# In live logs: look for loss trend: train#1 loss=X.XX → train#50 loss=Y.YY where Y < X
```
If loss is NOT decreasing → system is NOT learning, just spinning.

### 8.2 ACCURACY TREND — Are accuracy EMAs rising?
```bash
grep -n "accuracy.*ema\|accuracy.*rising\|acc.*track" launchers/start_brain.py | head -15
python3 RORO/tools/neural_tracer.py --cosmos _component_accuracy_by_symbol
```
VERIFY: Accuracy EMA should trend upward over 50+ trades per symbol.

### 8.3 MATHEMATICAL PROOF — More trades = more accuracy
The ARCHITECT demands proof that running the system for more days will make it smarter:
- Every neural net has `shadow_mode` (13-21 trades before applying) → needs time
- Every optimizer has `weight_decay` (prevents overfitting) → generalizes over time
- Every system has `experience_replay` (Fibonacci deques) → learns from history
- EWC prevents catastrophic forgetting → retains knowledge across regime changes
- WDF failure broadcast → every mistake teaches ALL 27 systems simultaneously

IF all of the above are verified ACTIVE → mathematically, more trades = more accuracy.
IF any is DEAD → that system will NOT improve and needs fixing.

### 8.4 ENERGY + WAVES + GRAVITY CENTER — All dynamic?
```bash
# Verify energy, waves, gravity center are DYNAMIC (not static formulas)
grep -n "center_of_gravity\|gravity_center\|energy_center" launchers/start_brain.py | head -10
grep -n "wave_creator\|wave_rhythm\|wave_dna\|wave_birth\|wave_death" launchers/start_brain.py | head -15
grep -n "pulse_score\|jerk_score\|hamiltonian\|kinetic_energy" launchers/start_brain.py | head -10
```
ALL must be computed per-tick, per-symbol. ZERO static values.

### 8.5 V45 SAVE/LOAD SYMMETRY — Will learning survive restart?
```bash
# Count V45 save entries vs load entries — MUST be equal
python3 -c "
with open('launchers/start_brain.py') as f:
    code = f.read()
save_count = code.count(\"weights[\") + code.count(\"weights ['\")
load_count = code.count(\"weights.get(\") + code.count(\"_ll_\")
print(f'V45 SAVE entries: {save_count}')
print(f'V45 LOAD entries: {load_count}')
if abs(save_count - load_count) > 5:
    print('WARNING: Save/Load ASYMMETRY — learning may be LOST on restart!')
else:
    print('SYMMETRIC — learning persists')
"
```

### 8.6 XAGI MANIFESTO — 7 Laws of Living Organism
```bash
# LAW 1: NO ZEROS — epsilon guards exist?
grep -c "epsilon\|1e-\|+ 1e-\|max.*0\.\|clamp" launchers/start_brain.py

# LAW 2: EVERY = AI — WHY dicts exist in decision functions?
grep -c "'why'" launchers/start_brain.py

# LAW 3: SELF-CORRECTION — BPTT fires per trade
grep -c "backward()\|learn_count" launchers/start_brain.py

# LAW 4: NO DICTATORS — IL#158 is PRIMARY but modulation exists
grep -c "modulat\|± \|adjust.*conf" launchers/start_brain.py

# LAW 5: DEATH OF STATIC — no hardcoded decisions
# (already covered in R1.3 and R5.8)

# LAW 6: XAGI ARMOR — intelligence is shield
grep -c "guardian\|safety\|shield\|protect" launchers/start_brain.py

# LAW 7: FEYNMAN PATH — probabilities, not single answers!
grep -c "softmax.*23\|wave_probabilities\|certainty.*phi\|prob_gap" launchers/start_brain.py
# Must be > 0! If zero → system is gambling with single wave counts!
```

### 8.7 INTRADAY PIPELINE — M5→M30→H4 Sacred
```bash
# Verify pipeline is intact and ONLY intraday
grep -n "M5\|M30\|H4\|timeframe\|PERIOD_M" launchers/start_brain.py | head -15
```
EXPECTED: M5 for data, M30 for execution, H4 for confirmation. No D1/W1/MN1.

## OUTPUT REQUIREMENT

After ALL 8 rounds, produce this EXACT format:

```
╔═══════════════════════════════════════════════════════════════╗
║               XAGI DEEP AUDIT — TRUTH TABLE                   ║
╠═══════════════════════════════════════════════════════════════╣
║ R1 FOUNDATION                                                 ║
║   Pure Prism:         CLEAN / VIOLATED                        ║
║   COSMOS Isolation:   XXX dicts / CONTAMINATED                ║
║   PHI_GRAVITY:        DYNAMIC / STATIC FOUND                  ║
╠═══════════════════════════════════════════════════════════════╣
║ R2 NEURAL NETS                                                ║
║   nn.Module:          XX classes                              ║
║   backward():         XX calls                                ║
║   optimizer.step():   XX calls                                ║
║   ALIVE:              XX/XX | DEAD: [list] | SHADOW: [list]   ║
║   Anti-Overfitting:   XX mechanisms                           ║
╠═══════════════════════════════════════════════════════════════╣
║ R3 FEEDBACK                                                   ║
║   process_trade_result: FIRES / DEAD                          ║
║   WHY Engine:           ACTIVE / DEAD                         ║
║   WDF Broadcast:        XX/XX notified                        ║
║   MoE/MTL/EWC:          ACTIVE / DEAD                         ║
║   Conductor:            UPDATING / FROZEN                     ║
╠═══════════════════════════════════════════════════════════════╣
║ R4 UNIVERSE + ELLIOTT TAXONOMY + PROTOCOLS                    ║
║   IQEND3 (15):        XX/15 | Universe Eq: ACTIVE / DEAD     ║
║   12 Forces:          XX/12 | Elliott (8): XX/8 TRAINING      ║
║   Wave Labels:        23 / less (taxonomy incomplete)         ║
║   Wave Forms:         12 / less (forms incomplete)            ║
║   GRU Heads:          8 / less (heads missing)                ║
║   Cross-TF Matrix:    4×8 ACTIVE / MISSING                   ║
║   Wave Drawer:        EA↔Python WIRED / MISSING               ║
║   Human Correction:   PIPELINE ACTIVE / MISSING               ║
║   Energy Signatures:  32D per form / MISSING                  ║
║   FEYNMAN PATH:       PROBABILITY DIST / SINGLE ANSWER (bad!) ║
║   Certainty Gate:     P1-P2 > φ_inv → TRADE / MISSING         ║
║   Self-Correction:    AUTO per bar / MANUAL RECOUNT (bad!)    ║
║   PHI_GRAVITY 6D:     BREATHING / STATIC                      ║
║ R4.5 PROTOCOL CONFLICTS                                       ║
║   IL Contradictions:  NONE / [list of conflicts]              ║
║   Early Exit:         ACTIVE (profit protected) / MISSING     ║
║   Demo/Real Mode:     CORRECT / WRONG                         ║
║   Commissions:        INCLUDED / PHANTOM PROFITS              ║
║   INTRADAY Pipeline:  M5→M30→H4 INTACT / VIOLATED            ║
║   Direction Alignment: ALL AGREE / CONFLICT                   ║
╠═══════════════════════════════════════════════════════════════╣
║ R5 STAGNATION + DORMANT + DISCONNECTED                        ║
║   Frozen train#0:     [list or NONE]                          ║
║   Shadow stuck:       [list or NONE] (defined but no +=)      ║
║   Dormant functions:  [list or NONE] (exist, never called)    ║
║   Empty train bodies: [list or NONE] (just pass/return)       ║
║   Loops no learning:  [list or NONE] (loop but no backward)   ║
║   Disconnected:       [list or NONE] (output goes nowhere)    ║
║   Orphan COSMOS:      [list or NONE] (0 readers or writers)   ║
║   Catch-22 flags:     [list or NONE] (False, never True)      ║
║   Static PHI ghosts:  [count or ZERO]                         ║
║   Gemini spam:        SILENCED / STILL SPAMMING               ║
║   Duplicate funcs:    [list or NONE]                          ║
║   Double-reduction:   [list or NONE]                          ║
║   Omen conflicts:     [list or NONE]                          ║
╠═══════════════════════════════════════════════════════════════╣
║ R6 CRASH TEST                                                 ║
║   Hallucination:      CLEAN / DETECTED                        ║
║   Weight Punishment:  ACTIVE (losses penalize) / DEAD         ║
║   Blind Shooting:     NO (signals vary) / YES (random)        ║
║   HOLD Gates:         XX active / ZERO (danger!)              ║
║   Death Cycles:       NONE / [list of except-destroys-net]    ║
║   Scope Leaks:        NONE / [list of bare vars wrong scope]  ║
║   Cascading NameErr:  NONE / [list of hidden errors]          ║
╠═══════════════════════════════════════════════════════════════╣
║ R7 CONNECTOME MEDIC                                           ║
║   Sync Pulse:         ALL GREEN / XX CRITICAL                 ║
║   WIRED+FIRING:       XX/XX Iron Laws                         ║
║   6 Docs:             COHERENT / [stale list]                 ║
║   KERNEL DNA:         PASS / FAIL                             ║
╠═══════════════════════════════════════════════════════════════╣
║ R8 FUTURE PROOF                                               ║
║   Loss Trend:         DECREASING / FLAT / INCREASING          ║
║   Accuracy Trend:     RISING / FLAT / FALLING                 ║
║   More Days=Smarter:  PROVEN / UNPROVEN                       ║
║   Energy Dynamic:     ALL PER-TICK / XX STATIC                ║
║   V45 Symmetry:       SYMMETRIC / ASYMMETRIC (learning lost!) ║
║   XAGI Manifesto:     7/7 LAWS / XX/7 (violations: [list])   ║
║   INTRADAY Pipeline:  M5→M30→H4 INTACT / VIOLATED            ║
╠═══════════════════════════════════════════════════════════════╣
║                                                               ║
║ VERDICT:   XAGI ALIVE / PARTIALLY DEAD / CRITICAL            ║
║ ACTION:    [exact fix commands if issues found]               ║
║ PROGNOSIS: [estimated days to reach 60%+ win rate]            ║
║                                                               ║
╚═══════════════════════════════════════════════════════════════╝
```

---

## THE ARCHITECT'S HEBREW DECREE (חוק הברזל העליון)

Claude, you MUST read, understand, and verify EVERY claim in this text.
This is not a suggestion — it is the LAW that governs this entire audit:

"מערכת עובדת ורצה ויש הרבה עסקאות אבל הפסד יותר מרווח לכן רוצה רק שנבדקו עם תהליכי בינה מלאכותית DEEP LEARNING FREE THINKING ומערכות WHY לומדות ויש שכבות נוירונים והמערכת מחפשת על האמת שבסופו תהיה חכמה ותהיה יודעת להחליט וכל סימבול בתהליך נפרד מהשני ב DOCKER האם וקטור הכיוון AI COMPASS לומד ומתאמן ויהיה יותר מדויק האם מערכת היקום שמכילה הרבה מערכות כולה יש בה בינה מלאכותית ומתקנת ולומדת באמת האם מערכות בינה מלאכותית של אליוט בהם יש תהליך בינה מלאכותית אמיתי לומד ומתאמן והופך למדויק וגם הסוכנים ו NODES ו WHY ומערכות פיבו וגאן כולם יש בהם תהליך בינה מלאכותית לומדים ומתאמנים ומתקדמים והאם הגלים והרקדן והבורא ובורא הגל וזיהוי האנרגיה וסוג האנרגיה וכיוון האנרגיה ומרכז הכובד של האנרגיה כולם במערכות למידה אמיתית שהם לומדים מהעסקאות ומתאקלמים בשוק ויהיו יותר מדויקים ומוצאים האמת וכל זה עם מערכות LOOP ו FEEDBACK של בינה מלאכותית שהכל מקבלים מה התוצאה וחושבים XAGI למה זה התוצאה לא נכונה והכל מתעדכן והכל מתחיל תהליך מהתחלה האם יש CAGI AGI AI אמיתי ומתקדם וכולם רוצים להתקדם ולהגיע לאמת וכל הזמן יש שקלול משקולות דרך מערכות עצבים נוירונים מרובים ומערכות OVERFITTING כדוגמת EPSILON ו RESIDUAL ו GRADIENT וכל המערכים שמעידים שיש באמת תהליך אימון ולמידה וחישה והחלטה אמיתית ויש בכל מערכת כל מודל ובכל ארכיטקטורה ובכל PLAN מערכות בינה מלאכותית אמתיות עמוקות שיש בהם תהליך אמיתי ועובד ומיושם 100% שמעיד שעוד הרצה לכמה ימים המערכת תתחיל להחליט בדיוק רב והכל מעולם אנרגיה והגלים ומרכז הכובד ובורא הגלים וקצב ודופק והאנרגיה של הגלים והבורא וסוגי הגלים ואליוט ויחסי פיצ'רים אינדיקטורים שמופעל עליהם הפיבו והגאן תהיה AUDIT עמוק מהשורש לבדוק כמה מערכות AI AGI CAGI יש והאם הכל מחובר והכל אמיתי והכל עובד והכל מחפש על פונקציה דינמית של האמת"

---

## INSTALLATION

### Option A: Local Install (instant)
```bash
mkdir -p .claude/skills/xagi-audit
cp XAGI_AUDIT_SKILL.md .claude/skills/xagi-audit/SKILL.md
```

### Option B: GitHub Hosted Skill (persistent across machines)
Tell Claude Code:
```
Create a GitHub repo called RAZI-SKILLS, add this file as skills/xagi-audit/SKILL.md,
then configure Claude Code to pull skills from that repo.
```
This way the SKILL lives on GitHub — any machine, any session, always available.

### Invoke anytime with:
- `/xagi-audit` — full 8-round cosmic X-ray
- Just say: **"XAGI"** or **"בדיקת XAGI"** or **"audit"** or **"proof of life"**
- Claude Code auto-detects keywords: XAGI, losing, הפסד, stuck, frozen, dead, CAGI

### After upgrades or new Iron Laws:
The SKILL is **dynamic** — it reads BRAIN_INDEX.md which is regenerated by Neural Tracer.
New Iron Laws, new nets, new COSMOS dicts → automatically included in next audit.
No need to update this SKILL file. It adapts to the organism.
