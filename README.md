<h1 align="center">🥦 Taze<sup>𝛼</sup></h1>
<p align="center"><sup>(/ta:zei/, <em>fresh</em> in Turkish)</sup></p>
<p align="center">A modern cli tool that keeps your deps fresh</p>

![](./screenshots/r-major.png)

<pre align="center">npx <b>taze</b></pre>

<p align="center">or recursively for <b>monorepos</b></p>

<pre align="center">npx taze <b>-r</b></pre>

## Features

- Built-in support for monorepos
- No installation required - `npx taze`
- Safe by default - updates in the version range your allowed

## Usage

By default, `taze` will only bump versions in the ranges you specified in package.json *(which is safe and the default behavior of `npm install`)*

![](./screenshots/default.png)

To ignore the ranges, if you explicitly set the maximum allowenace version changes. For example `taze major` will check all changes and bump to the lastest stable changes including majors(breaking changes), or `taze minor` that bump to lastest minor changes within the same major version.

![](./screenshots/major.png)
![](./screenshots/minor.png)
![](./screenshots/patch.png)

### Monorepo

`taze` is built with the first-class monorepo support. Simply adding `-r`, it will scan the subdirectories that contains `package.json` and update them together. It will handles in local private packages automatically.

![](./screenshots/resolving.png)
![](./screenshots/r-default.png)

## Configures

See `taze --help`

### Filter

You can filter out packages you want to check for upgrades by string or regex.

```bash
taze --filter lodash,webpack
taze --filter /(lo|hi)dash/
```

![](./screenshots/filter.png)


## Programmatic APIs

> TODO:

## Alternatives

`taze` is great inspired from the following tools. They work well but have different feature sets and focuses, try them out as well!

- [npm-check-updates](https://github.com/raineorshine/npm-check-updates)
- [npm-check](https://github.com/dylang/npm-check)

## Thanks

Great thanks to [@sinoon](https://github.com/sinoon) who helped a lot on having idea brainstroming and feedback discussion. 