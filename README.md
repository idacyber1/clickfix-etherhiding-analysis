# ClickFix + EtherHiding — Campaign Analysis

A defender-focused writeup of a real-world **ClickFix** (fake-CAPTCHA → clipboard command) campaign that stages its payloads via **EtherHiding** (malware hidden in Binance Smart Chain smart contracts), observed in the wild in mid-2026.

## Disclaimer

This repository is published **solely for education, awareness, and defensive security** — to help defenders and users recognize and stop this class of attack.

- Provided **"as is," without warranty** of any kind. You are solely responsible for how you use this material.
- All indicators and commands here are **defanged**, and **no live malware samples are included**. Do **not** re-fang, reconstruct, or execute anything in this repository.
- Do **not** use this material to conduct or facilitate unauthorized access, intrusion, or any unlawful activity. Only act on systems you are authorized to test, and comply with all applicable laws.
- The compromised website referenced in this analysis is an **innocent victim** of the campaign, not a target.
- This is **not** legal or professional security advice. Views are the author's own and do not represent any employer or organization.

## Contents

- **[ClickFix-EtherHiding-Awareness-Article.md](ClickFix-EtherHiding-Awareness-Article.md)** — the narrative walkthrough: how the attack works, stage by stage, and how to protect people. Written for a broad security audience.
- **[ANALYSIS.md](ANALYSIS.md)** — the technical companion: full execution chain, IOCs, EDR/SIEM hunting ideas, and Windows (GPO/ASR) + macOS (MDM/Santa) hardening guidance.
- **[attack-path.svg](attack-path.svg)** / **[attack-path-horizontal.svg](attack-path-horizontal.svg)** — attack-path diagrams.
- **screenshots/** — annotated captures of the live lure (Windows + macOS) and a headless detonation.

## Safety notes

- **All indicators and commands in this repo are defanged** (`example[.]com`, and clipboard commands shown in their real structure but with domains neutered). **Do not re-fang them, and never paste any command into a shell.**
- **No live malware samples are included.** The decoded payloads, raw on-chain responses, and the compromised-site clone are intentionally withheld to avoid redistributing a working attack kit and re-publishing an innocent victim's site. Researchers who need samples should work from an isolated, attributable environment.
- The compromised photography site named in the IOCs is an **innocent victim** of the campaign, not the attacker — it is listed only so others can recognize and help remediate it.

## Purpose

Awareness and detection. The single rule that defeats this entire class of attack: **no legitimate website, CAPTCHA, or error page will ever ask you to press Win + R, open PowerShell/Terminal, or paste a command to "prove you're human."** If something asks you to — stop. It's an attack.

## License

Licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE). You're free to share and adapt with attribution.
