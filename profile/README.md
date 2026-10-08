# Family TimeCraft

An Open-Source, Privacy-Preserving Digital Wellbeing Platform for Modern Linux

---

## Overview

TimeCraft is a digital wellbeing and screen-time management platform designed specifically for families using Linux desktop environments.

Rather than functioning as restrictive surveillance software or cloud-connected monitoring tools, TimeCraft establishes a transparent partnership between parents and children. It pairs native screen-time awareness with collaborative gamification, allowing children to earn entertainment time and virtual rewards by completing everyday responsibilities such as studies, household chores, and physical activity.

---

## Core Pillars for Families

### 1. Data Sovereignty and Zero-Telemetry Privacy
* **Local-First Storage**: All detailed application usage logs, active window titles, and session histories reside exclusively on your home computer in local SQLite databases.
* **No Cloud Surveillance**: Browsing habits, private window titles, and personal activity logs are never transmitted to corporate servers, commercial analytics platforms, or external clouds.
* **GDPR Privacy by Design**: Fully compliant with European privacy regulations (GDPR Article 25) regarding data minimization for minors.

### 2. Partnership and Positive Reinforcement
* **Collaborative Agreements**: Replaces arbitrary lockouts and secret monitoring with explicit family rules and clear daily allowances.
* **Task Engine and Bonus Time**: Children view their daily checklist and submit tasks for confirmation. Completed tasks immediately unlock bonus screen time.
* **Permanent Coin Economy**: Tasks can also award virtual coins that never expire overnight. Children can save coins in their personal wallet, fostering patience, budgeting skills, and long-term goal setting.

### 3. Seamless Cross-Device Supervision
* **Instant Mobile Companion**: Parents and children can access the platform from any smartphone or tablet via an installable Progressive Web Application (PWA).
* **Stateless Synchronization**: Remote interactions (approving tasks, granting extra time, viewing current status) route through an encrypted, stateless relay. The server acts purely as a real-time router and retains zero personal family data.

---

## Key Features

* **Native Wayland and GNOME Compatibility**: Operates seamlessly within modern Wayland display servers and GNOME Shell on Ubuntu, Fedora, and Debian-based distributions.
* **Intelligent Application Categorization**: Automatically categorizes software into Education, Development, Entertainment, or Gaming using flexible matching rules.
* **Curfew and Schedule Enforcement**: Defines strict quiet hours (such as bedtime or study hours) during which recreational applications are suspended.
* **Parental Security Controls**: Settings and limit modifications are protected by administrative password hashing.
* **Community Presets**: Import curated, community-tested rules for identifying educational tools, popular games, and productivity applications without manual configuration.

---

## Ecosystem Repositories

The platform is maintained as a collection of focused, open-source repositories under the family-timecraft organization:

| Repository | Description | Key Technologies |
| :--- | :--- | :--- |
| **timecraft-desktop-linux** | Primary desktop application, administrative dashboard, and settings interface | Tauri v2, Rust, SolidJS, SQLite |
| **timecraft-wayland-tracker** | Background system service capturing active window sessions on Wayland | Python 3, D-Bus, SQLite (WAL) |
| **gnome-shell-extension-focused-window** | Native GNOME Shell bridge reporting active window metadata to session D-Bus | JavaScript (GJS, ESM), Mutter API |
| **timecraft-relay-server** | Lightweight, stateless WebSocket router for local and remote device synchronization | Bun, Hono, Redis |
| **timecraft-pwa** | Mobile companion web application for parents and children | SolidJS, Vite, WebCrypto, PWA |
| **timecraft-ts-shared** | Shared domain contracts, message envelopes, and schema definitions | TypeScript, Zod |
| **timecraft-community-presets** | Open catalog of application categorization rules and daily schedule templates | JSON Schema, Declarative Rules |

---

## Getting Started

### Desktop Installation

TimeCraft is packaged for Debian and Ubuntu distributions as an all-in-one system package. The installer sets up the desktop user interface, background tracker, and system integrations in a single step:

```bash
# Download the release package
# Install package and system dependencies
sudo apt install ./timecraft_amd64.deb
```

Once installed, launch **TimeCraft** from your system applications menu. Follow the onboarding wizard to configure the administrative parent password and default family schedules.

### Mobile Pairing

To monitor and approve tasks from a smartphone:

1. Open **TimeCraft Desktop** and navigate to the **Connected Devices** section.
2. Select **Pair New Device** to generate a secure, single-use pairing QR code.
3. Open the camera or browser on your mobile device, scan the code, and choose your access mode (Parent or Child).
4. Save the page to your home screen for immediate, full-screen mobile access.

---

## Open Source Licensing

TimeCraft is dedicated to digital sovereignty and user freedom:

* **Desktop Application and Core Services**: Licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)** to protect against proprietary cloud exploitation.
* **GNOME Shell Integration**: Licensed under **GPL-2.0-or-later** in compliance with upstream GNOME Shell standards.
* **Community Presets and Schemas**: Dedicated to the public domain under **MIT / CC0-1.0** for unrestricted sharing and community contribution.
