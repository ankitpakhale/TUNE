# GitHub Repository Setup

## Branch Strategy

TUNE uses the following branch strategy:

1. **main** - Production branch containing stable releases
2. **develop** - Development branch for integrating features
3. **feature/feature-name** - Feature branches for new functionality
4. **bugfix/bug-description** - Bugfix branches for specific issues
5. **release/vX.Y.Z** - Release branches for preparing new versions

## Branch Protection Rules

Set up the following branch protection rules in GitHub:

### For `main` branch:

- Require pull request reviews before merging
- Require status checks to pass before merging
  - Require the "build" status check
  - Require the "build-android" status check
- Require branches to be up to date before merging
- Do not allow bypassing the above settings
- Restrict who can push to matching branches (Limit to maintainers)

### For `develop` branch:

- Require pull request reviews before merging
- Require status checks to pass before merging
  - Require the "build" status check
- Require branches to be up to date before merging
- Allow force pushes (by maintainers only)

## Workflow

1. Create feature/bugfix branches from `develop`
2. Work on your feature or fix
3. Submit PR to `develop`
4. After review and approval, merge to `develop`
5. For releases:
   - Create a release branch from `develop`
   - Prepare final changes, version bumps
   - Submit PR to `main`
   - After approval, merge to `main`
   - Tag the release with version number
   - Merge `main` back to `develop`

## CI/CD Workflow

The GitHub Actions workflow defined in `.github/workflows/flutter-ci.yml` will:

1. Run for all PRs targeting `main` or `develop`
2. Check code quality with Flutter analyze
3. Run tests
4. Build debug APK for Android

For more complex CI/CD setup, consider using [Codemagic](https://codemagic.io/) or [Bitrise](https://www.bitrise.io/) for Flutter apps. 