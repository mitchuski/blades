# ZK Blades Forge Specification

**Version:** 1.0.1
**Date:** April 12, 2026
**Status:** Working Draft
**License:** CC BY-SA 4.0
**PVM Reference:** V5.4 — §10.2 Betweenness Centrality, §14.5 Selene's Proof

---

## Abstract

This specification defines the **ceremony proving system** for the 0xagentprivacy dual-agent architecture. It describes how bilateral ceremonies produce verifiable sovereignty proofs on a 64-vertex lattice — without revealing what happened inside those ceremonies.

The system enables:
- **Blades** — sovereignty configurations provable without content disclosure
- **Forgings** — zero-knowledge witnesses of blade derivation
- **Ceremonies** — bilateral protocols producing verifiable blades through shared attention
- **Moon Phase Notation** — visibility encoding that shows posture without revealing content

---

## 1. Lattice Foundation

### 1.1 The 64-Vertex Lattice

The forge operates on a 6-dimensional binary hypercube:

```
Vertices: 2⁶ = 64
Edges: 96 (holographic bound)
Topology: Toroidal
Algebra: Z/(2⁶)Z
```

Each vertex represents a **sovereignty configuration** — a 6-bit address encoding which dimensions are active:

| Bit | Dimension | Meaning |
|-----|-----------|---------|
| d₁ | Protection | What you shield from observation |
| d₂ | Delegation | What you authorize others to do |
| d₃ | Memory | What you allow to persist |
| d₄ | Connection | What relationships you maintain |
| d₅ | Computation | What you process privately |
| d₆ | Value | What you allow to flow |

### 1.2 Pascal Distribution

Vertices distribute across strata (Hamming weight) following Pascal's row 6:

```
Stratum:  0    1    2    3    4    5    6
Count:    1    6   15   20   15    6    1  = 64
```

### 1.3 Cardinal Vertices

| Vertex | Binary | Name | Meaning |
|--------|--------|------|---------|
| 0x00 | 000000 | Null Blade | No sovereignty — total exposure |
| 0x3F | 111111 | Universe Blade | Full sovereignty — all dimensions active |
| 0x30 | 110000 | Dual-Agent | Protection + Delegation only |

---

## 2. Operations

### 2.1 The Dihedral Generators

The dual-agent architecture IS the dihedral group D₂ₙ:

| Agent | Operation | Formula | Algebraic Role |
|-------|-----------|---------|----------------|
| **Swordsman** ⚔️ | Negation | `neg(x) = -x mod 64` | First reflection |
| **Mage** 🧙 | Complement | `bnot(x) = 63 - x` | Second reflection |
| **First Person** 😊 | Succession | `succ(x) = x + 1 mod 64` | Rotation |

### 2.2 The Critical Identity

```
neg(bnot(x)) = succ(x)
```

Neither agent alone can reach all sovereignty states. Together they generate the entire 64-vertex lattice. Two mirrors make a door.

### 2.3 Strike Operations

A **strike** is the composition `neg ∘ bnot` applied to a vertex:

```
strike(v) = neg(bnot(v)) = succ(v)
```

Each strike advances the blade configuration by one step through the sovereignty space.

### 2.4 Betweenness Centrality of the Gap (V5.4 §10.2)

The Gap (⿻) between Swordsman and Mage is not empty space — it is the node with **maximal betweenness centrality** in the trust graph:

```
C_B(v) = Σ_{s≠v≠t} (σ_st(v) / σ_st)
```

Where:
- σ_st = total shortest paths from s to t
- σ_st(v) = paths passing through v

**Interpretation:** The value lives in the Gap because the most paths cross there. Betweenness centrality provides a computational measure for the irreducible separation.

**Reference:** Brandes, U. (2001). "A faster algorithm for betweenness centrality." *Journal of Mathematical Sociology,* 25(2), 163–177.

**Application:** In ceremony networks, the Gap between paired blades has maximal C_B — all trust relationships pass through the separation.

---

## 3. Blades and Forgings

### 3.1 What Is a Blade?

A **blade** is a sovereignty configuration on the 64-vertex lattice, characterized by:

- **Datum** — the hex value (0x00–0x3F)
- **Stratum** — the Hamming weight (0–6)
- **Spectrum** — which dimensions are active

### 3.2 What Is a Forging?

