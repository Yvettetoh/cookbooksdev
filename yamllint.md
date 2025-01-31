# yamllint

## Links

- [Code Repository](https://github.com/adrienverge/yamllint)
- [Main Website](https://yamllint.readthedocs.io/en/stable/index.html)

## Docker

### Build

```sh
cat << EOF | docker build $(echo $DOCKER_BUILD_OPTS) -t example/yamllint -
FROM docker.io/alpine:3.9

RUN apk add -q --no-cache py3-setuptools==40.6.3-r0

RUN pip3 install --no-cache-dir \
      yamllint===1.16.0

ENTRYPOINT ["/usr/bin/yamllint"]

EOF
```

### Running

```sh
docker run -it --rm \
  $(echo "$DOCKER_RUN_OPTS") \
  -h yamllint \
  --name yamllint \
  example/yamllint:latest -h
```

## CLI

### Installation

#### Darwin

```sh
brew install yamllint
```

#### pip

```sh
pip3 install -U yamllint
```

#### APT

```sh
sudo apt update
sudo apt -y install yamllint
```

### Commands

```sh
yamllint -h
```

### Configuration

```sh
cat << EOF > ./.yamllint.yml
---
extends: default
# ignore: |
#   **/node_modules/**/*
rules:
  indentation:
    spaces: 2
    indent-sequences: consistent
  quoted-strings:
    quote-type: single
    required: only-when-needed
  truthy:
    # Allowing 'on' due to: https://github.com/adrienverge/yamllint/issues/158
    allowed-values: ['true', 'false', 'yes', 'no', 'on']
EOF
```

### Usage

```sh
#
yamllint ./
```

### Tips

#### [Disable with comments](https://yamllint.readthedocs.io/en/stable/disable_with_comments.html)

```yaml
---
# yamllint disable rule:line-length
# yamllint disable-line rule:line-length
# ...
```

#### Visual Studio Code

**Requirements:** yamllint CLI.

```sh
#
code --install-extension fnando.linter

#
#
jq '."recommendations" += ["fnando.linter"]' "$PWD/.vscode/extensions.json" | sponge "$PWD/.vscode/extensions.json"
```

<!-- "yaml.validate": false -->

### Issues

#### Min Spaces From Content

```log
too few spaces before comment yamllint(comments)
```

**Refer:** `./.yamllint.yaml`

```yaml
---
extends: default
# ...
rules:
  # ...
  comments:
    min-spaces-from-content: 1
```
