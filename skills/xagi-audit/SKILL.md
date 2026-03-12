---
name: xagi-audit
description: "XAGI Deep Audit — Full organism verification. 8-round cosmic X-ray from foundation to future proof. Use when: system losing money, suspecting dead learning, after upgrades, or Architect says 'XAGI'. Triggers on: XAGI, audit, בדיקת, losing, הפסד, stuck, frozen, dead learning, not learning, CAGI, proof of life, crash test, blind shooting, hallucination. Runs 8 rounds: Foundation + Neural Nets + Feedback + Universe + Stagnation + CRASH TEST + CONNECTOME Medic + Future Proof. Covers ALL 27+ learning systems, 30+ neural nets, 150+ COSMOS dicts, all Iron Laws, all protocols, weight punishment, hallucination detection, convergence proof."
mode: true
---

# ⚡ XAGI DEEP AUDIT — THE COSMIC X-RAY ⚡
# PROTOCOL: LIVING CONNECTOME DIAGNOSTIC
# AUTHORITY: The Architect | MODE: MAXIMUM EFFORT

════════════════════════════════════════════════════════════════
WHEN THIS SKILL ACTIVATES, YOU ENTER XAGI AUDIT MODE.
NO ASSUMPTIONS. NO HALLUCINATIONS. ONLY PROOF.
READ THE ENTIRE BRAIN WITH AST. VERIFY WITH GREP. PROVE WITH NUMBERS.
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

## ROUND 4: UNIVERSE ENGINE — IQEND + PHYSICS + ELLIOTT

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

### 4.4 Elliott Wave AI (IL#188-195)
```bash
for il in 188 189 190 191 192 193 194 195; do
    python3 RORO/tools/neural_tracer.py --il $il 2>/dev/null | head -3
done
```
VERIFY: ElliottEnergyGRU, WavePhaseNet, CorrectionDetectorNet, ElliottCompassNet, WaveDegreeNet — all training.

### 4.5 Wave Creator + Energy Type + Gravity Center
```bash
grep -n "wave_creator\|energy_type\|gravity_center\|wave_dna" launchers/start_brain.py | head -15
```

### 4.6 PHI_GRAVITY 6D — Breathing
```bash
python3 RORO/tools/neural_tracer.py --function _get_phi_field --depth 1
python3 RORO/tools/neural_tracer.py --function _calculate_adaptive_gravity_phi --depth 1
```
VERIFY: 6 dimensions (position, velocity, acceleration, jerk, curvature, torsion). Per-symbol. Per-tick.

---

## ROUND 5: ZERO STAGNATION HUNT — FIND THE DEAD

### 5.1 Frozen Systems
```bash
grep -r "train#0\|loss=0\.0000\|loss=0\.00 " /path/to/brain/logs/ 2>/dev/null | tail -20
# OR from live output:
grep "train#0" launchers/start_brain.py | head -10
```

### 5.2 Empty Training Functions
```bash
grep -n "def.*train_step\|def.*_train\b" launchers/start_brain.py | while read line; do
    num=$(echo "$line" | cut -d: -f1)
    # Check if function body is just 'pass'
    sed -n "$((num+1)),$((num+3))p" launchers/start_brain.py | grep -q "pass" && echo "DEAD: $line"
done
```

### 5.3 Orphan COSMOS Dicts (defined but never read)
```bash
python3 RORO/tools/neural_tracer.py --index 2>/dev/null
grep "readers: 0" RORO/core/BRAIN_INDEX.md | head -10
```

### 5.4 Static Values in Decision Paths
```bash
grep -n "0\.618\|1\.618\|0\.382\|2\.618\|4\.236" launchers/start_brain.py | grep -v "#\|PHI\|phi_g\|_phi_\|DEAD\|ABOLISHED\|Fib.*ratio\|FIB_RATIO" | head -20
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

---

## OUTPUT REQUIREMENT

After ALL 8 rounds, produce this EXACT format:

```
╔═══════════════════════════════════════════════════════════════╗
║               XAGI DEEP AUDIT — TRUTH TABLE                  ║
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
║ R4 UNIVERSE                                                   ║
║   IQEND3 (15):        XX/15 | Universe Eq: ACTIVE / DEAD     ║
║   12 Forces:          XX/12 | Elliott (8): XX/8 TRAINING      ║
║   Wave Creator/DNA:   DYNAMIC / STATIC                        ║
║   PHI_GRAVITY 6D:     BREATHING / STATIC                      ║
╠═══════════════════════════════════════════════════════════════╣
║ R5 STAGNATION                                                 ║
║   Frozen train#0:     [list or NONE]                          ║
║   Dead functions:     [list or NONE]                          ║
║   Orphan COSMOS:      [list or NONE]                          ║
║   Static values:      [count or ZERO]                         ║
╠═══════════════════════════════════════════════════════════════╣
║ R6 CRASH TEST                                                 ║
║   Hallucination:      CLEAN / DETECTED                        ║
║   Weight Punishment:  ACTIVE (losses penalize) / DEAD         ║
║   Blind Shooting:     NO (signals vary) / YES (random)        ║
║   HOLD Gates:         XX active / ZERO (danger!)              ║
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
