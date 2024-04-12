# eslint-plugin-import-absolute-parent-else-relative-path

A (zero-dependency!) eslint plugin that enforces absolute/relative imports on your
codebase. Plugin has autofix 🔧 ```--fix``` 

## Prerequisites

You must have a `baseUrl` defined in either `tsconfig.json` or `jsconfig.json`.
**This plugin does not currently work with `paths`!**

## How plugin works?

The plugin prohibits the use of relative path when importing from parent and above, only absolute path is allowed in such cases.
For example:
- We are in file: ```b/misc/button/index.ts```
- And trying to import data from ```b/misc/types.ts```
```
❌ ../types.ts
✅ b/misc/types.ts
🔧 ../types.ts -> b/misc/types.ts
```
Conversely, the plugin disallows importing by absolute path if we import a file at the same nesting level or lower.
For example:
- We are in file: ```b/misc/button/index.ts```
- And trying to import data from ```b/misc/button/Secondary/_.scss```
```
❌ b/misc/button/Secondary/_.scss
✅ ./Secondary/_.scss
🔧 b/misc/button/Secondary/_.scss -> ./Secondary/_.scss
```

## Setup

- `npm i --save-dev eslint-plugin-import-absolute-parent-else-relative-path`
- Add `eslint-plugin-import-absolute-parent-else-relative-path` to your
  eslint `plugins`
  section
-
Add `import-absolute-parent-else-relative-path/import-absolute-parent-else-relative-path`
to
your
eslint `rules` section

## License

MIT
