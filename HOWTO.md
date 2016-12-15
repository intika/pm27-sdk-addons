### Here is how to modify Firefox SDK-based addon to run in Pale Moon 27 by the example of RES (Reddit Enhancement Suite) with detailed comments.

* First, as usual, we should edit install.rdf to [change targetApplication and its minVersion & maxVersion](https://github.com/JustOff/pm27-sdk-addons/commit/628fc02ade5b466397870add422f400bb8eaf1af) to allow installation into Pale Moon. There we also will [change the addon's id and version](https://github.com/JustOff/pm27-sdk-addons/commit/684e56e50353bf539aff57de08aa46969ad1481f) to avoid the unwanted updates in the future. The last should be also applied to package.json to keep it in sync. At the same time we can [update the name and so on](https://github.com/JustOff/pm27-sdk-addons/commit/45eeb730d6ea6a0a80e8b56f3620679da9eea984), however it isn't necessarily.

* Next our target is bootstrap.js. Here we should [change COMMONJS_URI](https://github.com/JustOff/pm27-sdk-addons/commit/33dee057513abb00a21ece2266298cb42170f7e5) to specify correct path to the Jetpack modules embedded in browser, because it different for Firefox and Pale Moon.

It would seem this is enough, but Pale Moon will refuse to install the extension at this point. This is because the Addon Manager detects package.json inside XPI and therefore understands that it's SDK-based extension, which doesn't allowed.

* So, let's deceive it. As we can see from addon's bootstrap.js the actual loader is located at /sdk/addon/bootstrap.js and it looking for package.json at the rootURI. To satisfy this query we can simple [rename package.json](https://github.com/JustOff/pm27-sdk-addons/commit/bc8b618f653e29136f6c153c7879593ba0eb1c78) (for example to fackage.json) and redirect request to the real file to the fake one using chrome.manifest. We will use the unique name reddites to construct path to the root of our extension in [chrome.manifest](https://github.com/JustOff/pm27-sdk-addons/commit/a80ad1bd282abcdad6b01e9fca720d9c19fe58f5) and then [update rootURI](https://github.com/JustOff/pm27-sdk-addons/commit/634540ee06234f4e81d7c031e1fd87868ea74a9d) in bootstrap.js.

The resulting extension can be successfully installed into the browser, but unfortunately doesn't work. It is sad but expected result, because the addon uses sdk/ui/button/toggle call which known to be currently inconsistent with Pale Moon 27, along with many other APIs related to the browser interface. 

* Fortunately the main functionality of RES can be used even without UI, so we can just [disable ToggleButton in index.js](https://github.com/JustOff/pm27-sdk-addons/commit/dfcaf6c3f53f1636853c8683b4d09d1d3a53fdd1). And the final touch: we [disable styleSheetButton and updatedURL call on first run](https://github.com/JustOff/pm27-sdk-addons/commit/eb7fecccfb395d0e0f4f21ea05cd3e546d3e841c) and [restore missed icon.png](https://github.com/JustOff/pm27-sdk-addons/commit/58cbef30146d71067bcfabe409ff06ed71b1876c).

Further testing shows the full operability of addon. The only error was found in console when trying disable it or uninstall. It means that extension is unable to correctly release their hooks and memory and requires browser restart.

:collision: The main problem remains in that I don't know the way how to debug and/or fix such errors without debugger for bootstrapped code, but the [embedded Add-on Debugger](https://developer.mozilla.org/en-US/Add-ons/Add-on_Debugger$revision/600731) isn't workable in Pale Moon 27 for now. However if we find such tool we will be able to revive embedded Jetpack completely and open the opportunity to run any SDK-based addons. The related discussion is [here](https://forum.palemoon.org/viewtopic.php?f=46&t=14157).