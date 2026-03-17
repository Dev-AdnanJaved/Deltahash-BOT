# Deltahash BOT

An automated Python bot for mining $DTH tokens and managing multiple accounts on the Deltahash platform.

## Overview

- **Language:** Python 3.12
- **Type:** CLI bot (no frontend/web UI)
- **Main file:** `bot.py`

## Features

- Automated $DTH mining
- Multi-account management via `cookies.txt`
- Optional proxy support (HTTP, HTTPS, SOCKS4, SOCKS5) via `proxy.txt`
- Smart proxy rotation
- Social task automation (Follow X, Join Telegram)

## Dependencies

- `aiohttp==3.11.10` - Async HTTP client
- `aiohttp-socks==0.9.1` - SOCKS proxy support for aiohttp
- `colorama==0.4.6` - Colored terminal output

## Configuration

### cookies.txt
Add one cookie string per line (obtained from the Deltahash portal after logging in with your X account).

### proxy.txt (optional)
Add proxies one per line. Supported formats:
- `192.168.1.1:8080` (HTTP by default)
- `http://192.168.1.1:8080`
- `socks5://192.168.1.1:8080`
- `http://user:pass@192.168.1.1:8080`

## Running

The workflow runs `python bot.py` and displays in the console. On startup, you'll be prompted to:
1. Choose proxy mode (with/without proxy)
2. If using proxy, choose whether to enable auto-rotation of invalid proxies

## Workflow

- **Start application** — runs `python bot.py` as a console process
