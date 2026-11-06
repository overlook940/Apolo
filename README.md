<p align="center">
  <img src="src-tauri/icons/128x128@2x.png" width="128" height="128" alt="Apolo">
</p>

<h1 align="center">Apolo</h1>

<p align="center">
  <strong>更轻的图片，同样出色。</strong><br>
  macOS、Windows 和 Linux 的图片优化器：WebP、AVIF、JPEG XL、JPEG 和 PNG，全部在你自己的
  电脑上完成，保存之前先看到损失。免费且开源。
</p>

<p align="center">
  不上传任何地方，压缩图片并转换为 WebP、AVIF 或 JPEG XL：单张处理、整个文件夹、从终端，
  或交给你的 AI 智能体。
</p>

<p align="center">
  <a href="https://apolo.webcafeina.com/en/download/mac/"><img src=".github/readme/descargar-mac-en.svg" alt="下载 Mac 版" height="46"></a>
  <a href="https://apolo.webcafeina.com/en/download/windows/"><img src=".github/readme/descargar-windows-en.svg" alt="下载 Windows 版" height="46"></a>
  <a href="https://apolo.webcafeina.com/en/download/linux/"><img src=".github/readme/descargar-linux-en.svg" alt="下载 Linux 版" height="46"></a>
</p>

<p align="center">
  <a href="https://github.com/webcafeina/Apolo/releases/latest"><img src="https://img.shields.io/github/v/release/webcafeina/Apolo?label=version" alt="版本"></a>
  <a href="https://github.com/webcafeina/Apolo/releases"><img src="https://img.shields.io/github/downloads/webcafeina/Apolo/total?label=downloads" alt="下载量"></a>
  <a href="https://github.com/webcafeina/Apolo/actions/workflows/comprobar.yml"><img src="https://github.com/webcafeina/Apolo/actions/workflows/comprobar.yml/badge.svg" alt="检查"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-GPLv3-blue" alt="GPLv3"></a>
</p>

<p align="center"><a href="https://apolo.webcafeina.com/en/">apolo.webcafeina.com</a> · <a href="https://apolo.webcafeina.com/en/guides/">指南</a> · <a href="https://apolo.webcafeina.com/en/compare/">对比</a> · <a href="README.en.md">English</a> · <a href="README.es.md">Español</a></p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/readme/apolo-macos-oscuro-en.webp">
    <img src=".github/readme/apolo-macos-claro-en.webp" alt="Apolo 在 macOS：工作台用滑块对比原图与结果" width="900">
  </picture>
</p>

## 为什么选择 Apolo

- **保存之前，先看到损失。** 用滑块对比原图与结果，并排或差异图两种模式，Apolo 还会给出
  两者的 SSIMULACRA 2 评分。
- **与官方工具逐字节一致**：`cwebp`、`cjpeg`（MozJPEG）、`oxipng`、`avifenc` 和 `cjxl`
  都内置其中，带全部选项，Apolo 还会给出等价的命令。
- **按评分控制质量。** 要求无可察觉的损失，Apolo 会逐张照片找到达到该效果的最低质量。
- **整个文件夹**：并行批量、同时输出多种格式、每张取最轻的、统一尺寸，而且绝不覆盖任何
  文件。
- **裁剪与调整尺寸**：直接在图片上操作，按最长边、百分比或宽高。
- **可打开 iPhone 照片**（HEIC），以及 PNG、JPEG、WebP、AVIF、JPEG XL、TIFF、GIF、BMP、
  QOI 和 PNM。
- **为每个系统量身打造**：macOS 的 Liquid Glass、Windows 的 Fluent 与 Mica、GNOME 的
  Adwaita、KDE 的 Breeze。提供英语、西班牙语和简体中文界面。
- **私密且轻量**：图片绝不离开你的电脑，处理 2400 万像素照片时内存保持在 2 GB 左右。
- **配合 AI 智能体**：Claude、Cursor 或 VS Code 通过其 MCP 服务器完成优化。

<table>
  <tr>
    <td><img src=".github/readme/apolo-windows-claro-en.webp" alt="Apolo 在 Windows 11" width="300"></td>
    <td><img src=".github/readme/apolo-gnome-claro-en.webp" alt="Apolo 在 Ubuntu（GNOME）" width="300"></td>
    <td><img src=".github/readme/apolo-kde-claro-en.webp" alt="Apolo 在 KDE Plasma" width="300"></td>
  </tr>
  <tr>
    <td align="center">Windows 11</td>
    <td align="center">Ubuntu（GNOME）</td>
    <td align="center">KDE Plasma</td>
  </tr>
