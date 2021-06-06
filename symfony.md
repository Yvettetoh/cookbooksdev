# Symfony

<!--
https://www.linkedin.com/learning/learning-symfony-4/build-web-apps-with-symfony
-->

## Links

- [Symfony Releases](https://symfony.com/releases/)

## Bundles

- [Flagception](https://github.com/bestit/flagception-bundle)

## CLI

### References

- [Symfony Documentation](https://symfony.com/doc/current/index.html#gsc.tab=0)

### Installation

#### Unix-like

```sh
curl -sS https://get.symfony.com/cli/installer | /bin/bash
```

### Environment

For Bash or Zsh, put something like this in your `$HOME/.bashrc` or `$HOME/.zshrc`:

```sh
# Symfony
export PATH="$HOME/.symfony/bin:$PATH"
```

```sh
sudo su - "$USER"
```

### Commands

```sh
symfony -h
```

### Usage

```sh
#
symfony new [name] && cd "$_"

#
symfony server:start

#
symfony check:security
```
