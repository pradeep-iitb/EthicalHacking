# Ethical Hacking Learning Repository

A structured, notes-first repository for learning cybersecurity and ethical hacking fundamentals through theory, practical concepts, and progressive attack/defense topics.

This repo is organized as a personal learning roadmap with curated markdown notes across networking, attack lifecycle concepts, focused attack techniques, and certification-aligned content.

## Important Disclaimer

This repository is for **educational and defensive security learning** only.

- Use these materials only in legal environments you own or have explicit permission to test.
- Do not perform unauthorized scanning, exploitation, phishing, interception, or data access.
- Always follow local laws, platform policies, and responsible disclosure practices.

## Repository Goals

- Build a strong base in networking and Linux fundamentals.
- Understand the ethical hacking process from reconnaissance to post-exploitation concepts.
- Study common web and network attack patterns to better defend systems.
- Keep certification-oriented study notes in one place (Google + IBM tracks).

## Repository Structure

### Core Files

- [README.md](README.md): Repository overview and usage guide.
- [Roadmap.md](Roadmap.md): High-level cybersecurity and ethical hacking learning roadmap.

### Learning Modules

#### 1) ComputerNetworking

Foundational networking concepts required before security testing.

- [ComputerNetworking/IP Addresses and PORT.md](ComputerNetworking/IP%20Addresses%20and%20PORT.md)
- [ComputerNetworking/Linux.md](ComputerNetworking/Linux.md)
- [ComputerNetworking/Models & Protocols.md](ComputerNetworking/Models%20&%20Protocols.md)
- [ComputerNetworking/Types of network & Topologies.md](ComputerNetworking/Types%20of%20network%20&%20Topologies.md)
- [ComputerNetworking/Virtual Machines & Labs.md](ComputerNetworking/Virtual%20Machines%20&%20Labs.md)

#### 2) EthicalHackingBegins

Step-by-step beginner-to-intermediate ethical hacking concepts and methods.

- [EthicalHackingBegins/1. CyberKillChain.md](EthicalHackingBegins/1.%20CyberKillChain.md)
- [EthicalHackingBegins/2. Reconnaissance.md](EthicalHackingBegins/2.%20Reconnaissance.md)
- [EthicalHackingBegins/3. Scanning.md](EthicalHackingBegins/3.%20Scanning.md)
- [EthicalHackingBegins/4. Exploitation.md](EthicalHackingBegins/4.%20Exploitation.md)
- [EthicalHackingBegins/5. PasswordsAttacks.md](EthicalHackingBegins/5.%20PasswordsAttacks.md)
- [EthicalHackingBegins/6. Burpsuite.md](EthicalHackingBegins/6.%20Burpsuite.md)
- [EthicalHackingBegins/7. BeingAnonymous.md](EthicalHackingBegins/7.%20BeingAnonymous.md)
- [EthicalHackingBegins/8. PortForwarding&SocialEngineering.md](EthicalHackingBegins/8.%20PortForwarding&SocialEngineering.md)
- [EthicalHackingBegins/9. SQL_Injection&XSS_Scripting.md](EthicalHackingBegins/9.%20SQL_Injection&XSS_Scripting.md)
- [EthicalHackingBegins/10. DDOS_Attacks.md](EthicalHackingBegins/10.%20DDOS_Attacks.md)
- [EthicalHackingBegins/11. LoginPhishing.md](EthicalHackingBegins/11.%20LoginPhishing.md)
- [EthicalHackingBegins/12. Wireshark.md](EthicalHackingBegins/12.%20Wireshark.md)

#### 3) FocusedAttacks

Deep dives into selected attack themes.

- [FocusedAttacks/MITMAttack.md](FocusedAttacks/MITMAttack.md)
- [FocusedAttacks/OSINT.MD](FocusedAttacks/OSINT.MD)
- [FocusedAttacks/SessionHijacking.md](FocusedAttacks/SessionHijacking.md)

#### 4) Certification Notes

Certification-linked notes for structured study.

Google Cybersecurity:

- [GoogleCertfication/CybersecurityTerminology.md](GoogleCertfication/CybersecurityTerminology.md)
- [GoogleCertfication/Module1.md](GoogleCertfication/Module1.md)
- [GoogleCertfication/Module2.md](GoogleCertfication/Module2.md)
- [GoogleCertfication/Module3.1.md](GoogleCertfication/Module3.1.md)
- [GoogleCertfication/Module3.2.md](GoogleCertfication/Module3.2.md)
- [GoogleCertfication/Module4.md](GoogleCertfication/Module4.md)
- [GoogleCertfication/Module5.md](GoogleCertfication/Module5.md)
- [GoogleCertfication/Module6.md](GoogleCertfication/Module6.md)

IBM Security Fundamentals:

- [IBMCertification/1. Introduction.md](IBMCertification/1.%20Introduction.md)
- [IBMCertification/2. Common Security Threats & Risks.md](IBMCertification/2.%20Common%20Security%20Threats%20&%20Risks.md)
- [IBMCertification/3. Best Security Practices.md](IBMCertification/3.%20Best%20Security%20Practices.md)
- [IBMCertification/4. Safe Browsing.md](IBMCertification/4.%20Safe%20Browsing.md)

## Suggested Learning Path

If you are new, follow this sequence:

1. Start with [Roadmap.md](Roadmap.md) for the big picture.
2. Complete the networking and Linux notes in [ComputerNetworking](ComputerNetworking).
3. Move through [EthicalHackingBegins](EthicalHackingBegins) in numeric order (1 -> 12).
4. Read focused deep-dives in [FocusedAttacks](FocusedAttacks).
5. Use [GoogleCertfication](GoogleCertfication) and [IBMCertification](IBMCertification) for certification prep and revision.

## How To Use This Repository

- Treat each markdown file as a focused study unit.
- Take your own notes, command references, and lab observations as you go.
- Practice only in legal labs (local VMs, CTF platforms, intentionally vulnerable apps).
- Revisit earlier topics regularly; security learning is cumulative.

## Recommended Practice Setup

- Host OS with enough RAM/CPU for virtual labs.
- Linux VM for command-line and tooling practice.
- Isolated lab network for testing.
- Safe targets such as DVWA, Metasploitable, or CTF environments.

## Contributing

Contributions are welcome to improve clarity, structure, and correctness.

Typical contribution ideas:

- Fix typos and improve explanations.
- Add diagrams or examples to existing topics.
- Add references to official documentation and standards.
- Improve module ordering and cross-links between notes.

Suggested flow:

1. Fork the repository.
2. Create a feature branch.
3. Make focused changes.
4. Open a pull request with a clear summary.

## Future Improvements

- Add a dedicated labs folder with legal, sandbox-only walkthrough templates.
- Add an index page per module with estimated study time.
- Add short quizzes/checklists for revision.
- Add a glossary with linked terms across all notes.

## License

No license file is currently defined in this repository.
If you want to allow reuse, add a standard license such as MIT or Apache-2.0.
