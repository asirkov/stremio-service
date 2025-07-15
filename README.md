# Stremio Service

This project combines three components into one Docker-based setup:

- **Jackett** — torrent indexer proxy, aggregates torrent trackers.
- **Jackett-plugin** — custom backend plugin that queries Jackett and serves results in Stremio-compatible format.
- **Stremio-web** — a copy of the Stremio web client to access the UI.

---

## 📦 Components

### 1. Jackett

Jackett acts as a bridge between the torrent indexers and your plugin, providing torrent metadata via API.

### 2. Jackett Plugin

This is the core backend service which queries Jackett, filters torrents by your configuration, and exposes a Stremio add-on API.

### 3. Stremio-web

A static copy of Stremio web client served via a simple web server, not allowed to stream video, only for viewing or testing.

---

## 🚀 Getting Started

### Requirements

- Docker Compose

---

## ⚙️ Configuration

See: [Jackett Plugin](https://github.com/asirkov/jackett-plugin)

## 🚀 Quick Start

Build and run the services with Docker Compose:

```bash
docker-compose up -d
```

or:

```bash
./start.sh
```
