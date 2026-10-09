# EasySB Examples

[EasySB](https://github.com/EasySBTeam/EasySB) 的可读客户端与服务端配置样例。

这些文件原先位于 EasySB 仓库的 `templates/` 目录，现迁移至此，让主仓库只保留代码。

## 目录结构

| 目录 | 协议 | 内容 |
| :--- | :--- | :--- |
| [`Hysteria2/`](Hysteria2/) | Hysteria 2 | sing-box 客户端 / 服务端 JSONC 样例 |
| [`VLESS-Vision-REALITY/`](VLESS-Vision-REALITY/) | VLESS + Vision + REALITY | sing-box 客户端 / 服务端 JSONC 样例 |
| [`TUIC/`](TUIC/) | TUIC | sing-box 客户端 / 服务端 JSONC 样例 |
| [`AnyTLS/`](AnyTLS/) | AnyTLS | sing-box 客户端 / 服务端 JSONC 样例 |
| [`VMess-WebSocket-TLS/`](VMess-WebSocket-TLS/) | VMess + WebSocket + TLS | sing-box 客户端 / 服务端 JSONC 样例 |
| [`Config/`](Config/) | - | 订阅模板：`tun-fakeip.json`（sing-box）与 `mihomo.yaml`（mihomo / Clash Meta） |

## 使用方式

每个协议目录包含 `config_server.json` 与 `config_client.json`。文件为 JSONC 格式，
交给 sing-box 前需要去掉注释：

```bash
sing-box check -c VLESS-Vision-REALITY/config_server.json
```

样例中的 UUID、密码、REALITY 私钥、域名与证书路径均为占位符。部署前请自行生成，
并保持服务端与客户端一致。

`Config/` 下的两个文件是 EasySB 构建时内嵌模板（`internal/subscribe/tun-fakeip.json`
与 `internal/subscribe/mihomo.yaml`）的可读镜像，任一侧改动时请同步另一侧。

## 许可证

GPL-3.0，与 [EasySB](https://github.com/EasySBTeam/EasySB) 相同，详见 [LICENSE](LICENSE)。
