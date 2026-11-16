# Publishing

Public source repository: https://github.com/wanyue1215/zed-liquid-glass.

1. Publish this directory in a dedicated public Git repository; do not upload the surrounding workspace or personal settings.
2. Set `repository` in `extension.toml` to its public HTTPS GitHub URL and verify the public author name.
3. Commit the final extension, install that exact commit as a dev extension, and check the theme picker, project-tree pinned folders, hover states, menus, editor, and terminal.
4. Fork `zed-industries/extensions` and add the public repository as the `extensions/liquid-glass-theme` submodule. Its commit must be reachable from a branch.
5. Add the following entry to the registry's `extensions.toml`:

```toml
[liquid-glass-theme]
submodule = "extensions/liquid-glass-theme"
version = "0.1.0"
```

6. Run `pnpm sort-extensions` in the registry repository and open a pull request. The registry publishes after maintainer acceptance and merge.

Review the registry for ID/name collisions and similar functionality before submitting. This is an adaptation of Glass with a distinct palette and material treatment; acceptance is at the maintainers' discretion.

Official guide: https://zed.dev/docs/extensions/publishing/publishing-guide
