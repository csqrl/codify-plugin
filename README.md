<!-- Links -->

[repo/homepage]: https://github.com/csqrl/codify-plugin
[repo/releases]: https://github.com/csqrl/codify-plugin/releases
[repo/contributors]: https://github.com/csqrl/codify-plugin/graphs/contributors
[plugin/toolbox]: https://roblox.com/library/4749111907
[plugin/itch]: https://csqrl.itch.io/codify
[plugin/github]: https://github.com/csqrl/codify-plugin
[devhub/managing-plugins]: https://developer.roblox.com/en-us/articles/Intro-to-Plugins#finding-and-managing-plugins
[roact/repo]: https://github.com/roblox/roact
[fusion/repo]: https://github.com/elttob/fusion
[csqrl/github]: https://github.com/csqrl
[boatbomber/github]: https://github.com/boatbomber
[boatbomber/site]: https://www.boatbomber.com
[boatbomber/site/donate]: https://www.boatbomber.com/#h.aiqhaejpfy6p

<!-- Images -->

[image/cover]: assets/Cover.png
[image/plugin-screenshots]: assets/PluginScreenshots.png
[image/get/itch]: https://raw.githubusercontent.com/gist/csqrl/56c5f18b229ca1e61feb6eb5fb149f43/raw/itch.svg
[image/get/github]: https://raw.githubusercontent.com/gist/csqrl/56c5f18b229ca1e61feb6eb5fb149f43/raw/github.svg
[image/get/roblox]: https://raw.githubusercontent.com/gist/csqrl/56c5f18b229ca1e61feb6eb5fb149f43/raw/robloxSmall.svg

<div align="center">

[![Cover][image/cover]][plugin/itch]

✨ Convert Instances to code; just like magic!

[![Get on Itch][image/get/itch]][plugin/itch]
[![Get on Github][image/get/github]][repo/releases]

</div>

Codify _(formerly Roactify)_ is a collaborative project between [@boatbomber][boatbomber/github] and [@csqrl][csqrl/github], which converts your pre-existing Roblox Instances into code (v2.1.0 supports all Instances!).

Whether you work with vanilla Instances, or use a framework like [Roact][roact/repo] or [Fusion][fusion/repo], Codify has you covered!

# Installation

Codify is 100% free to download, but if you like this plugin, please **consider sponsoring** via the "Sponsor this project" panel!

> This project wouldn't have been possible without the help of [@boatbomber][boatbomber/github] and our [other contributors][repo/contributors]. If you'd like to show your support for [@boatbomber][boatbomber/github] too, follow the link below to find out how!
>
> [Learn more &rarr;][boatbomber/site/donate]

## itch.io

Help support plugin developers and download the latest version of Codify from itch.io!

[![Get on Itch][image/get/itch]][plugin/itch]

## Plugin Marketplace

The simplest way to install Codify is to install it from the plugin marketplace. This gives you access to the latest version of the plugin, and easy updates via the [Plugin Management][devhub/managing-plugins] window.

[![Get on Roblox][image/get/roblox]][plugin/toolbox]

## Manual Installation

Codify is an open-source plugin. New releases are automatically published to both the Roblox plugin marketplace and GitHub releases. If you'd rather install the plugin manually, download the latest binary (`.rbxm` or `.rbxmx`) from the [releases page][repo/releases], and drop it into your Studio plugins directory.

[![Get on GitHub][image/get/github]][repo/releases]

# Overview of Permissions

## HTTP Requests

Codify uses HTTP requests to fetch the latest information about Roblox Instances. This is **required** to enable core plugin functionality, as this is not possible without access to API dumps.

Below is a list of URLs used by Codify _(all requests are unauthenticated)_:

- `https://s3.amazonaws.com/setup.roblox.com/DeployHistory.txt`
- `https://s3.amazonaws.com/setup.roblox.com/versionQTStudio`
- `https://s3.amazonaws.com/setup.roblox.com/version-{{hash}}-API-Dump.json`
- `https://api.github.com/repos/csqrl/codify-plugin/contributors?anon=1`

## Script Injection

This is a completely optional permission and will not degrade functionality if disabled. You will only be prompted for this permission when selecting the **Save to Device** button.

This is necessary to the Save to Device feature only. The plugin will _temporarily_ create a ModuleScript inside of ServerStorage that will be used to prompt to save a file to your device. The ModuleScript will be **destroyed immediately** after closing the save dialogue.

- Temporary scripts are also unarchivable (`.Archivable` property set to `false`). This means that they will not be saved when (auto-)saving your project, or saving/publishing to Roblox.

# Screenshots

|                                Watch Codify in action on YouTube                                 |
| :----------------------------------------------------------------------------------------------: |
|                                   https://youtu.be/aLFWPKNiBGU                                   |
| [![Video Thumbnail](https://img.youtube.com/vi/aLFWPKNiBGU/0.jpg)](https://youtu.be/aLFWPKNiBGU) |

![Screenshot of the Plugin][image/plugin-screenshots]

## Open Source Projects

The following open-source projects helped to make Codify possible!

- [highlighter](https://github.com/boatbomber/highlighter) by @boatbomber
- [studio-plugin](https://github.com/csqrl/studio-plugin) by @csqrl
- [studio-theme](https://github.com/csqrl/studio-theme) by @csqrl
- [roblox-lua-promise](https://github.com/evaera/roblox-lua-promise) by @evaera
- [roact-hooks](https://github.com/kampfkarren/roact-hooks) by @kampfkarren
- [roact-router](https://github.com/reselim/roact-router) by @reselim
- [roact](https://github.com/roblox/roact) by @roblox
- [rodux](https://github.com/roblox/rodux) by @roblox
- [rodux-hooks](https://github.com/solarhorizon/rodux-hooks) by @solarhorizon
- [sift](https://github.com/csqrl/sift) by @csqrl

## Disclaimer

The code Codify produces is not 100% perfect. You should consider that the snippets produced are not optimal, but that shouldn't put you off using it!
