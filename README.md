# 🛡️ Firewall Academy

A hands-on, interactive web app that teaches network security and firewalls — from "what's a firewall?" all the way to security-engineer thinking — built around **[OPNsense](https://opnsense.org/)**, the leading open-source firewall.

No accounts, no servers, no build step. One HTML file that runs entirely in your browser and saves your progress locally.

> **Live demo:** _enable GitHub Pages (see below), then your app will be live at_ **https://firmvision.github.io/firewall-academy/**

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Made with HTML/CSS/JS](https://img.shields.io/badge/Made%20with-HTML%20%C2%B7%20CSS%20%C2%B7%20JS-blue.svg)
![No dependencies](https://img.shields.io/badge/dependencies-none-brightgreen.svg)

---

## ✨ Features

- **A complete learning path** — 5 modules, 13 lessons, 51 quiz questions, and a 49-term searchable glossary.
- **Beginner → Pro progression** — start with how networks and firewalls actually work; finish with the mental models, kill-chain thinking, and career roadmap of a security engineer.
- **OPNsense-focused** — every hands-on walkthrough (install, rules, NAT, WireGuard VPN, Suricata IDS/IPS, VLAN segmentation, traffic shaping) uses the real OPNsense workflow.
- **Quizzes that gate progress** — each lesson ends with a check-yourself quiz; answers come with explanations.
- **Progress that persists** — completed lessons, quiz scores, and your progress bar are saved in `localStorage`.
- **Zero dependencies** — pure HTML/CSS/JS in a single file. Works offline. Loads instantly.

## 📚 Curriculum

| # | Module | Level | Covers |
|---|--------|-------|--------|
| 1 | How Networks & Firewalls Work | Foundations | Stateful inspection, IP/ports/CIDR, NAT, default-deny, defense in depth |
| 2 | Installing OPNsense | Foundations | Hardware choices, install walkthrough, interface assignment, first login |
| 3 | Rules, NAT & VPN | Core Skills | Rule order, aliases, port forwarding, WireGuard remote access |
| 4 | IDS/IPS, Segmentation & Shaping | Advanced | Suricata, VLANs, FQ-CoDel/QoS, HA (CARP), logs & SIEM |
| 5 | From Hobbyist to Professional | Pro / Career | CIA triad, Zero Trust, the kill chain, home-lab portfolio, certifications |

## 🚀 Getting started

### Run it locally

Clone the repo and open the file — that's it.

```bash
git clone https://github.com/firmvision/firewall-academy.git
cd firewall-academy
# then open index.html in your browser (double-click, or:)
#   macOS:  open index.html
#   Linux:  xdg-open index.html
#   Windows: start index.html
```

No web server is required, but if you prefer one:

```bash
python3 -m http.server 8000
# visit http://localhost:8000
```

### Host it free on GitHub Pages

1. Push this repo to GitHub (it must contain `index.html` at the root).
2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Select the **`main`** branch and the **`/ (root)`** folder, then **Save**.
5. Wait ~1 minute. Your app goes live at `https://firmvision.github.io/firewall-academy/`.

## 🧩 How it's built

Everything is in **`index.html`**. The course content is data-driven — two JavaScript objects hold all of it:

- `CURRICULUM` — modules, lessons, lesson content, and quiz questions.
- `GLOSSARY` — the reference terms.

A small rendering engine reads from those objects, so adding a lesson or quiz question is mostly editing data, not logic. See [CONTRIBUTING.md](CONTRIBUTING.md).

## 🗺️ Roadmap ideas

- A printable cheat-sheet (key ports, commands, GUI paths).
- A guided "build your first segmented home lab" project track.
- Diagrams for each module (network topology, packet flow).
- Optional dark/light theme toggle.

## 🤝 Contributing

Contributions, corrections, and new quiz questions are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## ⚠️ Disclaimer

This is an educational resource. Firewall and OPNsense behavior evolves; always verify against the [official OPNsense documentation](https://docs.opnsense.org/) before relying on a configuration in production. Practice in a VM or lab, not on a live network you can't afford to break.

## 📄 License

[MIT](LICENSE) © 2026 Oluwafemi Akolade
