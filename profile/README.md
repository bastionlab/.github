# Bastion

**A phone-first dashboard for your Proxmox home server.** See what the host is doing, open the apps you run on
it and take the actions you need, from one installable web app. Everything beyond the core is an add-on you
switch on, install or remove from the dashboard itself.

- **Home, Metrics, Add-ons, Settings** in the core: app tiles with health checks, host/GPU/disk/backup metrics,
  container and tailnet status
- **Actions with a confirm step**: every change shows exactly what will run before you press Run
- **Add-on marketplace**: install, update or remove from the dashboard; each install is scanned first
- **Private by default**: runs on your tailnet and home LAN, own accounts (password, passkey, TOTP) with roles,
  no telemetry
- **Optional AI**: a local model (Ollama) that proposes actions, and Claude Code on the host

```sh
curl -fsSL https://raw.githubusercontent.com/bastionlab/core/main/install.sh | bash
```

## Repositories

- [**core**](https://github.com/bastionlab/core): the dashboard (Nuxt app + host agent) and the installer
- [**addons**](https://github.com/bastionlab/addons): the marketplace, one folder per add-on
- [**habits**](https://github.com/bastionlab/habits): offline-first habit tracker behind the Habits add-on
- [**deals**](https://github.com/bastionlab/deals): backend for the Deals, Flats and Jobs finders
- [**money**](https://github.com/bastionlab/money): Firefly III + bank sync behind the Money add-on

Core is AGPL-3.0; each add-on picks its own license. Not affiliated with Proxmox Server Solutions GmbH.
Security issues: see [SECURITY.md](https://github.com/bastionlab/core/blob/main/SECURITY.md).
