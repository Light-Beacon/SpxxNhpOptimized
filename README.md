# spxx

[![Build Status](https://travis-ci.com/SPGoding/spx.svg?branch=master)](https://travis-ci.com/SPGoding/spx)
![GitHub Top Language](https://img.shields.io/github/languages/top/SPGoding/spx.svg)
![License](https://img.shields.io/github/license/SPGoding/spx.svg)

The new and rewritten version of [spx](https://github.com/SPGoding/spx), the ultimate MCZWLT newslord utility.

## Components

### SPXX User Script™

Adds a "Copy Markdown" button to Minecraft.net, feedback.minecraft.net and help.minecraft.net articles and Tweets,
which sets the [Markdown][markdown] representation of this blog article to your clipboard.

You can use browser extensions like [Tampermonkey][tampermonkey] to install this script from URL: `https://cdn.jsdelivr.net/npm/@spxx/userscript/dist/bundle.user.js`

### SPXX Web Dashboard™

Replacing the SPX Discord Bot™, the SPXX Web Dashboard™ Provides means for a selection of trusted individuals to translate the summaries of _Minecraft: Java Edition_ bugs. Also, it provides a list of Minecraft.net blogs for translators to navigate.

Translations done in the (SPXFellow-Hosted™ SPXX Web Dashboard™)™ is not yet accessible at [https://spx.spgoding.com/bugs][bugs], and
will be utilized by the SPXX User Script™ to auto translate the "Fixed bugs" section in _Minecraft: Java Edition_.

## Credits

- [SPGoding](https://github.com/SPGoding) - maintained the OG spx.
- [RicoloveFeng](https://github.com/RicoloveFeng) - maintains [minecraft.net-translations](https://github.com/RicoloveFeng/minecraft.net-translations/blob/master/rawtable.csv).

## Contributing

Development environment: [Node.js LTS][node] and [Yarn][yarn]

This repo is a monorepo with multiple packages under `packages/`. Build commands live in each package:

- `@spxx/userscript` (userscript)
	- Install: `yarn`
	- Build: `yarn workspace @spxx/userscript run build`
	- Watch: `yarn workspace @spxx/userscript run watch`
	- Output: `packages/userscript/dist/bundle.user.js`

- `@spxx/tweeter` (server utilities)
	- Install: `yarn`
	- Build: `yarn workspace @spxx/tweeter run build`
	- Output: `packages/tweeter/out/`

Alternatively, build all workspaces:

- `yarn workspaces foreach -v run build`

Notes:

- Running `yarn run build` at the repo root will fail because the root `package.json` does not define a `build` script. Use workspace-specific commands above.
- This repo also includes `pnpm-workspace.yaml`, but the configured package manager is Yarn (`packageManager: yarn@4.0.0`). Prefer Yarn commands unless you intentionally use pnpm.

[markdown]: https://en.wikipedia.org/wiki/Markdown
[bugs]: https://spx.spgoding.com/bugs
[node]: https://nodejs.org/
[yarn]: https://yarnpkg.com/
[tampermonkey]: https://www.tampermonkey.net
[user-script]: https://spx.spgoding.com/user-script
