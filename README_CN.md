![封面图](./resources/header.png)

<p align="center">
  <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/subframe7536/maple-font">
  <img alt="GitHub Downloads (all assets, all releases)" src="https://img.shields.io/github/downloads/subframe7536/maple-font/total">
  <img alt="GitHub Release" src="https://img.shields.io/github/v/release/subframe7536/maple-font">
  <img alt="X (formerly Twitter) Follow" src="https://img.shields.io/twitter/follow/subframe7536">
</p>

<p align="center">
  <a href="#下载">下载</a> |
  <a href="https://font.subf.dev">网站</a> |
  <a href="./README.md">English</a> |
  中文
</p>

# Maple Mono

Maple Mono 是一款开源等宽字体，专注于优化您的编码体验。

我制作它是为了提升自己的工作效率，希望它也能对其他人有所帮助。

V7 是一个完全重制版本，提供了可变字体格式和字体工程源文件，重新设计了超过一半的字形，并提供更智能的连字。您可以[在这里](https://github.com/subframe7536/maple-font/tree/main)查看 V6 版本。

## 特性

- ✨ 可变 - 无限的字体粗细，以及手工微调的斜体字形。
- ☁️ 丝滑 - **圆角**，独特的 `@ $ % & Q ->` 字形，以及手写风格的斜体 `f i j k l x y`。
- 💪 实用 - 大量的智能连字，详见 [`features/`](./source/features/README.md)。
- 🎨 图标 - 提供 [Nerd-Font](https://github.com/ryanoasis/nerd-fonts) 嵌入的版本，添加图标支持。
- 🔨 定制 - 自由开关或者构建 OpenType 字体特性，打造您专属的字体。

### 简体中文、繁体中文和日文

CN 版本基于[资源圆体](https://github.com/CyanoHao/Resource-Han-Rounded)提供了完整的中文开发环境的字符集支持，包括简体中文、繁体中文和日文。同时，中英文 2:1 完美对齐的特性，使得本字体在多语言显示、Markdown 表格等场景可以做到整齐划一、美观舒适。但是中文的间距相比其他流行的中文字体更大，详情请参阅[发行版说明](https://github.com/subframe7536/maple-font/releases/tag/cn-base)和[这个议题](https://github.com/subframe7536/maple-font/issues/211)。

![2-1.png](./resources/2-1.png)

## 屏幕截图

![showcase.png](./resources/showcase.png)

- 生成：[CodeImg](https://github.com/subframe7536/vscode-codeimg)
- 主题：[Maple](https://github.com/subframe7536/vscode-theme-maple)
- 配置：字体大小 16px，行高 1.8，默认字母间距

## 下载

您可以从 [Releases](https://github.com/subframe7536/maple-font/releases) 下载所有字体压缩包。

### Scoop (Windows)
```sh
# 添加 bucket
scoop bucket add nerd-fonts
# Maple Mono (ttf 格式)
scoop install Maple-Mono
# Maple Mono (hinted ttf 格式)
scoop install Maple-Mono-autohint
# Maple Mono (otf 格式)
scoop install Maple-Mono-otf
# Maple Mono NF
scoop install Maple-Mono-NF
# Maple Mono NF CN
scoop install Maple-Mono-NF-CN
```

### Homebrew (MacOS, Linux)

```sh
# Maple Mono
brew install --cask font-maple-mono
# Maple Mono NF
brew install --cask font-maple-mono-nf
# Maple Mono CN
brew install --cask font-maple-mono-cn
# Maple Mono NF CN
brew install --cask font-maple-mono-nf-cn
```

### AUR (Arch Linux)

```shell
# Maple Mono
paru -S ttf-maple-beta
# Maple Mono NF
paru -S ttf-maple-beta-nf
# Maple Mono NF CN
paru -S ttf-maple-beta-nf-cn
```

## CDN

### Maple Mono

- [fontsource](https://fontsource.org/fonts/maple-mono)
- [ZeoSeven Fonts](https://fonts.zeoseven.com/items/443/)

### Maple Mono CN

- [The Chinese Web Fonts Plan (中文网字计划)](https://chinese-font.netlify.app/zh-cn/fonts/maple-mono-cn/MapleMono-CN-Regular)
- [ZeoSeven Fonts](https://fonts.zeoseven.com/items/442/)

## 使用方法 & 特性配置

请参阅 [文档](./source/features/README_CN.md) 或者在 [这里](https://font.subf.dev/zh-cn/playground) 尝试。

> [!note]
> 用于自定义构建的 Web 工具仍在开发中。

## 命名说明

### 字体特性

- **Ligature**: 带有连字的默认版本 (`Maple Mono`)
- **No-Ligature**: 没有连字的默认版本 (`Maple Mono NL`)
- **Normal-Ligature**: 带有连字的 [`--normal` 预设](#预设) (`Maple Mono Normal`)
- **Normal-No-Ligature**: 没有连字的 [`--normal` 预设](#预设) (`Maple Mono Normal NL`)

### 字体格式和字符集

- **Variable**: 最小版本，通过字体的可变轴改变字体粗细
- **TTF**: 最小版本，ttf 格式 [推荐！]
- **OTF**: 最小版本，otf 格式
- **WOFF2**: 最小版本，woff2 格式，多用于网页加载
- **NF**: 嵌入 Nerd-Font 的版本，为终端添加图标 (带有 `-NF` 后缀)
- **CN**: 中文版本，嵌入中文和日文字形 (带有 `-CN` 后缀)
- **NF-CN**: 完整版本，嵌入图标、中文和日文字形 (带有 `-NF-CN` 后缀)

### 字体微调

- **Hinted 字体** 用于低分辨率屏幕，以获得更好的渲染效果。根据我个人的经验，如果您的屏幕分辨率低于或等于 1080P，建议使用 "hinted 字体"。使用 "unhinted 字体" 会导致文本错位或粗细不均。
  - 在这种情况下，您可以选择 `MapleMono-TTF-AutoHint` / `MapleMono-NF` / `MapleMono-NF-CN` 等。
- **Unhinted 字体** 用于高分辨率屏幕（例如 MacBook）。使用 "hinted 字体" 会使您的文本模糊或看起来很奇怪。
  - 在这种情况下，您可以选择 `MapleMono-OTF` / `MapleMono-TTF` / `MapleMono-NF-unhinted` / `MapleMono-NF-CN-unhinted` 等。
- 为什么存在 `-AutoHint` 和 `-unhinted` 后缀？
  - 为了向后兼容，我保留了原始命名方案。`-AutoHint` 仅用于 `TTF` 格式。


## 自定义构建

[`config.json`](./config.json) 文件用于配置构建过程。查看 [schema](./source/schema.json) 或 [文档](./source/features/README.md) 了解更多详情。

还有一些 [命令行选项](#构建脚本用法) 用于自定义构建过程。命令行选项的优先级高于 `config.json` 中的选项。

### 使用 Github Actions

您可以使用 [Github Actions](https://github.com/subframe7536/maple-font/actions/workflows/custom.yml) 来构建字体。

1. Fork 仓库
2. (可选) 更改 `config.json` 中的内容
3. 转到 Actions 选项卡
4. 点击左侧的 `Custom Build` 菜单项
5. 点击 `Run workflow` 按钮并设置选项
6. 等待构建完成
7. 从 Releases 下载字体压缩包

### 使用 Docker

```shell
git clone https://github.com/subframe7536/maple-font --depth 1 -b variable
docker build -t maple-font .
docker run -v "$(pwd)/fonts:/app/fonts" -e BUILD_ARGS="--normal" maple-font
```

### 本地构建

克隆仓库并在您的本地机器上运行。确保您已安装 `python3` 和 `pip`

```shell
git clone https://github.com/subframe7536/maple-font --depth 1 -b variable
pip install -r requirements.txt
python build.py
```

- 对于 `Ubuntu` 或 `Debian`，可能还需要 `python-is-python3`

如果您在安装依赖项时遇到问题，只需创建一个新的 GitHub Codespace 并在那里运行命令

#### 自定义 Nerd-Font

对于自定义 `font-patcher` 参数，需要安装 `font-forge`（可能还需要 `python3-fontforge`）。

也许您还应该更改 [config.json](./config.json) 中的 `"nerd_font.extra_args"`

默认参数：`-l --careful --outputdir dir`
- 如果 `"nerd_font.mono"` 设置为 `true`，则增加 `--mono`

#### 预设

运行 `build.py` 时添加 `--normal` 参数，让字形不那么独特~~奇怪~~，就像 `JetBrains Mono` 一样（除了 `0` 的中间是斜线而不是点）。

#### 字体特性强制开启

有三种选项（[为什么](https://github.com/subframe7536/maple-font/issues/233#issuecomment-2410170270)）：

1. `enable`: 强制启用这些特性，而无需在字体特性配置中设置 `cvXX` / `ssXX` / `zero`，就像默认连字一样
2. `disable`: 删除 `cvXX` / `ssXX` / `zero` 中的特性，即使您手动启用它，也不在生效
3. `ignore`: 什么也不做

#### 加载自定义特性文件

运行 `build.py` 时添加 `--apply-fea-file` 参数，会读取 [`source/features/{regular,italic}.fea`](./source/features) 的特性文件并应用到可变字体中。您可以修改它来更改所有特性，例如删除 `calt` 中的一些连字。

### 中文版本

默认情况下不会生成中文字体，运行 `python build.py` 时添加 `--cn` 参数，中文基字（约 130 MB）将从 GitHub 下载。

如果您想从可变字体（约 35 MB）构建中文基字，请在 [config.json](./config.json) 中设置 `"cn.use_static_base_font": false` 并且**耐心等待**，可变字体静态化将花费大约 20-30 分钟。

#### 缩小中文字体的间距

如果您觉得中文字符的间距**过大**，有一个**实验性**的构建选项 `cn.narrow` 或 参数 `--cn-narrow` 可以缩小间距。您可以在 [#249](https://github.com/subframe7536/maple-font/issues/249) 中查看效果并跟踪问题。

#### GitHub 镜像

构建脚本将自动从 GitHub 下载所需的资源。如果您在下载时遇到问题，请在 [config.json](./config.json) 中设置 `github_mirror` 或将 `$GITHUB` 设置为您的环境变量。（目标 URL 为 `https://<github_mirror>/<user>/<repo>/releases/download/<tag>/<file>`），或者直接下载目标 `.zip` 文件并将其放在与 `build.py` 相同的目录中。

### 构建脚本用法

```
usage: build.py [-h] [-v] [-d] [--debug] [-n] [--feat FEAT] [--apply-fea-file]
                [--hinted | --no-hinted] [--liga | --no-liga] [--cn-narrow]
                [--nerd-font | --no-nerd-font] [--cn | --no-cn] [--cn-both]
                [--ttf-only] [--cache] [--cn-rebuild] [--archive]

✨ Builder and optimizer for Maple Mono

options:
  -h, --help        显示此帮助信息并退出
  -v, --version     显示程序的版本号并退出
  -d, --dry         输出配置并退出
  --debug           在字体名称中添加 `Debug` 后缀，跳过优化

Feature Options:
  -n, --normal      使用 normal 预设，就像带有斜杠 0 的 `JetBrains Mono`
  --feat FEAT       强制启用字体特性，用 `,` 分隔 (例如 `--feat
                    zero,cv01,ss07,ss08`)。对可变字体无效
  --apply-fea-file  从 `source/features/{regular,italic}.fea` 加载特性文件到
                    可变字体
  --hinted          在 NF / CN / NF-CN 中使用 hinted 字体作为基础字体 (默认)
  --no-hinted       在 NF / CN / NF-CN 中使用 unhinted 字体作为基础字体
  --liga            保留所有连字 (默认)
  --no-liga         删除所有连字
  --cn-narrow       减小中文字形间距 (实验性的)

Build Options:
  --nerd-font       构建 Nerd-Font 版本 (默认)
  --no-nerd-font    不构建 Nerd-Font 版本
  --cn              构建中文版本
  --no-cn           不构建中文版本 (默认)
  --cn-both         同时构建 `Maple Mono CN` 和 `Maple Mono NF CN`。必须启用
                    Nerd-Font 版本
  --ttf-only        仅构建 TTF 格式
  --cache           重用 TTF、OTF 和 Woff2 格式的字体缓存
  --cn-rebuild      重新静态化中文基字
  --archive         构建带有配置和许可的字体压缩包。如果带有 `--cache`
                    标志，则仅打包 Nerd-Font 和 CN 格式
```

## 我个人在用的其他中文字体资源

[cn-resource](https://github.com/subframe7536/maple-font/tree/other-resources/cn-resource)

## 鸣谢

- [JetBrains Mono](https://github.com/JetBrains/JetBrainsMono)
- [Roboto Mono](https://github.com/googlefonts/RobotoMono)
- [Fira Code](https://github.com/tonsky/FiraCode)
- [Victor Mono](https://github.com/rubjo/victor-mono)
- [Commit Mono](https://github.com/eigilnikolajsen/commit-mono)
- [Code Sample](https://github.com/TheRenegadeCoder/sample-programs-website)
- [Nerd Font](https://github.com/ryanoasis/nerd-fonts)
- [Font Freeze](https://github.com/MuTsunTsai/fontfreeze/)
- [Font Viewer](https://tophix.com/font-tools/font-viewer)
- [Monolisa](https://www.monolisa.dev/)
- [Recursive](https://www.recursive.design/)

## 赞助

如果这个字体对您有所帮助，可以通过 [爱发电](https://afdian.com/a/subframe7536) 赞助我

## 点星

[![Star History Chart](https://api.star-history.com/svg?repos=subframe7536/maple-font&type=Date)](https://www.star-history.com/#subframe7536/maple-font&Date)

## 许可

SIL Open Font License 1.1
