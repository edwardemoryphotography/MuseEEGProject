# Muse EEG Neurofeedback Project

> Real-time Muse EEG brainwave visualization and neurofeedback platform.

---

## Overview

**MuseEEGProject** is a containerized Python application that streams real-time EEG data from the **Muse 2 headband**, processes brainwave signals, and delivers live neurofeedback visualizations. Built with Docker for portable deployment across development and production environments.

This project is part of the broader EEG neurofeedback ecosystem alongside `muse-neurofeedback` and `neurocreative-platform`.

---

## Status

| Item | Status |
|------|--------|
| Active Development | ✅ Yes |
| Docker Container | ✅ Configured |
| EEG Data Streaming | ✅ Python (19%) |
| CI/CD Workflows | ✅ GitHub Actions |
| Test Suite | ✅ `tests/` folder |
| Muse 2 Compatibility | ✅ Yes |

---

## Architecture

```
MuseEEGProject/
├── .github/workflows/   # CI/CD pipelines
├── tests/               # Test suite
├── Dockerfile           # Container configuration
├── requirements.txt     # Python dependencies
├── RESOURCES.md         # Reference materials and links
└── README.md
```

---

## Features

- Real-time EEG data ingestion from Muse 2 headband
- Brainwave band analysis (alpha, beta, theta, delta, gamma)
- Docker-containerized deployment for portability
- Automated CI/CD via GitHub Actions workflows
- Comprehensive test suite in `tests/`
- Resource documentation in `RESOURCES.md`

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| EEG Hardware | Muse 2 Headband |
| Language | Python 3.9+ |
| Containerization | Docker |
| CI/CD | GitHub Actions |
| Testing | pytest |

---

## Getting Started

### Prerequisites

- Docker installed
- Muse 2 headband + Mind Monitor app
- Python 3.9+ (for local development)

### Run with Docker

```bash
git clone https://github.com/edwardemoryphotography/MuseEEGProject.git
cd MuseEEGProject
docker build -t muse-eeg .
docker run muse-eeg
```

### Run Locally

```bash
pip install -r requirements.txt
python main.py
```

### Run Tests

```bash
pytest tests/
```

---

## Roadmap

- [ ] Live brainwave dashboard (web UI)
- [ ] Session recording + playback
- [ ] WHOOP HRV integration
- [ ] Kubernetes deployment config
- [ ] REST API for external integrations
- [ ] Cross-repo sync with neurocreative-platform

---

## Related Repos

- [`neurocreative-platform`](https://github.com/edwardemoryphotography/neurocreative-platform) — Unified EEG + WHOOP backend
- [`muse-neurofeedback`](https://github.com/edwardemoryphotography/muse-neurofeedback) — Neurofeedback application

---

## Audit Notes

- **Last reviewed**: 2025 — Identified as stale-active during GitHub audit
- **Action taken**: README fully documented
- **Priority**: Medium — Docker + CI config is solid foundation

---

*Part of the edwardemoryphotography GitHub ecosystem.*
