# gemini

[![Deploy](https://github.com/eggplants/gemini/actions/workflows/deploy.yml/badge.svg)](https://github.com/eggplants/gemini/actions/workflows/deploy.yml) [![Website](https://img.shields.io/website?label=HTTPS&url=https%3A%2F%2Feggplants.srht.site)](https://eggplants.srht.site)

## Template

<https://github.com/eggplants/gemini-template>

## WHAT?

- Publish gmi documents to sourcehut automatically:
  - [gemini://eggplants.srht.site](https://portal.mozz.us/gemini/eggplants.srht.site)
  - [https://eggplants.srht.site](https://eggplants.srht.site)

## Step

1. [Fork me](https://github.com/eggplants/gemini/fork)
2. [Register sourcehut](https://meta.sr.ht/register)
3. [Generate OAuth2.0 Personal Token](https://meta.sr.ht/oauth2/personal-token)
4. Set generated PAT `PH_TOKEN` of repository's Secrets in Settings (see [docs](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository))
5. Modified gmi docs and directories in `./pub/gmi/`
6. Change [USERNAME](https://github.com/eggplants/gemini/blob/bff21010c6b49f9e7b50b50a94cd86316261a88d/.github/workflows/deploy.yml#L37) into yours
7. CI works by pushing your commits to repo or running [manually](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow)
8. Deployed!

## CheatSheet for writing Gemtext

```markdown
# Title
## heading
Hello! This is...
* 1aaaa
* 2bbbb
* 3cccc
> he says:
> Heeloooooooooooo woooold!!!!
## Link
=> gemini://hogee.com ほげえ
=> gopher://hugaa.com ふがあ
## Code
`󠀭``
echo test
`󠀭``
```

## Demo

![image](https://user-images.githubusercontent.com/42153744/133748288-6a480f25-a5d0-4db8-b1dc-7d8dcebbcab7.png)

## TIPS

- install [asuka](https://git.sr.ht/~julienxx/asuka) (TUI client)

```bash
git clone --depth 1 https://git.sr.ht/~julienxx/asuka
cd asuka
command -v cargo >/dev/null || {
  curl https://sh.rustup.rs -sSf | sh
  source $HOME/.cargo/env
}
cargo build --release
sudo install -m+x target/release/asuka /usr/local/bin
asuka
```

![asuka](https://user-images.githubusercontent.com/42153744/133748511-67fc69d5-e564-4be6-ac6b-a214fe42cf3a.png)

- install [laglange] (GUI client)

```bash
if command -v brew >/dev/null; then
  brew install --cask lagrange
else
  command -v ail-cli >/dev/null || {
    sudo add-apt-repository ppa:appimagelauncher-team/stable
    sudo apt update
    sudo apt install appimagelauncher -y 
  }
  wget https://git.io/JztqW
  ail-cli integrate Lagrange-*
fi
xdg-open gemini://eggplants.srht.site
```

![image](https://user-images.githubusercontent.com/42153744/133888463-50eb6156-b79f-4032-8cbd-14cff8be6e66.png)
