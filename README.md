# Hi, I'm AJ

I build defenses for systems that matter, and more and more that means AI systems.

I'm the cofounder and CTO of **Aether Security**, a CMMC Third-Party Assessment Organization (C3PAO), where I build and run the technical environment our assessment work depends on. I'm finishing a master's in information security engineering at the **SANS Technology Institute**, and I'm headed toward a doctorate in AI security.

**What I'm working on**

- Detection engineering for AI agents: turning what coding agents actually do on a machine into SIEM alerts
- Research on whether AI-written detection rules can catch poisoned AI tools
- Open-source security tools, each proven in a live lab before release

---

## Projects

My repositories are private while I finish them. Each one goes public with its tests and lab evidence.

### Wazuh detections for Claude Code
*Detection rules for AI coding agent activity · public release coming*

- A lightweight hook records every tool call Claude Code makes, and 26 Wazuh detection rules, mapped to MITRE ATT&CK where a technique fits, flag the risky ones: credential access, download-and-run, persistence, tampering with the agent's own guardrails, and new MCP servers.
- Every rule is tested in CI against a real Wazuh manager, with an attack case and a harmless look-alike (106 cases), then proven in a live lab with real Claude Code sessions.
- The lab caught what unit tests could not: Wazuh was silently dropping a new user's first events. Fixed before release.

`Python` `Wazuh` `MITRE ATT&CK` `Docker` `GitHub Actions`

### Can AI watch AI?
*Master's research, SANS Technology Institute · paper in progress*

- An AI agent's tool activity streams into Wazuh, and an AI rule-writer proposes detection rules as structured specs. Code renders and validates each rule, deploys high-confidence rules automatically, and queues the rest for blind human review.
- The study tests whether those rules catch poisoned MCP tools, using the MCPTox tool-poisoning benchmark.

`Python` `Wazuh` `MCP` `Ollama` `Claude`

### TARS
*A working TARS from Interstellar · public release coming*

- Wake-word voice conversation with a local AI model and a TARS-style voice, plus a face display with eyes, live captions and visible moods.
- Sees the room: camera vision with Hailo-accelerated person detection. TARS greets people as they arrive, and over Bluetooth switches the lights on when someone walks in and off when the room empties.
- Personality dials for trust and discretion, and long-term memory. Everything runs locally, with no cloud services.

`Python` `FastAPI` `Ollama` `Raspberry Pi 5` `Hailo`

### knowledge-drop
*Drop files in a folder, run one command, read them in your knowledge graph · public release coming*

- Turns recordings, slide decks and PDFs into clean Markdown pages that record where each one came from. Transcription runs on the device, so audio never leaves the machine.
- Deterministic and lossless: no AI calls in the tool itself, originals kept, and every file reported, so nothing is silently dropped.

`TypeScript` `Bun` `mlx-whisper`

---

**How I build:** tests that run against the real thing, honest limits in the README, and evidence that it works before I call it done.
