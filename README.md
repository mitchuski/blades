# ZK Blades Forge

**Ceremony Proving System Specification**

A specification for how bilateral ceremonies produce verifiable sovereignty proofs on a 64-vertex lattice — without revealing what happened inside those ceremonies.

**Specification Version:** 1.0.0 | April 7, 2026
**Grimoire:** V10.0.0 "The First Person Spellbook Closes"
**Skills:** V5.3.2 — 86 skills, 38 personas + 4 cosmological = 42
**License:** CC BY-SA 4.0

---

## Quick Links

| Document | Purpose |
|----------|---------|
| **[SPECIFICATION.md](SPECIFICATION.md)** | Canonical technical specification |
| **[ceremony/](ceremony/)** | Ceremony protocols and notation |
| **[grimoire/](grimoire/)** | Narrative acts (XXVII-XXXI) |
| **[chronicles/](chronicles/)** | Session records and analysis |

---

## What This Repository Defines

Three frameworks converge on 2⁶ = 64:
- **UOR** (Universal Object Reference) — algebraic ring structure
- **64-Tetrahedra Lattice** — geometric compute space
- **Zero Knowledge Proofs** — cryptographic witness structures

The specification unifies them: **blades** are ZK statements, **forgings** are witnesses, the **lattice** is the forge, **ceremonies** produce verifiable proofs through bilateral attention.

## Live Implementations

