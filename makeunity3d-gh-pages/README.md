# MakeUnity3D

A jquery plugin to easily embed Unity games into your website.

## Usage

* Import this plugin: `<script type="text/javascript" src="../js/jquery.makeunity3d.js"></script>
`
* Add a div element where your game should be embedded: `<div class="unityPlayer" data-options='{"url": "DotUnity3dURL"}'></div>`
* Call `makeUnity3D()` on the div: `$(".unityPlayer").makeUnity3D();` (probably inside `$(document).ready(function()...` or similar).

That's it.

### Iframe

Alternatively you can embed the webplayer in an iframe. Simply use `//theoddler.github.io/makeunity3d/embed.html` as a source, adding options as needed:

`<iframe src="//theoddler.github.io/makeunity3d/embed.html?url=url to your .unity3d file&event=click width="600" height="350"></iframe>`

All options can be added to `src`.

## Options

Options can be added on two levels.

* In the `data-options` attribute of the div.
* As parameter for the `makeUnity3D` function.

Options set as parameter in makeUnity3D will override the default for all divs instantiated with that call. Options set in the attribute will take preference over any other.

The options that can be specified (name [default]: description)

* url [""]: The URL of the .unity3d objects. Required.
* event [null]: When the game should be loaded. Eg. 'mouseover'. If null the game will be loaded when the page is loaded.
* addMissingHtml [true]: Whether the some html should be placed in case unity is missing.

You can also add any options defined by Unity, most importantly:

* width [800]
* height [450]
* disableContextMenu [true]
