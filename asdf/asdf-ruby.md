# asdf Ruby

## Dependencies

### Homebrew

```sh
brew install coreutils gpg
```

## Installation

```sh
asdf plugin-add ruby 'https://github.com/asdf-vm/asdf-ruby.git'
```

## Usage

```sh
#
asdf list-all ruby

#
KEEP_SOURCE=1 \
  asdf install ruby [version]

#
asdf global ruby [version]

#
asdf list ruby

#
asdf reshim ruby [version]
```
