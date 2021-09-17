# gemini

[![Deploy](https://github.com/eggplants/gemini/actions/workflows/deploy.yml/badge.svg)](https://github.com/eggplants/gemini/actions/workflows/deploy.yml) [![Website](https://img.shields.io/website?label=HTTPS&url=https%3A%2F%2Feggplants.srht.site)](https://eggplants.srht.site)

## WHAT?

- Publish gmi documents to sourcehut automatically:
  - `gemini://${USERNAME}.srht.site`
  - `https://${USERNAME}.srht.site`

## Step

1. [Fork me](https://github.com/eggplants/gemini/fork)
2. [Register sourcehut](https://meta.sr.ht/register)
3. [Generate OAuth2.0 Personal Token](https://meta.sr.ht/oauth2/personal-token)
4. Set generated PAT to `PH_TOKEN` repository's sectets (see [docs](https://docs.github.com/en/actions/reference/encrypted-secrets#creating-encrypted-secrets-for-a-repository))
5. Modified gmi docs and director(ies) in `./pub/gmi/`
6. Change [USERNAME](https://github.com/eggplants/gemini/blob/bff21010c6b49f9e7b50b50a94cd86316261a88d/.github/workflows/deploy.yml#L37) into yours
7. CI works by pushing your commits to repo or running [manually](https://docs.github.com/en/actions/managing-workflow-runs/manually-running-a-workflow#running-a-workflow)
8. Deployed!
