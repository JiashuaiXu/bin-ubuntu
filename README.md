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
./download -x "https://github.com/JiashuaiXu/bin-ubuntu/raw/main/download"
```

**之后用 download 下载其他脚本（支持 GitHub 页面链接，自动 blob→raw）：**

```bash
# 下载并赋予执行权限（适合脚本）
./download -x "https://github.com/JiashuaiXu/bin-ubuntu/blob/main/install-claude-code"
./install-claude-code
```

```bash
# 仅下载
./download "https://github.com/JiashuaiXu/bin-ubuntu/blob/main/with-proxy"
chmod +x with-proxy
```

**与代理组合使用：**

```bash
with-proxy ./download -x "https://github.com/JiashuaiXu/bin-ubuntu/raw/main/install-fnm"
./install-fnm
```

```bash
# 或先 with-proxy 再执行任意命令
with-proxy ./install-fnm
```

**说明：** `download -x <url>` 表示下载后自动 `chmod +x`；可直接粘贴 GitHub 页面链接（含 `blob`），脚本会转为 raw 地址下载。

## Windows

在 WSL 或 Git Bash 中执行上述命令；未装 curl 可：`winget install curl.curl`。