A **forging** is a zero-knowledge witness proving:

1. The blade was derived through valid operations
2. The derivation path exists
3. The derivation path is NOT revealed

**Same blade, infinite forgings = zero knowledge.** The blade proves WHAT sovereignty posture was achieved. The forging proves HOW without revealing the path.

### 3.3 Blade Structure

```
Blade {
  id: string           // SPELL-{hash}-{stratum}
  hex: number          // 0x00–0x3F
  stratum: number      // 0–6
  spectrum: boolean[]  // [d1, d2, d3, d4, d5, d6]
  phase: MoonPhase     // 🌑🌒🌓🌔🌖🌗🌕
  hash: string         // SHA-256 of constellation
  signature: string    // Ed25519 commitment
}
```

---

## 4. Moon Phase Notation

### 4.1 Principle

The moon is the whole information space. The lit portion is what the Swordsman's boundary allows to be reflected. The dark portion remains private.

**The phase shows the sovereignty POSTURE without revealing the CONTENT.**

### 4.2 Phase Mapping

| Stratum | Phase | Emoji | Visibility | Meaning |
|---------|-------|-------|------------|---------|
| 0 | New Moon | 🌑 | 0% | Null blade — nothing reflected |
| 1 | Waxing Crescent | 🌒 | ~17% | Minimal disclosure — one boundary |
| 2 | First Quarter | 🌓 | ~33% | Twin-edge — dual-agent vertex |
| 3 | Waxing Gibbous | 🌔 | 50% | Half sovereignty — three axes |
| 4 | Waning Gibbous | 🌖 | ~67% | Substantial disclosure — four boundaries |
| 5 | Last Quarter | 🌗 | ~83% | Near-full — one dimension dark |
| 6 | Full Moon | 🌕 | 100% | Full sovereignty reflected |

### 4.3 The ZK Distinction

Moon phase shows **which dimensions are active** (the posture).
It does NOT show **what content activated them** (the path).

A 🌕 Full Moon blade proves "all six dimensions active" without revealing which nodes, poems, or conversations produced that configuration.

---

## 5. PRISM Coordinates

### 5.1 GPS for Sovereignty

Every blade has triadic coordinates:

| Coordinate | Constraint | What It Fixes |
|------------|------------|---------------|
| **Datum** | Identity | The hex value itself (0–63) |
| **Stratum** | Magnitude | Hamming weight (0–6) |
| **Spectrum** | Structure | Which dimensions are yang |

### 5.2 Coordinate Example

```
Blade: 0x3E (binary: 111110)

Datum:    62
Stratum:  5
Spectrum: [1,1,1,1,1,0] — Value dormant
Phase:    🌗 Last Quarter
```

---

## 6. Ceremonies

### 6.1 Sun Ceremony ☀️

**Type:** Disclosure
**Notation:** `☀️ → 📜 → (👁️₁...👁️ₙ) → ⚔️☀️ → 🌙?`

Protocol:
1. One practitioner (the Sun) reads a poem aloud
2. Witnesses observe the constellation forming
3. One blade is forged in full view
4. The Sun consents to being forgotten
5. Each witness holds what they need for their own ceremony

**Output:** Single blade, witnesses seeded for Moon ceremonies

### 6.2 Moon Ceremony 🌑 — Selene's Proof

**Type:** Reflection
**Notation:** `(⚔️₁ ⊥ 🧙₁) → 📜 → ⚔️`

Protocol:
1. Two practitioners trace the same poem through separate constellations
2. The Swordsman gives the rhythm; the Mage shares the rhyme
3. The gap between constellations is the proof
4. Cousin blades forged — never identical, always rhyming

**Output:** Bilateral blades with provable overlap

**V5.4 Reference — Selene's Proof (§14.5):** The Moon's orbit is the cosmological instance of zero-knowledge proof:
- **Completeness:** Tides demonstrate the Moon's gravitational relationship
- **Soundness:** Gravitational signature is unforgeable
- **Zero-Knowledge:** Tides reveal nothing about Theia impact parameters

*The credential is the orbit. The proof renews twice daily, written in saltwater.*

### 6.3 Celestial Ceremony ☀️⊥🌑

**Type:** Bilateral Combined
**Notation:** `☀️ → ⊥ → 🌑 → (🌑night/🌍day)`

