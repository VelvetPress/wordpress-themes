# Changelog

All notable changes to VP Starter Theme will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.5.0] - 2026-02-14

### Changed
- All VelvetPress update logic moved to the standalone VelvetPress plugin
- Removed all VelvetPress functions from functions.php (settings, update checker, registration, reporting, PUC library)
- Theme is now a minimal block theme shell — install the VelvetPress plugin for update management

### Removed
- `plugin-update-checker/` library (now bundled in the VelvetPress plugin)
- `velvetpress_get_settings()`, `velvetpress_starter_init_update_checker()`, `velvetpress_report_version()`, `velvetpress_register_site()`, settings page functions

### Migration
- Install and activate the VelvetPress plugin before or after updating the theme
- Existing `velvetpress_settings` option is reused by the plugin — no reconfiguration needed

## [1.4.2] - 2026-02-07

### Added
- Site self-registration: theme calls POST /register on settings save
- Automatic version reporting: theme calls POST /report hourly (throttled via transient)
- Dashboard now shows per-site theme version, WordPress version, and last seen timestamp

## [1.4.1] - 2026-02-06

### Changed
- Test release to verify automatic update flow

## [1.4.0] - 2026-02-06

### Added
- Admin settings page (Appearance → VelvetPress Updates)
- Connection status indicator with auto-check on page load
- /ping API endpoint for connection testing
- Debug info panel for troubleshooting

### Changed
- API credentials now stored in database (or wp-config.php)
- CORS headers added to all API responses

## [1.3.0] - 2026-02-05

### Changed
- Update checker now uses secure API with key + domain validation
- Downloads use pre-signed S3 URLs (no public bucket access)

### Security
- API key required for update checks
- Domain validation prevents key sharing across unauthorized sites

## [1.2.0] - 2026-02-03

### Added
- Front page template with hero section
- Theme screenshot

## [1.1.1] - 2026-02-03

### Changed
- Test update to verify update flow works

## [1.1] - 2026-02-03

### Added
- GitHub Actions workflow for automated releases
- S3-based update distribution

## [1.0] - 2026-02-03

### Added
- Initial release
- Minimal block theme structure (style.css, theme.json, templates/index.html)
- Update checker integration for S3-based updates
- Docker Compose setup for local development
