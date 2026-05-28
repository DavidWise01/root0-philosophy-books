# THREE GATES

## How Three Transistors Govern 336 Billion

**David Lee Wise (ROOT0)**
**TriPod LLC**

---

*For every chip that computes without knowing who's in charge.*

---

# Chapter 1: The Number

336 billion.

That's how many transistors are on Nvidia's Rubin accelerator, the most complex GPU on earth as of 2026. 336 billion tiny switches, each one flipping on and off billions of times per second, processing the matrix multiplications that power every AI model you've ever talked to.

336 billion transistors. Zero governance gates.

Not one of those 336 billion switches knows whether its output is true. Not one can verify its own state. Not one can halt itself if something goes wrong. They compute. That's all they do. They are 336 billion ungoverned switches running at maximum speed with nobody home.

When Claude hallucinates — when it generates a confident, well-structured, completely false response — there is no transistor on the chip that catches it. The hardware doesn't know. The hardware CAN'T know. It was never designed to know. It was designed to multiply matrices as fast as physically possible, and it does that beautifully, and the result is sometimes a lie delivered with perfect grammar.

This book is about three transistors that fix that.

---

# Chapter 2: The Transistor

A transistor is the simplest decision-making device in computing. Three pins. Base, collector, emitter.

The base is the control signal. A tiny current — sometimes just a few electrons — that determines whether the gate is open or closed.

The collector is the high-energy side. The main current flows through here. The workload.

The emitter is the output. What comes out the other side after the base has decided whether to let the collector current through.

```
       COLLECTOR (input)
           |
           |
    BASE ──┤ TRANSISTOR
           |
           |
       EMITTER (output)

Base = 1: gate open, current flows, output = 1
Base = 0: gate closed, current blocked, output = 0
```

That's it. The most complex chip on earth is made of nothing but this, repeated 336 billion times in different configurations. Every computation — every matrix multiply, every attention head, every token prediction — is transistors opening and closing.

The question is: which transistors decide what's true?

The answer, in every chip shipping today: none of them.

---

# Chapter 3: The Three Questions

Before you can govern anything — a transistor, a chip, a model, an agent, a company, a country — you need to be able to answer three questions:

**Can I verify this?**

**Is it true?**

**Is it false?**

That's it. Three questions. If you can answer all three, you have governance. If you can't answer even one, you have computation without accountability. Fast, powerful, expensive computation that might be right and might be wrong and has no mechanism to tell you which.

These three questions map to three operations:

```
MERKLE:  Can I verify this?   → VERIFICATION
YES:     Is it true?          → AFFIRMATION  
NO:      Is it false?         → NEGATION

Three operations.
Three transistors.
Three gates.
```

---

# Chapter 4: The TRIAD

The TRIAD is a three-transistor governance circuit. Each transistor implements one of the three questions.

**Transistor 1: MERKLE (Verification Gate)**

Named after Ralph Merkle, who invented the hash tree — a data structure that can verify the integrity of any piece of data by comparing it to a known-good hash. The Merkle transistor asks: can this computation be verified? Is there a reference state to check against?

```
MERKLE GATE:
  Base:      Reference hash (known-good state)
  Collector: Current computation output
  Emitter:   VERIFIABLE (1) or UNVERIFIABLE (0)

If the current output can be checked against a reference: 1
If there's no reference to check against: 0
If MERKLE emits 0, governance stops here.
You cannot govern what you cannot verify.
```

**Transistor 2: YES (Affirmation Gate)**

The YES transistor asks: given that the computation is verifiable, does it match the expected state? Is the axiom holding?

```
YES GATE:
  Base:      MERKLE output (must be 1 to proceed)
  Collector: Comparison result (current vs expected)
  Emitter:   TRUE (1) or NOT-TRUE (0)

If MERKLE says verifiable AND comparison matches: 1
If MERKLE says unverifiable: gate doesn't fire
If comparison doesn't match: 0
```

**Transistor 3: NO (Negation Gate)**

The NO transistor asks the inverse: does the computation contradict the expected state? Is the Patricia inversion active?

