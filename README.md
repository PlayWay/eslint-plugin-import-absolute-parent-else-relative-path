# eslint-plugin-import-absolute-parent-else-relative-path

A (zero-dependency!) eslint plugin that enforces absolute imports on your
codebase.

## Prerequisites

You must have a `baseUrl` defined in either `tsconfig.json` or `jsconfig.json`.
**This plugin does not currently work with `paths`!**

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
