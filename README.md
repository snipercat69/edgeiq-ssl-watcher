# 🔒 EdgeIQ SSL Watcher

**Monitor SSL certificate health and domain expiry dates for your web properties.**

Catch expired certs, misconfigured chains, and domains about to lapse before they become production emergencies.

[![Project Stage](https://img.shields.io/badge/Stage-Beta-blue)](https://edgeiqlabs.com)
[![Python](https://img.shields.io/badge/Python-3.8+-green)](https://python.org)
[![License](https://img.shields.io/badge/License-MIT-orange)](LICENSE)

---

## What It Does

Monitors SSL/TLS certificate health: issuer verification, validity window, chain completeness, protocol versions, cipher strength, and days until expiry. Also tracks domain registration expiry dates.

---

## Key Features

- **SSL Certificate Check** — issuer, validity, chain completeness, protocol/cipher strength
- **Domain Expiry Check** — WHOIS registration and expiration via port 43
- **Days-to-Expiry Alerting** — configurable warning thresholds (30/14/7/3 days)
- **Batch Monitoring** — check multiple domains in one run
- **Silent Mode** — full report, no stdout noise unless issues found
- **Pure Python** — no external dependencies beyond stdlib + socket

---

## Prerequisites

- Python 3.8+
- **Pure stdlib** — no pip install required

---

## Installation

```bash
git clone https://github.com/snipercat69/edgeiq-ssl-watcher.git
cd edgeiq-ssl-watcher
# No pip install needed!
```

---

## Quick Start

```bash
# Check SSL for a domain
python3 ssl_watcher.py --domain example.com

# Check multiple domains
python3 ssl_watcher.py --domains example.com store.example.com api.example.com

# Silent mode (only report issues)
python3 ssl_watcher.py --domains example.com --silent

# Alert on domains expiring within 30 days
python3 ssl_watcher.py --domains example.com --alert-days 30
```

---

## Pricing

| Tier | Price | Features |
|------|-------|----------|
| **Free** | $0 | 3 domains, weekly checks |
| **Pro** | $5/mo | Unlimited domains, daily checks, email alerts |
| **Lifetime** | $25 one-time | All Pro features, forever |

---

## Integration with EdgeIQ Tools

- **[EdgeIQ Subdomain Hunter](https://github.com/snipercat69/edgeiq-subdomain-hunter)** — monitor TLS on discovered subdomains
- **[EdgeIQ Network Scanner](https://github.com/snipercat69/edgeiq-network-scanner)** — scan hosts for SSL issues

---

## Support

Open an issue at: https://github.com/snipercat69/edgeiq-ssl-watcher/issues

---

*Part of EdgeIQ Labs — [edgeiqlabs.com](https://edgeiqlabs.com)*
