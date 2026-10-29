# public — agent guide

Static files Vite copies into the build unchanged (`dist/` → `out/`), served from the site root. Everything else the browser loads is bundled from `src/`.

## Files

- `favicon.svg`: the only asset. An original drawing (a gold pin flag and a white ball on a dark-green rounded square, brand colours `#004737` and `#b8974e`), referenced from `index.html` as `/favicon.svg`. No club logo, photograph or proprietary font is embedded anywhere in the repository (see [docs/brand.md](../docs/brand.md)).

## Rules

- Original drawings only: no club logos, photographs, or files taken from skolkovogolf.com. The wordmark is set in text in `src/styles/global.css`.
- Nothing here may carry data or personal information; it is public on the Pages URL.
- Keep the folder small. A new static file needs a reason the bundler cannot serve it (a PWA manifest or a robots file would qualify) and a line in [FILE_MAP.md](../FILE_MAP.md).
- The CSP in `scripts/build-static.sh` allows images from `'self'`, `data:` and `blob:` only; an asset here must not need anything else.

## Related

- [src/styles/AGENTS.md](../src/styles/AGENTS.md) for brand tokens, [scripts/AGENTS.md](../scripts/AGENTS.md) for the build that copies this folder.
- Inherits every invariant and the workflow from the root [AGENTS.md](../AGENTS.md) (money, permissions, one fact in one place, quiet notifications, fictional data, English and Russian).
