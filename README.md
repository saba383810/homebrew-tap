# homebrew-tap

saba383810 の macOS アプリ用の Homebrew tap。

## 使い方

```sh
brew tap saba383810/tap
```

`brew tap` は省略できるので、直接インストールしてもよい。

## Casks

### coding-agent-usage-bar

Claude Code と Codex の使用量を macOS のメニューバーに表示するアプリ。
→ [saba383810/coding-agent-usage-bar](https://github.com/saba383810/coding-agent-usage-bar)

```sh
brew install --cask --no-quarantine saba383810/tap/coding-agent-usage-bar
```

未署名のため `--no-quarantine` が必要。付け忘れて Gatekeeper に止められた場合は
次のコマンドで解除できる。

```sh
xattr -dr com.apple.quarantine /Applications/CodingAgentUsageBar.app
```

アンインストールは次のとおり (`--zap` を付けると設定も消える)。

```sh
brew uninstall --cask coding-agent-usage-bar
brew uninstall --cask --zap coding-agent-usage-bar
```
