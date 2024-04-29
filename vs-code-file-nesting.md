# VSCode: File Nesting (Grouping)

- Nest Flutter/Dart related generic config files under `pubspec.yaml`.
- Nest Git-related files under `.gitignore`.
- Nest Readme files (`.md`).
- Nest `package<-lock>.json`
- Next `env`ironmental files, such as .env, .env.local, .env.prod

How to set it up:

- Open VS Code palette with `Cmd + Shift + P`.
- Type `Open Settings (JSON)`.
- Insert the code below into `settings.json`.

``` JSON
{
 "explorer.fileNesting.enabled": true,
 "explorer.fileNesting.expand": false,
 "explorer.fileNesting.patterns": {
    "pubspec.yaml": ".flutter-plugins, .packages, .dart_tool, .flutter-plugins-dependencies, .metadata, .packages, pubspec.lock, build.yaml, analysis_options.yaml, all_lint_rules.yaml",
    ".gitignore": ".gitattributes, .gitmodules, .gitmessage, .mailmap, .git-blame*",
    "readme.*": "authors, backers.md, changelog*, citation*, code_of_conduct.md, codeowners, contributing.md, contributors, copying, credits, governance.md, history.md, license*, maintainers, readme*, security.md, sponsors.md",
    "*.dart": "$(capture).g.dart, $(capture).freezed.dart",
    "*.env": ".env.*",
    "package.json": "package-lock.json"
  }
}
```
