# bin-ubuntu

Ubuntu / Linux 下的一键脚本，用 `download` 按 URL 下载即可，可与其他命令组合（如 `with-proxy download ...`）。

## 下载方式：使用 download

先获取 `download` 脚本（只需一次），再用它下载任意本仓库脚本。

**首次获取 download（二选一，复制粘贴即可）：**

```bash
curl -fSL -o download "https://github.com/JiashuaiXu/bin-ubuntu/raw/main/download"
chmod +x download
```

或（若已有 download）：

```bash
./download "https://github.com/JiashuaiXu/bin-ubuntu/raw/main/download"
```

**之后用 download 下载其他脚本（直接贴链接，自动 blob→raw 并 chmod +x）：**

```bash
./download "https://github.com/JiashuaiXu/bin-ubuntu/blob/main/install-claude-code"
./install-claude-code
```

```bash
./download "https://github.com/JiashuaiXu/bin-ubuntu/blob/main/with-proxy"
./with-proxy curl -s ifconfig.me
```

**与代理组合使用：**

```bash
with-proxy ./download "https://github.com/JiashuaiXu/bin-ubuntu/raw/main/install-fnm"
./install-fnm
```

```bash
with-proxy ./install-fnm
```

**说明：** 直接 `download <url>` 即可，会下载并赋予执行权限；可粘贴 GitHub 页面链接（含 `blob`），脚本会自动转为 raw 下载。

## Windows

在 WSL 或 Git Bash 中执行上述命令；未装 curl 可：`winget install curl.curl`。

## 参数用法速查

| 脚本 | 用法 |
|------|------|
| `download` | `download <url>` 或 `download <url> [输出文件名]` |
| `install-claude-code` | `install-claude-code [API_KEY]` 或 `install-claude-code --api-key <KEY>`，无 Key 时交互输入 |

更多选项可执行 `./脚本名 --help` 查看。