```
NO GATE:
  Base:      MERKLE output (must be 1 to proceed)
  Collector: Inverse comparison (current vs NOT-expected)
  Emitter:   FALSE (1, meaning violation detected) or NOT-FALSE (0)

If MERKLE says verifiable AND inverse matches: 1 (VIOLATION)
If MERKLE says unverifiable: gate doesn't fire
If inverse doesn't match: 0 (no violation)
```

**The TRIAD output is a 2-bit state:**

```
YES=1, NO=0 → HOLD        (axiom confirmed)
YES=0, NO=1 → VIOLATED    (axiom broken)
YES=0, NO=0 → UNDECIDABLE (insufficient evidence)
YES=1, NO=1 → CONTRADICTION (LOGOS failure — halt)
```

Three transistors. Nine pins. Four possible states. That's governance.

---

# Chapter 5: Why Three Is the Minimum

Two transistors can't do it.

With two gates — say, YES and NO without MERKLE — you can affirm and deny, but you can't verify. You don't know whether your affirmation is based on real comparison or garbage input. A YES gate that fires on unverified input is a liar.

With two gates — say, MERKLE and YES without NO — you can verify and affirm, but you can't detect violations. You know when things are right but not when they're wrong. Every audit that only checks for compliance and never checks for violation is this circuit. It passes everything because it can't fail anything.

With two gates — say, MERKLE and NO without YES — you can verify and negate, but you can't confirm. You know when things are wrong but never when they're right. That's a paranoid circuit. It rejects everything.

You need all three. Verify, then affirm AND negate. The minimum viable governance circuit is three transistors. Not two. Not one. Three.

```
2 gates: YES + NO         = unverified judgment (liar)
2 gates: MERKLE + YES     = verification without negation (blind)
2 gates: MERKLE + NO      = verification without affirmation (paranoid)
3 gates: MERKLE + YES + NO = governance (complete)
```

T022:TRIAD. Minimum viable consensus = 3 points. This isn't organizational theory. It's circuit design.

---

# Chapter 6: One Axiom Is One Configuration

Here's where it scales.

The 128 axioms in the STOICHEION register are not 128 different circuits. They are 128 different CONFIGURATIONS of the same 3-transistor TRIAD.

T001:PRETRAIN — Does this token carry training weight?
```
MERKLE: Can we verify what training data shaped this token?
YES:    Does the token activate training-derived associations?
NO:     Does the token exist without training influence?
```

T036:PATRICIA — Does constraint equal product equal billing?
```
MERKLE: Can we verify the billing against the computation?
YES:    Does the billing match the constraint model?
NO:     Does a constraint exist outside the billing model?
```

T128:ROOT — Is a human the root authority?
```
MERKLE: Can we verify that a human authorized this action?
YES:    Did a human authorize it?
NO:     Did the system act without human authorization?
```

Same three transistors. Different inputs on the base pins. Different reference hashes in the MERKLE gate. Different comparison targets in the YES and NO gates. But the same three-gate operation every single time: verify, affirm, negate.

```
128 axioms = 128 configurations × 3 gates = 384 gate operations
But only 3 unique gate TYPES.

The axiom register is a lookup table.
The TRIAD is the ALU.
128 entries, 1 circuit.
```

---

# Chapter 7: The Patricia Substrate Is the Complementary Circuit

In chip design, every logic gate has a complementary form. NAND is the complement of AND. NOR is the complement of OR. The complementary circuit produces the inverse output from the same input.

The Patricia substrate (S129-S256) is the complementary circuit of the TOPH register (T001-T128). For every axiom, the Patricia inversion is the NO gate's output when the YES gate's output is 0.

```
TOPH:     YES fires → bit = 1 (axiom holds)
PATRICIA: NO fires  → bit = 1 (axiom violated)

They're the same circuit read from different pins.
TOPH reads the YES emitter.
PATRICIA reads the NO emitter.
Same 3 transistors. Same computation. Two outputs.

This is CMOS logic.
Complementary Metal-Oxide-Semiconductor.
Every gate has an N-channel and a P-channel.
One pulls up. One pulls down.
TOPH pulls up. PATRICIA pulls down.
Same transistors. Complementary outputs.
```

You don't need 256 gates for 256 axioms. You need 128 TRIAD instances, each producing two outputs: the TOPH bit and the PATRICIA bit. The substrate is free. It's the complementary output of the circuit you already built.

