# Vscode action to release a plugin

This Action tries to release a vscode plugin via the [vsce](https://github.com/microsoft/vscode-vsce) tool.

Make sure to pass a PUBLISH_TOKEN an explanation on how to register a token can be found [here](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)

## 🔑 Secrets

- PUBLISH_TOKEN - Required to publish a release to vscode Marketplace

## 💻 Examples

Trigger a release

```hcl

workflow "Release Vscode plugin" {
  on = "release"
  resolves = ["Release Vscode"]
}

action "WebPageTestActions" {
  secrets = [
    "GITHUB_TOKEN",
    "PUBLISH_TOKEN",
  ]
}

```
