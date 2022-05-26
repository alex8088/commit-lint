
# commit-lint

> Lint commit messages using Angular's commit convention

---

## What is commit-lint

`commit-lint` is not the same as [commitlint](https://github.com/conventional-changelog/commitlint). It's extremely simple, doesn't support rule configuration, and enforces [Angular's commit conventions](https://github.com/conventional-changelog/conventional-changelog/tree/master/packages/conventional-changelog-angular). It was born inspired by `Vue` related projects.

## Usage

### Install

```sh
npm i @alexwei/commit-lint -D
```

### Add Hook

With `husky`, add command to `.husky/commit-msg` file.

```sh
#!/bin/sh
. "$(dirname "$0")/_/husky.sh"

npx commit-lint $1
```

With `simple-git-hooks`, add command to `package.json` file.

```json
"simple-git-hooks": {
    "commit-msg": "npx commit-lint $1"
}
```

With `yorkie`, add command to `package.json` file.

```json
"gitHooks": {
    "commit-msg": "npx commit-lint $1"
}
```

## License

[MIT](./LICENSE)