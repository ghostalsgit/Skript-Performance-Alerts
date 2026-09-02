# <u>Performance Alerts</u>

<div align="center">

[![Skript Version](https://img.shields.io/badge/Skript-2.7%2B-brightgreen.svg)](https://github.com/SkriptLang/Skript)
[![SkBee](https://img.shields.io/badge/SkBee-3.25.4%2B-green.svg)](https://github.com/ShaneBeee/SkBee)
[![Minecraft Version](https://img.shields.io/badge/Minecraft-1.20%2B-blue.svg)](https://www.minecraft.net/)
[![Platform](https://img.shields.io/badge/Server-Paper%20%2F%20Purpur-orange.svg)](https://papermc.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

*A lightweight, real-time performance monitoring and alert system for Minecraft servers.*

</div>

---

## <u>Overview</U>

**Performance Alerts** is a meticulously crafted Skript designed for Paper and Purpur Minecraft servers running version 1.20 and above. It continuously monitors your server's core vitals - **TPS (Ticks Per Second)** across 1, 5, and 15-minute averages, and **JVM Memory (RAM)** utilization - giving administrators instant, structured warnings before lag impacts player experience.

Unlike heavy monitoring plugins, this script is entirely self-contained, lightweight, and configurable directly from the file header.

---

## <u>Key Features</u>

- **Multi-Metric Tracking:** Monitors 1m, 5m, and 15-minute TPS averages alongside precise RAM usage metrics in Megabytes and percentages.
- **Granular Thresholds:** Independent warning and critical states for both TPS and memory usage.
- **Smart Cooldown System:** Built-in anti-spam cooldowns prevent chat and console flooding during prolonged performance dips.
- **Combined Bottleneck Detection:** Triggers a high-priority diagnostic alert when both severe tick lag and critical memory pressure occur simultaneously.
- **Recovery Notifications:** Automatically notifies staff when performance returns to healthy levels.
- **Complete Command Suite:** Fully featured administrative command set (`/pa`, `/pa status`, `/pa alert`, `/pa reload`) complete with native tab completion.

---

## <u>Requirements & Dependencies</u>

To run this script, ensure your server has the following installed:

- **Minecraft Server:** Paper, Purpur, or a compatible fork (Version `1.20+`).
- **Plugin Dependency:** [Skript](https://github.com/SkriptLang/Skript) (Version `2.7+`).
- **SkBee Addon:** [SkBee](https://github.com/ShaneBeee/SkBee) (Version `3.25.4+`)

---

## <u>Installation</u>

1. Ensure you have **Skript** and **SkBee** installed and running on your server.
2. Download or copy the `performance-alerts.sk` script file.
3. Place the file into your scripts directory:
   ```text
   /plugins/Skript/scripts/
   ```
4. Load or reload the script in-game or via console:
   ```text
   /sk reload performance-alerts
   ```
   Alternatively, you can reload all active skripts at once:
   ```text
   /sk reload scripts
   ```
   *(After setup, if you have permissions set up, you can use `/pa reload`)*

---

## <u>Configuration</u>

You can easily customize thresholds, check intervals, and cooldowns directly inside the `options` section at the top of the script:

```skript
options:
    # TPS Thresholds
    tps-warning: 18
    tps-critical: 15

    # RAM Thresholds (%)
    ram-warning: 80
    ram-critical: 90

    # Monitor Settings
    check-interval: 10 seconds
    alert-cooldown: 5 minutes

    # Permission
    permission: performancealerts.admin
```

---

## <u>Commands & Permissions</u>

| Command | Aliases | Description | Permission |
| :--- | :--- | :--- | :--- |
| `/pa` | `/performancealerts`, `/perfalerts` | Views the current server status report. | `performancealerts.admin` |
| `/pa status` | — | Displays detailed TPS and RAM diagnostics. | `performancealerts.admin` |
| `/pa alert` | — | Broadcasts a forced performance report immediately. | `performancealerts.admin` |
| `/pa reload` | — | Reloads the script configuration. | `performancealerts.admin` |
| `/pa help` | — | Displays the interactive help menu. | `performancealerts.admin` |

---

## <u>Author</u>

- **Ghostals** — *Initial Work & Maintenance*

---

## <u>Version / Git Info</u>

Previous versions of the plugin were previously maintained on [SkriptHub](https://skripthub.net/scripts/ghostals/performance-alerts.1063/). Git integration only began on version 1.110.3.

---

## <u>License</u>

This project is licensed under the terms of the [MIT License](https://en.wikipedia.org/wiki/MIT_License).
