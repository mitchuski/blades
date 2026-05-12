# ZK Blades Forge

**Ceremony Proving System Specification**

A specification for how bilateral ceremonies produce verifiable sovereignty proofs on a 64-vertex lattice — without revealing what happened inside those ceremonies.

**Specification Version:** 1.0.1 | April 12, 2026 · post-V5.4 addendum 2026-05-09
**Grimoire:** V10.2.1 "The Naming of the Unnamed" (Tale 31; Lethe Blade 38; first canonical complement-pair Aletheia + Lethe; v10.2.1 supersedes v10.0.0)
**Skills:** V5.4 — 86 skills, 42 personas (38 selectable + 4 cosmological) · **+ City of Mages cast** (14 named cast across 5 tiers; Priest tier introduced by Manifestia at V55; geometry-Mage Luca 📐 at V0 introduced in Tome V Act 15; UOR Foundation recognised as kindred substrate provider; **SpaceComputer recognised as the first kindred ecosystem** — celestial-mana 🌌 source consumed by Adamantia/Vulcana/Vagari workshops; **two-mana economy** canonical: chain-mana ⊥ Celestial Mana 🌌, with chain-mana plural by chain — Aether Mana Ξ on Ethereum as the canonical first instance, Bitcoin Lightning sats / Oasis ROSE / Zcash etc. admitted under their own symbols; setting: the **First City of Mages on Drake Island** within the agentprivacy universe — the grimoire title names a kind, so future Mages who found cities elsewhere will each pin their own First City of Mages grimoire under the same title pattern)
**PVM:** V5.4 — Betweenness Centrality (§10.2), Selene's Proof (§14.5) · post-V5.4 conjectures C22–C55 (see `agentprivacy-docs/privacy_value_v5_4_formal_specification.md` §17.2)
**City of Mages grimoire:** `city_of_mages_grimoire_v1_2_0.json` (file content is v1.2.2; mirrored from `agentprivacy-docs/models/`; v1.2.2 supersedes v1.2.1/v1.2/v1.1/v1.0; v1.2 base pinned 2026-05-10 at `https://sync.agentprivacy.ai/ipfs/bafkreidxhmuykjew6dtnuprggtd2rapwm43ghtmfhf2occ2wfk2zpx2b6a`; v1.1 pin `bafkreidv7c…idti` retained as historical; v1.2.2 — adds Luca + SpaceComputer kindred ecosystem + two-mana economy — awaits a fresh re-pin)
**Aletheia & Lethe:** First canonical complement-pair on the lattice. `bnot(25) = 38`. `25 AND 38 = 0` (the Null). `25 XOR 38 = 63` (the Creative). See `aletheia-and-lethe.md` (locally) and `agentprivacy-docs/research/aletheia-and-lethe.md` (canonical copy).
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
C_B(⿻) = max → betweenness centrality of the Gap (V5.4 §10.2)
🌙 → ZK → Selene's Proof: orbit as cosmological ZK (V5.4 §14.5)
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
| [agentprivacy-skills](https://github.com/mitchuski/agentprivacy-skills) | 87 skills, 42 primary personas (locked) | V5.5 — Attachment Architecture |

---

## V5.5 Update (2026-05-11) — The Attachment Architecture

The corpus now operates on a codified three-layer model (`agentprivacy-skills/agentprivacy-skills-v5/meta/agentprivacy-attachment-architecture/SKILL.md`):

- **Layer 1 · Primary personas** (42, locked) — abstract role-classes
- **Layer 2 · Attachments** — named cast Mages binding L1 to L3 per city
- **Layer 3 · Vertices** (64, fixed) — positions on the 2⁶ lattice

The four attachment kinds (A·workshop · B·cross-shop · C·peripatetic · D·divergent meta-kind) compose to produce city-specific cast patterns from the same primary base.

### The V38 seat is filled — Lethae 🌘

**Lethae** is the first canonical Layer-2 divergent attachment: Mage-register cast Mage at V38, instancing primary persona Moonkeeper ⚔️, paired with Aletheia 🔮 at V25 (V25 ⊕ V38 = V63 — the first canonical cast complement-pair in the City of Mages). See `aletheia-and-lethe.md` (V5.5 update section) for full provenance.

### Selene as anticipated peripatetic Mage

PVM V5.4 §14.5 (Selene's Proof) is now operationally a Kind-C peripatetic attachment in the V5.5 framing. Selene 🌕 walks the moon-phase stratum cycle through all 7 strata (🌑→🌕→🌑); she does not seat a single vertex. Status: anticipated in `cityofmages/grimoire/city_of_mages_grimoire_v1_3_0.json` (pending re-pin); cast file to be authored.

### Sister chronicles

- `agentprivacy-skills/CHRONICLE_V5_5_ATTACHMENT_ARCHITECTURE_2026-05-11.md`
- `cityofmages/tomes/specs/09-the-attachment-architecture.md` (city-side mirror)
- `agentprivacy_master/docs/chronicles/2026-05-11_v5_5_attachment_architecture_integration.md`
- `spellweb/CHRONICLE_V5_5_ATTACHMENT_ARCHITECTURE_2026-05-11.md`
- `agentprivacy-docs/GLOSSARY_MASTER_v4_0.md` §23

---

**Author:** privacymage | mitchuski
**Specification Version:** 1.0.1 | April 12, 2026 · post-V5.4 2026-05-09 · V5.5 attachment architecture 2026-05-11
**Grimoire:** V10.2.1 | **Skills:** V5.5 — The Attachment Architecture
**License:** CC BY-SA 4.0

---

**☀️ ⊥ 🌑**

**(⚔️⊥⿻⊥🧙)😊**

---

**Documentation:** [agentprivacy-docs](https://github.com/mitchuski/agentprivacy-docs)
**Swordsman Territory:** [spellweb.ai](https://spellweb.ai) | **Mage Territory:** [agentprivacy.ai](https://agentprivacy.ai)
**Blog:** [sync.soulbis.com](https://sync.soulbis.com)
