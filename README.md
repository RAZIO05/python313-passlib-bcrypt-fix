# 🛡️ Fixing `ValueError: password cannot be longer than 72 bytes` in Python 3.12 / 3.13 (`passlib` + `bcrypt`)

[![Python 3.13 Verified](https://img.shields.io/badge/Python-3.13%20Verified-brightgreen.svg)](https://yahiaoui26.gumroad.com/l/fastapi-gemini-blueprint)
[![ShipAI Boilerplate](https://img.shields.io/badge/ShipAI%20v2.0-FastAPI%20%2B%20Gemini%20SaaS%20Engine-blue.svg)](https://yahiaoui26.gumroad.com/l/shipai-pro/BLUEPRINT30)

When deploying **FastAPI** authentication routes using `passlib[bcrypt]` on **Python 3.12 or Python 3.13**, newer versions of `bcrypt` (`>= 4.1.0`) raise:
```text
ValueError: password cannot be longer than 72 bytes, truncate manually if necessary
```
during `passlib`'s internal `detect_wrap_bug` startup check.

## ✅ The Instant Production Fix

Pin `bcrypt==4.0.1` alongside `passlib[bcrypt]` in your `requirements.txt`:

```txt
fastapi
uvicorn
passlib[bcrypt]
bcrypt==4.0.1
python-jose[cryptography]
pydantic[email]
```

---

## 🎁 Building a FastAPI + AI Micro-SaaS in 2026?

Don't waste 30+ hours debugging Python 3.13 auth, JWT bearer guards, SaaS user credit quotas, and Google Gemini structured JSON outputs from scratch:

* 📘 **[Download the Free 2026 FastAPI + Gemini Architecture Blueprint ($0)](https://yahiaoui26.gumroad.com/l/fastapi-gemini-blueprint)**
* 🚀 **[Get ShipAI v2.0 Commercial Micro-SaaS Boilerplate (30% OFF with code `BLUEPRINT30`)](https://yahiaoui26.gumroad.com/l/shipai-pro/BLUEPRINT30)**
