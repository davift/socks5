# socks5

![Static Badge](https://img.shields.io/badge/Python-blue?style=social&logo=Python)

A toy SOCKS5 server proxy with username/password authentication.

Fork of https://rushter.com/blog/python-socks-server/

## Usage

```bash
python3 socks5.py
```

By default it listens on `0.0.0.0:9011` and requires SOCKS5 username/password
authentication. Override any of these via environment variables:

| Variable | Default | Purpose |
|---|---|---|
| `SOCKS_HOST` | `0.0.0.0` | Bind address |
| `SOCKS_PORT` | `9011` | Bind port |
| `SOCKS_USER` | `useRName` | Auth username |
| `SOCKS_PASS` | `pasSWord` | Auth password |

**Change `SOCKS_USER`/`SOCKS_PASS` before exposing it** — the defaults are public.

Test it:

```bash
curl --socks5 useRName:pasSWord@127.0.0.1:9011 https://ifconfig.me
```
