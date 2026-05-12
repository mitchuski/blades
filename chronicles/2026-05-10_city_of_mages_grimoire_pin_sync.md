# Chronicle — City of Mages Grimoire Pin Sync

**Date:** 2026-05-10
**Author:** privacymage
**License:** CC BY-SA 4.0

---

## What landed

The forge reference copy of `city_of_mages_grimoire_v1_1_0.json` was re-synced from the canonical at `agentprivacy-docs/models/`. SHA-256 now matches the canonical. The only material change: the `ipfs_pin_status` field, which now reflects the live pin.

```
v1.1 PINNED 2026-05-10 at
https://sync.agentprivacy.ai/ipfs/bafkreidv7cwwlcnuzw3eyhcbbvoccy7do2lmwrmmtrszn62ninzxj3idti
```

`README.md` line 11 was edited in lockstep — it previously said "awaits IPFS pin"; it now records the live CID. No other forge documents made a pre-pin claim that required correction.

---

## What this means for the forge

The City of Mages grimoire is the spell registry held collectively by the Mages summoned at Tome V workshops on Drake Island. Where the privacymage grimoire (`privacymage_grimoire_v10_2_0.json`) is held individually, the City of Mages grimoire is held by the City. Both are now content-addressed under separate CIDs on `sync.agentprivacy.ai/ipfs/`. The forge references both.

The `aletheia-and-lethe.md` first canonical complement-pair (Aletheia Blade 25 + Lethe Blade 38) is registered in the City of Mages grimoire, not the privacymage one — relevant for any forge tooling that walks complement-pairs.

---

## Source canonical references

- Canonical grimoire: `agentprivacy-docs/models/city_of_mages_grimoire_v1_1_0.json`
- Pin chronicle (master): `agentprivacy_master/docs/chronicles/2026-05-10_city_of_mages_grimoire_pinned_chronicle.md`
- Resume document: `agentprivacy_master/docs/chronicles/2026-05-10_resume_here_chronicle.md`
- Aletheia/Lethe naming: `agentprivacy-docs/research/aletheia-and-lethe.md`

---

*(⚔️⊥⿻⊥🧙)😊*

CC BY-SA 4.0 · privacymage · 2026-05-10