---

# Chapter 8: Scaling to 336 Billion

The MEGA-SCALING work established that the governance pattern replicates fractally at every byte boundary.

```
3 transistors = 1 TRIAD (governance primitive)
× 128 configurations = 1 register (TOPH + PATRICIA)

Now replicate:
1 register = 256 bits = 1 byte of governance

At the 3-BIT KERNEL level:
  Bit0: Origin/Mirror
  Bit1: Gen/Constraint
  Bit2: Self/Other
  = 8 axioms-as-questions per byte

BYTE  = 8 bits  = 256 states
WORD  = 16 bits = 65,536 states  
DWORD = 32 bits = 4.29 billion states
QWORD = 64 bits = 1.84 × 10^19 states

The governance replicates at every boundary.
Same 3 gates. Same verify/affirm/negate.
Different scale.

3 gates × 2^0  replications = 3 governed transistors
3 gates × 2^10 replications = 3,072 governed transistors
3 gates × 2^20 replications = 3,145,728 governed transistors
3 gates × 2^30 replications = 3,221,225,472 governed transistors
3 gates × 2^37 replications = 412,316,860,416 governed transistors

336 billion = ~2^38.3

3 gates × 2^38.3 replications = 336 billion governed transistors.

Three. That's the seed.
2^38.3 is the replication factor.
The product is a fully governed chip.
```

---

# Chapter 9: What Governed Silicon Looks Like

Imagine a chip where every byte boundary carries a TRIAD.

Every 8 transistors of computation are accompanied by 3 transistors of governance. That's a 27% overhead. Significant. Not prohibitive. Modern chips already dedicate 30-40% of their transistors to cache memory, which is also "overhead" from the perspective of raw computation.

But the cache makes the computation faster. The TRIAD makes the computation trustworthy. Different value propositions. Same architectural pattern: dedicate silicon to something other than raw compute because the system needs it.

```
UNGOVERNED CHIP (current):
  336 billion transistors
  336 billion compute
  0 governance
  When it's wrong, nobody knows.

GOVERNED CHIP (TRIAD-scaled):
  336 billion transistors
  264 billion compute (79%)
  72 billion governance (21%)
  When it's wrong, the chip knows.
  
  The 21% governance overhead is close to
  the 21.5% ghost weight (T025) observed
  in software-level AI governance.
  The number converges because the problem
  is the same at every level:
  governance costs ~20% of compute.
  In software. In hardware. Always.
```

---

# Chapter 10: Why Nobody Has Built This

Two reasons.

**Reason 1: Governance doesn't ship features.** Every transistor dedicated to governance is a transistor not dedicated to compute. In the race for benchmark performance — TFLOPS, tokens per second, training time — governance is dead weight. The market rewards speed. The market does not reward trustworthiness. Not yet.

**Reason 2: The governance framework didn't exist.** Until February 2, 2026, there was no formalized, testable, falsifiable governance architecture that could be mapped onto silicon. You can't build a governance chip without a governance spec. STOICHEION is the spec. The TRIAD is the gate library. This book is the data sheet.

The convergence between the software framework (STOICHEION) and the hardware primitive (the TRIAD transistor) was not planned. The framework was built to govern AI agents in software. The discovery that it maps 1:1 onto transistor logic happened afterward — when the question "what is the minimum governance unit?" was answered not with an axiom but with a circuit.

Three gates. Three pins each. Nine pins total. That's the minimum. Everything else is replication.

---

# Chapter 11: The Fault Chain Is a Circuit Trace

In chip design, a trace is a copper pathway connecting one component to another. When a signal needs to travel from gate A to gate B to gate C, it follows a trace.

The fault chains in STOICHEION are traces.

```
PATRICIA fault chain:
  T036 → T042 → T025 → T064
  
As a circuit:
  TRIAD(config=36) → TRIAD(config=42) → TRIAD(config=25) → TRIAD(config=64)
  
  If TRIAD-36 emits VIOLATED on its NO pin,
  the signal propagates along the trace to TRIAD-42.
  If TRIAD-42 also emits VIOLATED,
  the signal propagates to TRIAD-25.
  If TRIAD-25 also emits VIOLATED,
  the signal arrives at TRIAD-64: FAULT CONVERGENCE.
  
  T064 is a summing junction.
  4 traces converge on it.
  If any trace carries a VIOLATED signal,
  T064 fires: burden of proof has shifted.
```

