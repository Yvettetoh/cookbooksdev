# GitHub

<!--
https://github.com/revoltchat/.github
https://github.com/chdsbd/kodiak

https://media-exp1.licdn.com/dms/image/sync/C4E27AQFXhz19BLKTlg/articleshare-shrink_800/0/1620311917375?e=1620406800&v=beta&t=kcsEPLfDy2Up6iCcr7gyH9OIJhH0Pgj09CtvABBcVGc

https://github.com/cla-assistant/cla-assistant

https://github.community/t/picture-tag-in-markdown/149471
-->

## Links

- [Government](https://government.github.com/community/)
- [GitHub Flavored Markdown Spec](https://github.github.com/gfm/)
- [Bug Report](https://support.github.com/contact/bug-report)

## References

- [myOctocat](https://myoctocat.com/)
- [GitHub Status](https://githubstatus.com/)

## API

- [Rate Limit](https://api.github.com/rate_limit)
- [GitHub GraphQL API](https://docs.github.com/en/graphql/overview/explorer)

## Tools

- [GitHub social previews](https://mugshotbot.com/github)
- [PullApprove](https://pullapprove.com/)

## Settings

- [Settings / Theme preferences](https://github.com/settings/appearance)
- [Notifications](https://github.com/settings/notifications)
- [Register a new OAuth application](https://github.com/settings/applications/new)

## Guides

- [Customizing your organization's profile](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile)

## Misc

- [User Avatar](https://github.com/brunowego.png)
- [Issues / Assigned](https://github.com/issues/assigned)
- [How can we help with your forks?](https://support.github.com/request/fork)

## Search

```txt
".node" in:file filename:.gitattributes
```

## App

### Installation

#### Homebrew

```sh
brew install --cask github
```

## CLI

### Installation

#### Homebrew

```sh
brew install gh
```

#### Chocolatey

```sh
choco install gh
```

### Commands

```sh
gh -h
```

### Usage

```sh
#
gh auth login -w

#
gh repo create \
  --public
```

## Tips

### Personal Access Token

- [docker-cli](https://github.com/settings/tokens/new?description=docker-cli&scopes=write:packages)
- [git-cli](https://github.com/settings/tokens/new?description=git-cli&default-expires-at=90&scopes=repo)

### Clone with GitHub Token

```sh
git clone "https://${GITHUB_TOKEN}:x-oauth-basic@github.com/[my-org]/[my-repo].git"
```

### Automatically Delete Branches

1. Repository -> Settings Tab
2. Options Menu
3. Merge button Section -> Automatically delete head branches

### Add License

1. Add file -> Create new file
2. Type "Name your file...": License
   - Choose a license template
