# Changelog

All notable changes to the **MEMZone.WriteLog** module will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.8] - 2026-03-27

### Changed

- `[BREAKING]` Renamed module from `PSWriteLog` to `MEMZone.WriteLog`.
- `[BREAKING]` Renamed `Initialize-PSWriteLog` to `Initialize-WriteLog`.
- Build script auto-increments patch version by default; use `-VersionBump Minor` or `-VersionBump Major` to override.

### Added

- Automatic GitHub Release creation on tag push.
- `VersionBump` parameter in build script (`Major`, `Minor`, `Patch`) to auto-update the manifest version.
- `Last Modified` date in compiled module header, auto-set at build time.
- `Module Version` in compiled module header, auto-synced from manifest at build time.

### Fixed

- Single-character table cell values (e.g. ✓, ✗) are now centered within the column.
- `Write-LogBuffer` no longer warns on module import when log path is not yet initialized.
- Pester `PassThru` configuration for reliable test result reporting.
- GitHub Actions upgraded to Node.js 24 (`actions/checkout@v5`, `actions/upload-artifact@v5`).

## [1.0.0] - 2025-01-14

### Added

- `Initialize-WriteLog` - Module initialization with configurable log path, console output, debug logging, and size-based rotation.
- `Write-Log` - Structured logging with severity levels, dual console/file output, and rich formatting support.
- `Write-LogBuffer` - Buffered log flushing for improved I/O performance.
- `Test-LogFile` - Log directory/file creation and size-based rotation.
- `Format-Message` - Rich text formatting: Block, CenteredBlock, Line, InlineHeader, InlineSubHeader, Timeline, TimelineHeader, List, Table modes.
- `Write-FunctionHeaderOrFooter` - Debug-level function entry/exit tracing with parameter logging.
- `Invoke-WithAnimation` - Background runspace execution with animated console progress indicators (Spinner, Dots, Braille, Bounce, Box).
- `Invoke-WithStatus` - Synchronous execution with success/failure status indicators.
- Pester 5 unit tests.
- PSScriptAnalyzer validation.
- GitHub Actions CI/CD pipeline with automated PSGallery publishing.
- Build script supporting Analyze, Test, Build (compiled single-file), and Publish tasks.
