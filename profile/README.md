# Bastion

**A self-hosted, phone-first control panel for your home server, with an open marketplace of add-ons.**

Bastion shows what your machine is doing and lets you act on it safely: containers, storage, backups, network,
updates. Everything beyond that is an add-on you pick: media, dev boxes, notes, local AI, finders, finance,
game servers, themes, or something you build yourself and share with everyone.

<p align="center">
  <img src="https://github.com/bastionlab/core/raw/main/docs/screenshots/home-desktop.webp" alt="Bastion Home on a desktop" width="100%">
</p>
<p align="center">
  <img src="https://github.com/bastionlab/core/raw/main/docs/screenshots/home-phone.webp" alt="Home on a phone" width="24%">
  <img src="https://github.com/bastionlab/core/raw/main/docs/screenshots/metrics-phone.webp" alt="Metrics on a phone" width="24%">
  <img src="https://github.com/bastionlab/core/raw/main/docs/screenshots/addons-phone.webp" alt="The add-on marketplace" width="24%">
  <img src="https://github.com/bastionlab/core/raw/main/docs/screenshots/hero.gif" alt="Moving through the app on a phone" width="24%">
</p>

**Try it without a server:** `git clone https://github.com/bastionlab/core && cd core && demo/run`, then open
http://127.0.0.1:3000 (Node 22, sample data).

## Why Bastion

- **Small core, open marketplace.** The core is Home, Metrics, Add-ons and Settings. Every other feature is an
  add-on you install, update, switch off or remove from the dashboard.
- **Same logic, your own setup.** Everyone shares the core and the marketplace. Which add-ons you run, your
  layout, your data and your secrets never leave your machine.
- **You confirm every change.** Actions are shown as exactly what will run before you press Run. A local
  model can suggest them in plain words; it can never run one by itself.
- **Made for the phone.** An installable web app with push notifications, over Tailscale or your home network.
- **Private by default.** No telemetry, no cloud account, no vendor in the middle.

## Get started

On a Proxmox VE host, as root:

```sh
curl -fsSL https://raw.githubusercontent.com/bastionlab/core/main/install.sh | bash
```

Then open `https://dash.<your-tailnet>/`, unlock with the PIN you chose, and browse the Add-ons page.
Requirements, an unattended mode and moving to a new host: [core README](https://github.com/bastionlab/core#install).

Bastion runs on Proxmox VE today. Plain Linux hosts with Docker are on the
[roadmap](https://github.com/bastionlab/core#roadmap).

## Repositories

| Repository | What it is |
|---|---|
| [**core**](https://github.com/bastionlab/core) | The dashboard: web app, host agent, installer, add-on SDK and template |
| [**addons**](https://github.com/bastionlab/addons) | The marketplace: add-ons, skins, widget packs and designs |
| [**deals**](https://github.com/bastionlab/deals) | Backend for the Deals, Flats and Jobs finder add-ons |
| [**money**](https://github.com/bastionlab/money) | Backend for the Money add-on (Firefly III and bank sync) |

## Contribute

**Build an add-on, skin or design.** Generate one with `templates/new-addon <id> "<Name>"`, develop it live on
your own install, then press Publish. An automatic check covers ownership, malware, leaked secrets, style and
lint; when it is green your add-on goes live for everyone within minutes. You can only publish and update your
own work. Guide: [Building an add-on](https://github.com/bastionlab/addons#building-an-add-on).

**Improve the core.** Fixes and improvements to the dashboard, agent and installer go through pull requests to
[core](https://github.com/bastionlab/core). New features usually belong in an add-on. Guide:
[CONTRIBUTING.md](https://github.com/bastionlab/core/blob/main/CONTRIBUTING.md). Sign-off (DCO), no CLA.

**Report and discuss.** Bugs and ideas: [core issues](https://github.com/bastionlab/core/issues). Security
problems: privately, see [SECURITY.md](https://github.com/bastionlab/core/blob/main/SECURITY.md).

## Good to know

- The host agent runs as root. Every change waits for your confirmation, but there is no warranty: keep backups.
- Some add-ons use unofficial APIs or sites whose terms forbid automated access. They say so before install and
  are meant for personal use.
- The core is licensed under [AGPL-3.0](https://github.com/bastionlab/core/blob/main/LICENSE); add-ons choose
  their own license.
- Not affiliated with Proxmox Server Solutions GmbH.
