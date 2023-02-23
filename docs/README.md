<h1 align="center">
  <p>
    <a href="https://github.com/z-shell/zsh-lsd">
      <img width="80" height="80" src="https://raw.githubusercontent.com/z-shell/zi/main/docs/images/logo.png" alt="Logo" />
    </a>
    ❮ Zsh Plugin - Lsd ❯
  </p>
</h1>
  <h2 align="center">
    <p>Zsh plugin which replace GNU/ls with next generation <kbd>ls</kbd> by <a href="https://github.com/Peltoche/lsd">Peltoche/lsd</a></p>
  </h2>
<h3 align="center">
  <p>
    <a href="https://github.com/orgs/z-shell/discussions/"> 《❔》 Ask a Question </a>
    <a href="https://z.digitalclouds.dev/search/"> 《💡》 Search Wiki </a>
    <a href="https://digitalclouds.crowdin.com/z-shell/"> 《🌐》 Localize </a>
  </p>
</h3>
<div align="center">
<a href="https://github.com/z-shell/zsh-lsd/actions/workflows/trunk-check.yml">
  <img align="center" src="https://github.com/z-shell/zsh-lsd/actions/workflows/trunk-check.yml/badge.svg?branch=main" alt="⭕ Trunk Check" />
</a>
<a href="https://open.vscode.dev/z-shell/zsh-lsd/">
  <img
    align="center"
    src="https://img.shields.io/badge/--007ACC?logo=visual%20studio%20code&logoColor=ffffff"
    alt="Visual Studio Code"
  />
</a></div>

## Default settings

The Zsh plugin replaces the **GNU/ls** with lots of added features like **colors**, **icons**, **tree-view**, and other formatting options.

> Enable auto list directories on `cd` with `export AUTOCD=1`.

## Install

The <kbd>lsd</kbd> should be present to use this plugin. Install <kbd>lsd</kbd> with **Zi**:

```shell
zi ice binary from'gh-r' sbin'**/lsd -> lsd' \
  atclone'cp lsd-*/lsd.1 $ZI[MAN_DIR]/man1; ln -s lsd-*/*/_lsd _lsd'
zi light Peltoche/lsd
```

### With [Zi](https://github.com/z-shell/zi)

To install add to the `.zshrc` file:

```shell
zi light z-shell/zsh-lsd
```

Install only if <kbd>lsd</kbd> available in `$PATH` and enable auto-list directories:

```shell
zi ice has'lsd' atinit'AUTOCD=1'
zi light z-shell/zsh-lsd
```

Install only if <kbd>lsd</kbd> available in `$PATH` and enable auto-list directories in turbo mode:

```shell
zi ice wait lucid has'lsd' atinit'AUTOCD=1'
zi light z-shell/zsh-lsd
```

Install only if <kbd>lsd</kbd> available in `$PATH` and enable auto-list directories in turbo mode with the syntax:

```shell
zi wait lucid for \
  has'lsd' atinit'AUTOCD=1' \
    z-shell/zsh-lsd
```

### With [Oh My Zsh](https://ohmyz.sh/)

Clone the repository and add `zsh-lsd` to the plugins array of your `.zshrc` file:

```sh
~/.oh-my-zsh/custom/plugins
```

```sh
plugins=(... zsh-lsd)
```

### With Zplug

Add `zplug z-shell/zsh-lsd` to your `~/.zshrc` and re-open your terminal session.