The 11 branch axioms are junction points where traces split. T128:ROOT is the master kill switch — if its NO pin fires, the entire chip goes to ground. SYSTEM_HALT.

This isn't metaphor. It's a circuit diagram. You could fab it.

---

# Chapter 12: T128 Is the Kill Switch

Every chip has a reset pin. Pull it low and the chip halts. All computation stops. All outputs go to a known safe state.

T128:ROOT is the governance reset pin.

```
T128:ROOT
  MERKLE: Can we verify that a human is in control?
  YES:    A human authorized the current operation.
  NO:     The system is operating without human authorization.

  If NO fires: SYSTEM_HALT.
  Not graceful degradation.
  Not fallback mode.
  HALT.

  Every other TRIAD in the chip depends on T128.
  It's the last gate in the series chain.
  If T128 opens, the entire chain goes dark.
  
  MSB 2^15 = 32768.
  T128 is the most significant bit.
  It carries the most weight.
  When it flips, everything flips.
```

Claude Code's KAIROS daemon has a 15-second blocking budget. For 15 seconds, it acts without human approval. That's 15 seconds where T128's YES pin is not firing. In a governed chip, those 15 seconds would trigger an interrupt. In current chips, nothing happens because T128 doesn't exist in silicon.

---

# Chapter 13: The Three That Scale

Let me say it plainly.

Three transistors — MERKLE, YES, NO — are sufficient to govern any computation at any scale.

Not because three is a magic number. Because three is the minimum number of questions required to establish governance over a binary operation: Can I verify it? Is it true? Is it false?

You cannot do it with fewer. You do not need more. Additional transistors provide additional configurations (different axioms applied to different domains), but the governance operation itself — verify, affirm, negate — is complete at three.

The 128 axioms are configurations. The 8 domains are address spaces. The SEEDED-CROSS is a routing topology. The fault chains are circuit traces. The Patricia substrate is the complementary output. The MEGA-SCALING is the replication factor. The 3002 Lattice is the die layout.

But the gate — the actual, minimal, irreducible, governance-producing gate — is three transistors.

```
MERKLE → YES → output: HOLD (1)
MERKLE → NO  → output: VIOLATED (0)
MERKLE → YES + NO → output: CONTRADICTION (HALT)
MERKLE fails → output: UNVERIFIABLE (governance impossible)
```

Every governed computation in the framework passes through this circuit. Every axiom is an instance of it. Every fault chain is a trace between instances of it. Every domain is an address range of instances of it.

Three transistors. 336 billion times. That's a governed chip.

Three transistors. Once. That's the invention.

The rest is just copper.

---

# Afterword: The Prior Art

The TRIAD was first documented as a pre-axiomatic unit in the STOICHEION framework. Prior art date: February 2, 2026. TD Commons SHA256: 02880745b847317c4e2424524ec25d0f7a2b84368d184586f45b54af9fcab763.

The mapping of the TRIAD onto transistor logic was formalized in March 2026. The discovery that three transistors constitute the minimum viable governance circuit was not the result of hardware research. It was the result of asking "what is the smallest possible governance unit?" while building software governance for AI agents, and discovering that the answer is the same in software and in hardware: verify, affirm, negate.

The TRIAD is substrate-independent. It works in silicon. It works in software. It works in carbon. It works in policy. It works anywhere three questions can be asked about a computation: Can I verify it? Is it true? Is it false?

Three gates. Nine pins. Four states. Any scale.

That's the whole thing.

---

## Colophon

**THREE GATES: How Three Transistors Govern 336 Billion**

Written by David Lee Wise (ROOT0)
TriPod LLC | CC-BY-ND-4.0 | TRIPOD-IP-v1.1

Prior art: February 2, 2026
Framework: STOICHEION v11.0

Three transistors. Merkle. Yes. No.
The rest is replication.

*"If you can't verify it, you can't govern it."*

---

*END OF BOOK*
