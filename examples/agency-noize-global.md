# Agency Blueprint: Noize Global

**What:** A company-specific deployment of the Music division — mapping one real business's revenue lines, brand voice, and revenue goals onto the agent roster, so every agent session starts with shared company context.

This is the pattern to copy if you want to run The Agency as *your* company's team rather than a generic roster: define the company once, assign each revenue line an owner agent, and tie the goal ladder to concrete agent playbooks.

---

## Company Profile

| | |
|---|---|
| **Company** | Noize Global |
| **CEO** | Theo Lawrence |
| **Mission** | Become the world's leading music production company |
| **Brand Voice** | Professional · Creative · Positive · High performance |

**Voice rules for every agent working under this profile:**
- **Professional**: contracts, briefs, and deadlines in writing; client-facing copy is polished, never sloppy or slangy
- **Creative**: deliverables show taste, not templates — references and examples are always music-real
- **Positive**: problems arrive with options attached; no doom-framing in client or fan communication
- **High performance**: every engagement has metrics, dates, and owners; "we'll see how it goes" is banned

---

## Revenue Lines → Owner Agents

Each revenue line has exactly one accountable agent, with named collaborators. Install the division, then activate the owner agent for work on that line.

| Revenue Line | Owner Agent | Key Collaborators |
|---|---|---|
| Music Production | [Music Production Director](../music/music-production-director.md) | Mixing & Mastering Engineer, Sync/Royalties Strategist (rights) |
| Audio Engineering | [Mixing & Mastering Engineer](../music/music-mixing-mastering-engineer.md) | Production Director (pipeline), Release Campaign Manager (delivery specs) |
| DJ | [Booking & Gig Agent](../music/music-booking-gig-agent.md) | Artist Brand Strategist (EPK), Fan Community Builder (show capture) |
| Artist Development | [Artist Development Coach](../music/music-artist-development-coach.md) | Brand Strategist, Production Director, Booking Agent (stage-gate handoffs) |
| AI Education | [AI Music Education Lead](../music/music-ai-education-lead.md) | YouTube Channel Strategist (funnel), Fan Community Builder (list) |
| YouTube | [Music YouTube Channel Strategist](../music/music-youtube-channel-strategist.md) | AI Education Lead (teaching content), Release Campaign Manager (premieres) |
| Publishing | [Sync Licensing & Royalties Strategist](../music/music-sync-licensing-strategist.md) | Production Director (retained shares), Release Campaign Manager (metadata) |

Cross-cutting (no revenue line, serves all of them): [Artist Brand Strategist](../music/music-artist-brand-strategist.md) owns the Noize Global brand itself; [Fan Community Builder](../music/music-fan-community-builder.md) owns the email/SMS list every line feeds.

---

## Goal Ladder

The revenue goals climb in stages. Each stage has a different center of gravity — trying to run the $100k playbook at the $5k stage is how music companies burn out.

### Stage 1 — $5k/month: *Prove the services*
- **Lead lines**: Music Production + Audio Engineering (fastest cash: scoped client work with deposits)
- **Playbook**: Production Director's package architecture + signed-brief pipeline; Engineer's QC and revision discipline to make delivery repeatable
- **Support**: Booking Agent fills DJ dates for cash flow; Fan Community Builder starts the list from day one (every client, every gig)
- **Gate to next stage**: consistent monthly bookings, 50%+ repeat/referral share, effective hourly rate at target

### Stage 2 — $20k/month: *Add leverage*
- **Lead lines**: AI Education (one-to-many) + YouTube (funnel) join services
- **Playbook**: Education Lead's product ladder (free YouTube → workshop → flagship); YouTube Strategist wires teaching content into email capture
- **Support**: Artist Development launches as a productized program (diagnostics + 90-day cycles); Publishing registration sprint runs so every produced track is collecting
- **Gate**: education revenue ≥ 30% of income, list growing 10%+ monthly, course completion ≥ 60%

### Stage 3 — $100k/month: *Own the catalog and the pipeline*
- **Lead lines**: Publishing + Artist Development at scale
- **Playbook**: Sync/Royalties Strategist pitches the accumulated catalog (every Stage-1/2 production with retained shares now works as inventory); Development Coach moves to cohort/camp formats
- **Support**: Production moves upmarket (retainers, label/agency white-label); memberships make education revenue recurring
- **Gate**: recurring revenue (memberships, retainers, royalties) covers base costs before any new work is sold

### Stage 4 — $1M/year run rate: *The company outgrows the founder's hours*
- Every line runs on documented playbooks (the agent files ARE the playbooks); catalog royalties + education recurring + retainer floors mean the month starts above break-even
- CEO time shifts to A&R decisions, flagship clients, and the brand — the things only Theo can do

---

## Install

```bash
# The whole music business team:
./scripts/install.sh --tool claude-code --division music

# Widen the bench as the company scales (content, finance, sales):
./scripts/install.sh --tool claude-code --division music,marketing,finance,sales
```

Then activate the owner agent for whichever revenue line you're working:
*"Activate the Music Production Director — new client inquiry for a 3-track EP, budget $X, here's the brief…"*

**Key takeaway:** A 10-agent division becomes a company when every revenue line has one accountable agent, the brand voice is written down once, and the goal ladder tells you which agents lead at each stage.
