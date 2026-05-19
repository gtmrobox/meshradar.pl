# Mesh Radar — Live Meshtastic Network Map

**meshradar.pl** — Real-time map and monitoring dashboard for the Meshtastic LoRa mesh network, focused on Poland and Central/Eastern Europe.

## Overview

Mesh Radar collects, decrypts and visualizes packets from the Meshtastic mesh network in real time. It aggregates data from multiple MQTT brokers and serves it to a live web map with WebSocket updates.

## Features

- **Live map** with Leaflet.js + MarkerCluster — nodes update in real time via WebSocket
- **Node detail panel** — neighbors, RF links, telemetry (battery, voltage, environment), recent messages
- **Multi-broker collection** — loranet.pl, mqtt.meshtastic.org, liamcottle.net mirror, local broker
- **AES decryption** of Meshtastic encrypted packets
- **Redis cache** — all API endpoints cached, zero DB reads on repeated requests
- **PWA** — installable on mobile

## Tech Stack

- **Backend:** Python
- **Database:** MariaDB
- **Cache / Pub-Sub:** Redis
- **Meshtastic:** official `meshtastic` Python library + protobuf definitions
- **Frontend:** Vanilla JS, Leaflet 1.9.4, Socket.IO

---

> This project is not affiliated with the official Meshtastic project. Live instance: [meshradar.pl](https://meshradar.pl)
