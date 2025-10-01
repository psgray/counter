# Release Process

1. Merge PRs into `main` (CI must pass).
2. Tag a release:
   ```bash
   git tag v1.0.0
   git push origin v1.0.0
   ```
3. GitHub Actions builds all artifacts.
4. Draft changelog is updated by Release Drafter.
5. Publish the release in GitHub UI.