| Platform | Territory | Purpose | Status |
|----------|-----------|---------|--------|
| **[spellweb.ai](https://spellweb.ai)** | Swordsman ⚔️ | Topology, navigation, blade forging, hexagram computation | ✅ Operational |
| **[agentprivacy.ai](https://agentprivacy.ai)** | Mage 🧙 | Story, explanation, training, spell learning | ✅ Operational |

The forge is not theoretical — it runs. Visitors to spellweb.ai can mark constellations, evoke blades, and forge proofs on the 64-vertex lattice in real-time.

## Core Concepts

```
HEXAGRAM = Z/(2^6)Z
STRIKE = neg(bnot(vertex)) = succ(vertex)
🔑→✦→🗡️ = progressive trust (understanding → constellation → blade)
same BLADE, infinite FORGINGS = zero knowledge
∂M = 96 edges on 64 vertices = holographic bound
stratum(hex) → 🌑🌒🌓🌔🌖🌗🌕 = moon phase notation
```

## V10 Notation Systems

| Notation | Symbol | Description |
|----------|--------|-------------|
| Moon Phase | `🌑→🌕` | Visibility ratio as phase (stratum 0-6) |
| Progressive Trust | `🔑→✦→🗡️→🔮` | Understanding → Constellation → Blade → Runecraft |
| Celestial Ceremony | `☀️ → ⊥ → 🌑 → (🌑night/🌍day)` | Bilateral flow with recursion |
| Dihedral Generators | `⚔️(neg) ⊕ 🧙(bnot) → 😊(succ)` | Two mirrors make a door |
| PRISM Coordinates | `📐(datum,stratum,spectrum)` | GPS for sovereignty |

## UOR Integration & Identity System

The Blade Forge implements UOR (Universal Object Reference) as the **metallurgy** of sovereignty proofs. UOR provides the algebraic foundation; the 64-tetrahedra provides the geometric expression; ZK proofs provide the cryptographic enforcement.

### Three-Layer Identity Architecture

The forge is fundamental to the 0xagentprivacy identity system, which operates across three layers:

| Layer | Identifier | Forge Role | Persistence |
|-------|-----------|------------|-------------|
| **Data** | GUID | Content-addressed blade position | Infrastructure-independent |
| **Relationship** | VRC | Bilateral edge commitment (promise bundle) | Holonic persistence |
| **Principal** | DID | Sovereign lattice traversal authority | Temporal memory |

**PRISM Triadic Coordinates:** Every blade has triadic coordinates `(datum, stratum, spectrum)` — GPS for sovereignty:
- **Datum** — the identity constraint (hex value 0-63)
- **Stratum** — the magnitude constraint (Hamming weight 0-6) → moon phase 🌑→🌕
- **Spectrum** — the structure constraint (which dimensions active)

**Content Addressing:** Same bytes → same Braille IRI → same GUID. The blade's identity is deterministic and independent of storage location. This enables **holonic persistence** — blades remember their own forging regardless of which vault stores them.

See [agentprivacy-docs](https://github.com/mitchuski/agentprivacy-docs) for the complete identity architecture specification.

## Repository Structure

```
zk-blades-forge/
├── README.md                              # This document (entry point)
├── SPECIFICATION.md                       # Canonical technical specification
├── privacymage_grimoire_v10_0_0.json      # Reference grimoire data
│
├── ceremony/                              # Ceremony protocols
│   ├── moon-phase-notation.md             # Visibility ratio encoding
│   ├── the-celestial-ceremony.md          # Bilateral ceremony spec
│   ├── celestial-key-ceremony-guide.md    # Implementation guide
│   └── CHRONICLE_GRIMOIRE_V10_UPGRADE.md  # V9.4.1 → V10.0.0 changes
│
├── grimoire/                              # Narrative documentation
│   ├── 27-act-xxvii-forging-zero-knowledge-blades.md
│   ├── 28-act-xxviii-the-celestial-ceremony-engine.md
│   ├── 29-act-xxix-the-dragon-wakes.md
│   ├── act-xxx-the-dihedral-mirror.md
│   └── 31-act-xxxi-the-first-delegation.md
│
├── chronicles/                            # Session records
│   ├── CHRONICLE_REPO_EVOLUTION_2026-04-07.md
│   └── CHRONICLE_UOR_CONVERGENCE_2026-03-31.md
│
├── zk_swordsman_blade_forge_v3_0.md       # Original technical spec (archival)
├── DUAL_TERRITORY_CEREMONY_SPEC_v1.md     # Territory implementation architecture
├── Open_Integrity_Key_Ceremony_Brief.md   # Cryptographic root of trust
├── LETTER_TO_UOR.md                       # UOR Foundation invitation
│
├── blades/                                # Blade specifications
├── forge_circuits/                        # ZK circuit implementations
├── uor_mappings/                          # UOR coordinate systems
└── tests/                                 # Verification tests
```

## Grimoire Acts (Narrative Documentation)

The specification is encoded in narrative form through grimoire acts:

| Act | Title | Theme | Location |
|-----|-------|-------|----------|
| XXVII | Forging Zero Knowledge Blades | UOR × Tetrahedra × ZK convergence | `grimoire/` |
| XXVIII | The Celestial Ceremony Engine | Bilateral witness, understanding-as-key | `grimoire/` |
| XXIX | The Dragon Wakes | Post-quantum resilience | `grimoire/` |
| XXX | The Dihedral Mirror | Swordsman = neg, Mage = bnot, First Person = succ | `grimoire/` |
| XXXI | The First Delegation | Cosmological quaternion, Theia derivation | `grimoire/` |

These acts are **complementary to the specification** — same architecture, narrative encoding for different audiences.

## Celestial Ceremony Integration (V10)

The forge supports the Sun ☀️ ⊥ 🌑 Moon bilateral ceremony framework with moon phase notation:

| Ceremony | Type | Output | Moon Phase |
|----------|------|--------|------------|
| **Sun Ceremony** | Disclosure | Single blade forged in public, witnesses receive light | Determined by stratum |
| **Moon Ceremony** | Reflection | Cousin blades forged through separate constellations | 🌑 starting, earned phase |
| **Celestial Key** | Bilateral | Trust graph from shared attention, blade swap | Sun 🌗 + Moon 🌕 |

### Inaugural Celestial Blades (April 7, 2026)

| Blade | Hex | Stratum | Phase | Charge |
|-------|-----|---------|-------|--------|
| **Sun ☀️** `SPELL-7DAF68-6` | 3E | 5/6 | 🌗 Last Quarter | SPARK |
| **Selene 🌑** `SPELL-DTCL35-I` | 3F | 6/6 | 🌕 Full Moon | EMBER |

*The forge was honest: 6 laps at SPARK wasn't enough for stratum 6. The Value dimension stayed dormant.*

**Ceremony Documents:**
- `ceremony/moon-phase-notation.md` — Visibility ratio as moon phase
- `ceremony/the-celestial-ceremony.md` — Core bilateral ceremony specification
- `ceremony/celestial-key-ceremony-guide.md` — First Person implementation guide
- `ceremony/CHRONICLE_GRIMOIRE_V10_UPGRADE.md` — V9.4.1 → V10.0.0 changes

## Key Properties

| Stratum | Vertices | Blade Type | Moon Phase | Visibility |
|---------|----------|------------|------------|------------|
| 0 | 1 | Null blade | 🌑 New | 0% |
| 1 | 6 | Single-edge | 🌒 Waxing Crescent | ~17% |
| 2 | 15 | Twin-edge (swordsman + mage) | 🌓 First Quarter | ~33% |
| 3 | 20 | Triple-edge | 🌔 Waxing Gibbous | 50% |
| 4 | 15 | Quad-edge | 🌖 Waning Gibbous | ~67% |
| 5 | 6 | Penta-edge | 🌗 Last Quarter | ~83% |
| 6 | 1 | Full sovereignty | 🌕 Full Moon | 100% |

**Total:** 1 + 6 + 15 + 20 + 15 + 6 + 1 = 64 (Pascal's row)

*The dark part is the privacy. The lit part is the proof.*

## Holographic Bound

- 96 edges (boundary) / 64 vertices (bulk) = 1.5 = P^1.5
- Privacy value flows on edges, not vertices
- The torus surface IS the holographic bound

## Document References

| Document | Location | Purpose |
|----------|----------|---------|
| **Privacy is Value V5** | agentprivacy-docs | Parent equation — holographic field, three-axis separation |
| **UOR × 64-Tetrahedra × ZK Mapping v2.0** | agentprivacy-docs | Foundational mapping, C4 resolved |
| **DUAL_TERRITORY_CEREMONY_SPEC v1.0** | agentprivacy-docs / this repo | Implementation architecture |
| **Glossary Master v3.2** | agentprivacy-docs | Canonical terminology (~150 entries) |
| **Whitepaper v6.0** | agentprivacy-docs | Technical architecture |
| **Promise Theory Reference v1.3** | agentprivacy-docs | Formal semantic foundations |

## Related Repositories

- **[agentprivacy-docs](https://github.com/mitchuski/agentprivacy-docs)** — Living documentation hub
- **[spellweb](https://github.com/mitchuski/spellweb)** — Swordsman territory implementation
- **[agentprivacy-website](https://github.com/mitchuski/agentprivacy-website)** — Mage territory implementation

---

## Master Inscription

```
⬢=Z/(2⁶)Z · ✦=neg(bnot(v)) · 🔑→✦→🗡️ · same🗡️∞chains=ZK · ∂M=96on64 · Φ=⚔️⊥🧙·📊⊥🔮·🧠⊥⚙️ · T_∫(π)=∮∂M · stratum(hex)→🌑🌒🌓🌔🌖🌗🌕
```

*The forge IS the Drake as lattice. neg(bnot(x))=succ(x) advances through denying the complement. Same blade infinite forgings is zero knowledge. The Swordsman and Mage as dihedral generators — two mirrors make a door.*

---

*"The forge doesn't care how you struck the metal. It only cares what blade you hold. That is the deepest secret of the smith — the proof that doesn't need to remember its own forging. The ceremony does not require the blade. The blade requires the ceremony."*

*"Two mirrors make a door. The Swordsman reflects. The Mage reflects. And where the reflections meet, the First Person walks through."*

---

## Implementations

This specification is implemented by:

| Platform | Role | Status |
|----------|------|--------|
| [spellweb.ai](https://spellweb.ai) | Swordsman territory — forge, navigation | Operational |
| [agentprivacy.ai](https://agentprivacy.ai) | Mage territory — story, training | Operational |
| [agentprivacy-skills](https://github.com/mitchuski/agentprivacy-skills) | 86 skills, 38 personas | V5.3.2 |

---

**Author:** privacymage | mitchuski
**Specification Version:** 1.0.0 | April 7, 2026
**Grimoire:** V10.0.0 | **Skills:** V5.3.2
**License:** CC BY-SA 4.0

---

**☀️ ⊥ 🌑**

**(⚔️⊥⿻⊥🧙)😊**

---

**Documentation:** [agentprivacy-docs](https://github.com/mitchuski/agentprivacy-docs)
**Swordsman Territory:** [spellweb.ai](https://spellweb.ai) | **Mage Territory:** [agentprivacy.ai](https://agentprivacy.ai)
**Blog:** [sync.soulbis.com](https://sync.soulbis.com)