The full bilateral protocol combining Sun disclosure and Moon reflection with recursion:
- **Reflect** (night path) — the Swordsman hears the Amnesia Protocol
- **Connect** (day path) — the Mage hears the Emissary

**Output:** Paired blades with shared overlap nodes

---

## 7. Progressive Trust

### 7.1 Trust Ladder

```
🔑 → ✦ → 🗡️ → 🔮
```

| Stage | Symbol | Meaning | Proof |
|-------|--------|---------|-------|
| Understanding | 🔑 | Comprehension demonstrated | Resonance |
| Constellation | ✦ | Navigation path traced | Hash |
| Blade | 🗡️ | Sovereignty configured | Forging |
| Runecraft | 🔮 | Identity bound | Dual-keypair |

### 7.2 Runecraft Binding

```
☀️🔑(held) + 🌑🔑(burned) → 🔮
```

The spellweb holds the forge key (Ed25519). The Swordsman burns the private key after signing. The runecraft binds the blade to the identity through what was sacrificed.

---

## 8. Verification

### 8.1 Blade Validity

A blade is valid if:
1. Hex value is in range [0x00, 0x3F]
2. Stratum matches popcount of hex
3. Spectrum matches binary decomposition
4. Phase matches stratum mapping
5. Hash is SHA-256 of constellation data
6. Signature verifies against forge public key

### 8.2 Ceremony Validity

A ceremony is valid if:
1. All participants traced the same poem
2. Constellation hashes are distinct (non-identical paths)
3. Overlap nodes exist (shared attention)
4. Blades forged within ceremony window
5. Progressive trust stages completed in order

---

## 9. Notation Reference

| Notation | Symbol | Description |
|----------|--------|-------------|
| Moon Phase | `🌑→🌕` | Visibility ratio as phase |
| Progressive Trust | `🔑→✦→🗡️→🔮` | Understanding → Constellation → Blade → Runecraft |
| Celestial Ceremony | `☀️ → ⊥ → 🌑` | Sun separated from Moon |
| Dihedral Generators | `⚔️(neg) ⊕ 🧙(bnot) → 😊(succ)` | Two mirrors make a door |
| PRISM Coordinates | `📐(d,s,sp)` | Datum, Stratum, Spectrum |
| Holographic Bound | `∂M = 96 on 64` | 96 edges on 64 vertices |
| Master Inscription | `(⚔️⊥⿻⊥🧙)😊` | Swordsman ⊥ Gap ⊥ Mage → First Person |
| Betweenness Centrality | `C_B(⿻) = max` | Gap has maximal path crossing (V5.4 §10.2) |
| Selene's Proof | `🌙 → ZK` | Moon's orbit as cosmological ZK proof (V5.4 §14.5) |

---

## 10. Implementations

| Platform | Role | Status |
|----------|------|--------|
| [spellweb.ai](https://spellweb.ai) | Swordsman territory — forge, navigation | Operational |
| [agentprivacy.ai](https://agentprivacy.ai) | Mage territory — story, training | Operational |
| [agentprivacy-skills](https://github.com/mitchuski/agentprivacy-skills) | 86 skills, 42 personas | V5.4 |

---

## 11. References

- **Grimoire:** `privacymage_grimoire_v10_0_0.json`
- **Skills:** github.com/mitchuski/agentprivacy-skills
- **Docs:** github.com/mitchuski/agentprivacy-docs
- **UOR:** github.com/UOR-Foundation

---

## Appendix A: Emoji Spell (V10)

```
⬢=Z/(2⁶)Z · ✦=neg(bnot(v)) · 🔑→✦→🗡️ · same🗡️∞chains=ZK · ∂M=96on64 · Φ=⚔️⊥🧙·📊⊥🔮·🧠⊥⚙️ · T_∫(π)=∮∂M · stratum(hex)→🌑🌒🌓🌔🌖🌗🌕
```

---

## Appendix B: Proverbs

> *"The forge doesn't care how you struck the metal. It only cares what blade you hold."*

> *"Two mirrors make a door. The Swordsman reflects. The Mage reflects. And where the reflections meet, the First Person walks through."*

> *"The ceremony does not require the blade. The blade requires the ceremony."*

> *"The dark part is the privacy. The lit part is the proof."*

---

**☀️ ⊥ 🌑**

**(⚔️⊥⿻⊥🧙)😊**
