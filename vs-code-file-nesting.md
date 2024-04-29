# VSCode: File nesting (grouping)

- Flutter/Dart related generic config files (nest under `pubspec.yaml`)
- Git related files (nest under `.gitignore`)
- Readme files (`.md`)

How to set it up:

- Open VS Code palete `cmd + shift + P`
- Type `Open Settings (JSON)`
- Insert the code below in to setting.json

``` JSON
{
  "explorer.fileNesting.enabled": true,
  "explorer.fileNesting.expand": false,
  "explorer.fileNesting.patterns": {
    "pubspec.yaml": ".flutter-plugins, .packages, .dart_tool, .flutter-plugins-dependencies, .metadata, .packages, pubspec.lock, build.yaml, analysis_options.yaml, all_lint_rules.yaml",
    ".gitignore": ".gitattributes, .gitmodules, .gitmessage, .mailmap, .git-blame*",
    "readme.*": "authors, backers.md, changelog*, citation*, code_of_conduct.md, codeowners, contributing.md, contributors, copying, credits, governance.md, history.md, license*, maintainers, readme*, security.md, sponsors.md",
    "*.dart": "$(capture).g.dart, $(capture).freezed.dart",
  }
}
```