</table>

## 下载

最简单的方式是 **[apolo.webcafeina.com](https://apolo.webcafeina.com/en/)**：它知道你的电脑
型号并给出对应的下载。每个文件也都在
**[最新 Release](https://github.com/webcafeina/Apolo/releases/latest)**，校验和在
`SHA256SUMS.txt` 中。

| 系统 | 应用 |
|---|---|
| **macOS 11+**，Apple 芯片与 Intel | 通用 `.dmg` |
| **Windows 10 和 11**，x64 与 ARM | `.exe` 安装器 |
| **Linux**，x64 与 ARM | `.deb`（Debian、Ubuntu）、`.rpm`（Fedora、openSUSE）、AppImage 或 PKGBUILD（Arch） |

**用 Homebrew**，适用于 macOS 和 Linux：

```sh
brew install --cask webcafeina/apolo/apolo   # 应用（macOS）
brew install webcafeina/apolo/apolo          # 命令行和智能体服务器
```

**在 Linux 上使用软件仓库**（用 [Apolo 的密钥](https://apolo.webcafeina.com/apolo.asc)签名），
它会随系统的其余部分一起更新：

```sh
# Debian 和 Ubuntu
sudo install -dm755 /etc/apt/keyrings
sudo curl -fsSLo /etc/apt/keyrings/apolo.asc https://apolo.webcafeina.com/apolo.asc
sudo curl -fsSLo /etc/apt/sources.list.d/apolo.sources https://apolo.webcafeina.com/apt/apolo.sources
sudo apt update && sudo apt install apolo

# Fedora
sudo curl -fsSLo /etc/yum.repos.d/apolo.repo https://apolo.webcafeina.com/rpm/apolo.repo
sudo dnf install apolo

# openSUSE
sudo zypper addrepo https://apolo.webcafeina.com/rpm/apolo.repo
sudo zypper install apolo

# Arch、Manjaro、EndeavourOS、CachyOS（AUR 即将提供，apolo-bin）
mkdir apolo && cd apolo
curl -fsSLO https://apolo.webcafeina.com/aur/PKGBUILD
makepkg -si
```

**自动更新**：有新版本时，Apolo 会提示你并一键安装。

**首次运行**时，由于安装器未签名，系统会警告：
- **macOS**：在「系统设置 › 隐私与安全性」中点「仍要打开」。如果提示已损坏：
  `xattr -dr com.apple.quarantine /Applications/Apolo.app`。
- **Windows**：在 SmartScreen 中点「更多信息」›「仍要运行」。

### 校验下载

Release 中每个文件的 SHA-256 都在 `SHA256SUMS.txt`，并带有 GitHub 签署的来源证明（哪次
构建、哪个提交）。用 [GitHub 命令行](https://cli.github.com)：

```sh
gh attestation verify Apolo_1.0.0_universal.dmg --repo webcafeina/Apolo
```

APT 和 RPM 仓库以及 `.rpm` 文件用 GPG 密钥
`6D95 3C94 D0D6 6AB6 B9B0 FA26 CA21 CD7A B7FA 57FC` 签名。如何报告安全问题见
[SECURITY.md](SECURITY.md)。

## 在终端中

`apolo` 命令行做应用做的一切，带各官方工具的选项和相同的预设：

```sh
apolo webp -q 80 photo.png -o photo.webp                     # 同 cwebp
apolo avif -q 60 photo.png photo.avif                        # 同 avifenc
apolo lote photos/ --formato webp,avif --objetivo 80         # 整个文件夹，按评分
apolo lote photos/ --mas-ligero --formato webp,avif,jpeg --lado-mayor 1920
apolo medir photo.png photo.webp                             # SSIMULACRA 2、PSNR 和 SSIM
```

更多示例见[命令行页面](https://apolo.webcafeina.com/en/cli/)。

## 配合 AI 智能体

Apolo 可以在 **Claude、Cursor、VS Code** 以及任何支持
[MCP](https://modelcontextprotocol.io) 的智能体中使用：它在你的电脑上分析、优化、在相同
感知质量下比较格式、度量损失、转换文件夹。**绝不覆盖或删除任何文件。**

服务器 `apolo-mcp` 内置于应用，随应用一起更新。在 Apolo 侧栏的 **MCP** 一行里，有各个
智能体的配置可直接复制，也有 Claude Desktop 扩展。在 Claude Code 和 Cowork 中，最简单的是
**插件**，它还会教 Claude 何时使用 Apolo（需要 Node.js 18 或更高版本；位于
[empaquetado/claude](empaquetado/claude/apolo)）：

```
/plugin marketplace add webcafeina/Apolo
/plugin install apolo@webcafeina
```

或者在 Claude Code 中手动添加：

```sh
claude mcp add --scope user apolo -- "/Applications/Apolo.app/Contents/MacOS/apolo-mcp"   # macOS
claude mcp add --scope user apolo -- "%LOCALAPPDATA%\Apolo\apolo-mcp.exe"                  # Windows
claude mcp add --scope user apolo -- /usr/bin/apolo-mcp                                    # Linux
```

如何连接各个智能体见[智能体页面](https://apolo.webcafeina.com/en/agents/)；可以问它什么见
[指南](https://apolo.webcafeina.com/en/guides/optimize-images-with-an-ai-agent/)；十一个工具
见 [docs/mcp/catalogo.md](docs/mcp/catalogo.md)（西班牙语）。智能体请求的内容（路径、名称、
缩略图）会进入它的对话，模型提供方也能看到：全部细节见
[隐私页面](https://apolo.webcafeina.com/en/privacy/)。

[![Apolo MCP on mcprush](https://mcprush.com/badge/apolo-mcp/score.svg)](https://mcprush.com/to/apolo-mcp?ref=badge)

## 指南

数据由 Apolo 在 24 张可自由使用的照片上实测：

- [将图片转换为 WebP](https://apolo.webcafeina.com/en/guides/convert-to-webp/)
- [AVIF、WebP 还是 JPEG XL：如何选择](https://apolo.webcafeina.com/en/guides/avif-webp-or-jpeg-xl/)
- [不损失质量地压缩图片](https://apolo.webcafeina.com/en/guides/compress-images-without-losing-quality/)
- [为网页优化图片](https://apolo.webcafeina.com/en/guides/optimize-images-for-the-web/)
- [用 AI 智能体优化图片](https://apolo.webcafeina.com/en/guides/optimize-images-with-an-ai-agent/)
- [将 HEIC 转为 JPG](https://apolo.webcafeina.com/en/guides/heic-to-jpg/)

Apolo 与其他工具的对比见[对比页面](https://apolo.webcafeina.com/en/compare/)。

## 常见问题

免费吗？会上传我的图片吗？为什么系统会警告我？答案见 [FAQ](https://apolo.webcafeina.com/en/faq/)。
每个版本的新增内容见[更新日志](https://apolo.webcafeina.com/en/whats-new/)。

## 构建

需要：
- stable Rust、Node 22 和 pnpm；
- CMake、nasm 和 clang（libjxl 用 clang 构建，与官方 `cjxl` 一致）；
- Linux 上还需要 `libwebkit2gtk-4.1-dev librsvg2-dev libssl-dev pkg-config`。

克隆时带上子模块：`git clone --recurse-submodules`。

```sh
make comprobar     # 格式化、clippy、测试、界面和官网
make equivalencia  # 与 cwebp、cjpeg、oxipng、qoiconv、avifenc 和 cjxl 生成相同的文件
make cli           # 命令行
make mcp           # 智能体服务器 apolo-mcp
make app           # 应用（内含 apolo-mcp）
```

## 许可证

[GPLv3](LICENSE)。Apolo 是自由软件：你可以使用、研究、修改和分享它。内置的引擎各有其
许可证，全部兼容：

| 许可证 | 引擎 |
|---|---|
| BSD | libwebp、MozJPEG、libavif、aom、libyuv 和 libjxl |
| MIT | OxiPNG |
| GPLv3 | libimagequant |
| LGPLv3 | libheif 和 libde265 |
| Apache-2.0 | highway、sjpeg 和 rmcp |
| MIT 或 Apache-2.0 | sys-locale |

由 [Webcafeína](https://webcafeina.com/?utm_source=github&utm_medium=readme&utm_campaign=apolo) 制作。
