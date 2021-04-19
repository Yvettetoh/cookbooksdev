# EditorConfig

## Syntax

### Configuration

```sh
cat << EOF > ./.editorconfig
root = true

[*]
charset = utf-8
end_of_line = lf
indent_size = 2
indent_style = space
insert_final_newline = true
max_line_length = 100
trim_trailing_whitespace = true

[*.md]
max_line_length = 0
trim_trailing_whitespace = false
EOF
```

### Tips

#### Visual Studio Code

```sh
code --install-extension EditorConfig.EditorConfig
```

#### Edit Commit Messages

```conf
[COMMIT_EDITMSG]
max_line_length = 0
```
