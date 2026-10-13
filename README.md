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
brew install --cask saba383810/tap/coding-agent-usage-bar
```

未署名なので、Gatekeeper に止められないよう Cask がインストール後に quarantine 属性を外す。
Homebrew 7 以降は tap の trust が必要だが、上のように `saba383810/tap/...` の完全修飾名で
インストールすれば自動で trust される。

`version :latest` なので、通常の `brew upgrade` では更新されない。
新しいリリースを入れる時は次のとおり。

```sh
brew upgrade --cask --greedy coding-agent-usage-bar
```

アンインストールは次のとおり (`--zap` を付けると設定も消える)。

```sh
brew uninstall --cask coding-agent-usage-bar
brew uninstall --cask --zap coding-agent-usage-bar
```
