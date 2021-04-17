# GNU Make

## References

- [Manual](https://www.gnu.org/software/make/manual/html_node/index.html)
- [Dealing with assignment operator](https://github.com/amjadmajid/Makefile#dealing-with-assignment-operator)

## CLI

### Installation

#### APT

```sh
sudo apt update
sudo apt -y install make
```

#### YUM

```sh
yum check-update
sudo yum -y install make
```

#### APK

```sh
sudo apk update
sudo apk add make
```

### Commands

```sh
make --help
```

### Tips

#### EditorConfig

```sh
cat << EOF >> ./.editorconfig

[{*.mk,Makefile}]
indent_size = 4
indent_style = tab
EOF
```

### Issues

<!-- #### Missing GNU Readline Library

```log
/bin/sh: /tmp/_MEIl8vInH/libreadline.so.7: no version information available (required by /bin/sh)
```

TODO -->
