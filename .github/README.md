# GitHub Actions Configuration

## Disabling Expensive Runners

To save costs, macOS and Windows builds are **disabled by default**. Only Linux builds run automatically.

### To Enable macOS/Windows Builds

1. Go to your repository **Settings** → **Secrets and variables** → **Actions** → **Variables** tab
2. Add repository variables:
   - `ENABLE_MACOS_BUILDS` = `true` (to enable macOS builds)
   - `ENABLE_WINDOWS_BUILDS` = `true` (to enable Windows builds)

### Current Behavior

- ✅ **Linux builds**: Always enabled (free on GitHub Actions)
- ❌ **macOS builds**: Disabled by default (requires `ENABLE_MACOS_BUILDS=true`)
- ❌ **Windows builds**: Disabled by default (requires `ENABLE_WINDOWS_BUILDS=true`)

### What Still Works

Even with macOS/Windows disabled:

- ✅ Linting and code quality checks
- ✅ Linux builds and tests
- ✅ Release preview (semantic-release dry-run)
- ✅ All workflows remain configured and ready

### When to Enable

Enable macOS/Windows builds when:

- Preparing for a release
- Testing cross-platform compatibility
- You have available GitHub Actions minutes

The workflows are fully configured and will work immediately once you enable the variables.
