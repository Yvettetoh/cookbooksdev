# cross-env

## CLI

### Installation

#### NPM

```sh
npm install cross-env --save-dev
```

### Configuration

**Refer:** `package.json`

```json
{
  "scripts": {
    "start": "cross-env NODE_ENV='production' node ./index.js",
    "dev": "cross-env NODE_ENV='development' nodemon ./index.js"
  }
}
```
