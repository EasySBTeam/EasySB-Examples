# EasySB Examples

Readable client and server configuration samples for
[EasySB](https://github.com/EasySBTeam/EasySB).

These files used to live under `templates/` in the EasySB repository. They were
moved here so the main repository stays code-only.

## Layout

| Directory | Protocol | Contents |
| :--- | :--- | :--- |
| [`Hysteria2/`](Hysteria2/) | Hysteria 2 | sing-box client / server JSONC samples |
| [`VLESS-Vision-REALITY/`](VLESS-Vision-REALITY/) | VLESS + Vision + REALITY | sing-box client / server JSONC samples |
| [`TUIC/`](TUIC/) | TUIC | sing-box client / server JSONC samples |
| [`AnyTLS/`](AnyTLS/) | AnyTLS | sing-box client / server JSONC samples |
| [`VMess-WebSocket-TLS/`](VMess-WebSocket-TLS/) | VMess + WebSocket + TLS | sing-box client / server JSONC samples |
| [`Config/`](Config/) | - | Subscription templates: `tun-fakeip.json` (sing-box) and `mihomo.yaml` (mihomo / Clash Meta) |

## Usage

Every protocol directory holds `config_server.json` and `config_client.json`.
The files are JSONC, so strip the comments before handing them to sing-box:

```bash
sing-box check -c VLESS-Vision-REALITY/config_server.json
```

The UUIDs, passwords, REALITY private keys, domains and certificate paths in
these samples are placeholders. Generate your own values and keep the server and
client sides in sync before deploying.

The two files under `Config/` are the readable mirrors of the templates EasySB
embeds at build time (`internal/subscribe/tun-fakeip.json` and
`internal/subscribe/mihomo.yaml`). Keep each pair in sync when either side
changes.

## License

GPL-3.0, the same license as
[EasySB](https://github.com/EasySBTeam/EasySB). See [LICENSE](LICENSE).
