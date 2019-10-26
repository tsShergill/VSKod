# Blakod for Visual Studio Code

![pic](https://i.imgur.com/qDVHIfc.png)

## What's in the folder

This folder contains all of the files necessary for the extension.
* `package.json` - this is the manifest file that defines the location of the snippet file and specifies the language of the snippets.
* `kod.code-snippets.json` - the file containing all snippets. Used for autocomplete of functions.
* `kod.tmlLanguage.json` - the file containing syntax highlighting.

## Install

To start using the extension with Visual Studio Code copy this repo it into the /.vscode/extensions folder and restart Code.
- Windows: `%USERPROFILE%\.vscode\extensions`
- macOS: `~/.vscode/extensions`
- Linux: `~/.vscode/extensions`

Navigate to settings.json
- Windows: `%APPDATA%\Code\User\settings.json`
- macOS: `$HOME/Library/Application Support/Code/User/settings.json`
- Linux: `$HOME/.config/Code/User/settings.json`

Include the following line before.
```
    "[kod]": {
        "files.encoding" : "windows1252"
     }
```

### Hide .bof and .rsc in the file explorer.

To hide compiled kods, include the following in settings.json as well:

```
    "files.exclude": {
        "**/*.bof": { "when": "$(basename).kod"}
        "**/*.rsc": { "when": "$(basename).kod"}
    }
```
