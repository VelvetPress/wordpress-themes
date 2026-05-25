# velvetpress-themes

Open-source WordPress themes published through [VelvetPress](https://velvetpress.dev) — push to `main` and connected WordPress sites receive the update through the native wp-admin update system.

## Themes

| Theme | Description | Path |
|-------|-------------|------|
| VelvetPress Starter | Minimal block theme shell — install the VelvetPress plugin alongside it for update management | [`velvetpress-starter/`](velvetpress-starter/) |

## Local development

Each theme is a standard WordPress block theme. To work on one locally, symlink or copy the theme directory into your WordPress install's `wp-content/themes/`:

```bash
ln -s "$(pwd)/velvetpress-starter" /path/to/wp-content/themes/velvetpress-starter
```

## Publishing a release

Releases are triggered by a push to `main` after bumping the theme's `Version:` header in `style.css`. The VelvetPress backend picks up the webhook and publishes the new ZIP.

See [Publishing a plugin or theme](https://velvetpress.dev/docs/publishing-a-plugin-or-theme) for the full release flow.
