# NPM Cheat Sheet

List configs and origins (Windows)

```bash
npm config ls -l
```

Open global .npmrc file

```bash
npm config edit --global
```

Search published npm packages

```bash
npm search package-name
```

Combine and wrap files into npm package (great way to test you .npmignore or files config)

```bash
npm pack
```

Verify package installs and works (before publish)

```bash
npm install . -g
```

Verify package has been included

```bash
npm ls -g
```

Refresh symlink package to project connection (created by [npm-link](https://docs.npmjs.com/cli/v9/commands/npm-link))

```bash
npm rebuild -g
```

## Typical .npmrc locations (Windows)

- Global .npmrc:  `C:\Users\%username%\AppData\Roaming\npm\etc\npmrc`
- Per-user .npmrc:  `C:\Users\%username%\.npmrc`
- Built-in .npmrc:  `C:\Program Files\nodejs\node_modules\npm\npmrc`






