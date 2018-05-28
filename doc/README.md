# Visual Studio Code extension for nyan

## Nice-to-have features
- Jump to definition
- Find all references
- Intellisense: code completion
- Debugger support

## Development
The [VS Code documentation](https://code.visualstudio.com/docs/extensions/overview) is a good place to start learning about VS Code extensions.

The nyan extension currently only has passive components like syntax highlighting and language configuration.
This implies that debugging it is limited to starting VS Code with the extension files replaced.

In VS Code one can do this systematically by adding a debug configuration in `.vscode/launch.json`: `configurations` array
```json
{
    "type": "extensionHost",
    "request": "launch",
    "name": "Launch Extension",
    "runtimeExecutable": "${execPath}",
    "args": [
        "--extensionDevelopmentPath=${workspaceFolder}"
    ]
}
```
The debug view should show a "Launch Extension" option to start debugging the extension.

Note: _Debugging has to be restarted after making local changes._

## Publishing
The process of publishing a new version is described in [the VS Code documentation](https://code.visualstudio.com/docs/extensions/publish-extension).

The official extension will be published by the maintainers using the [`SFTtech` publisher](https://marketplace.visualstudio.com/manage/publishers/sfttech).
