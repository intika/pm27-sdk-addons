### :heavy_exclamation_mark: SDK-based add-ons can be run in Pale Moon 27.1, but they should be [properly adapted](https://github.com/JustOff/pm27-sdk-addons/blob/master/PMkit.md).

| Original Extension | Pale Moon 27.1 Compatibility Status | Alternative (non-SDK) |
| -------------- | ----------------------------------- | ----------- |
| [Add URL to Window Title](https://addons.mozilla.org/addon/add-url-to-window-title/) | [✓] Supported since [1.03](https://addons.mozilla.org/en-US/firefox/addon/add-url-to-window-title/versions/1.03) | [[1]](https://addons.mozilla.org/addon/customize_titlebar_v2/) |
| [cliget](https://addons.mozilla.org/addon/cliget/) | Support request was [accepted](https://github.com/zaidka/cliget/pull/43), awaiting for release | Unknown |
| [Close last tab with middle-click](https://addons.mozilla.org/addon/close-last-tab-with-middle-/) | [✓] Replaced by [Close last tab with middle-click](https://forum.palemoon.org/viewtopic.php?p=99210#p99210) (non-SDK) | Unknown |
| [Decentraleyes](https://addons.mozilla.org/addon/decentraleyes/) | [✓] Supported since [1.3.7](https://addons.palemoon.org/extensions/decentraleyes/) | Unknown |
| [Emoji Cheatsheet](https://addons.mozilla.org/addon/emoji-cheatsheet/) | Support request was [accepted](https://github.com/johannhof/emoji-helper/pull/83), awaiting for release | Unknown |
| [Enter Selects](https://addons.mozilla.org/addon/enter-selects/) | Support request was [sent](https://github.com/Mardak/enterSelects/pull/17) | Unknown |
| [I don't care about cookies](https://addons.mozilla.org/addon/i-dont-care-about-cookies/) | Support request was sent via e-mail (2017.01.24) <sup>[[*]](#testing)</sup> | [[1]](https://www.kiboke-studio.hr/i-dont-care-about-cookies/abp/) |
| [Load from Cache](https://addons.mozilla.org/addon/load-from-cache/) | [✓] Replaced by [Greedy Cache](https://addons.palemoon.org/extensions/greedy-cache/) (non-SDK) | Unknown |
| [Play/Pause](https://addons.mozilla.org/en-US/firefox/addon/play-pause/) | [✓] Supported since [1.2.2](https://addons.mozilla.org/en-US/firefox/addon/play-pause/versions/1.2.2) | Unknown |
| [Reddit Enhancement Suite](https://addons.mozilla.org/addon/reddit-enhancement-suite/) | Add-on should be forked based on [4.6.1](https://addons.mozilla.org/en-US/firefox/addon/reddit-enhancement-suite/versions/4.6.1) <sup>[[*]](#testing)</sup> | [[1]](http://userscripts-mirror.org/scripts/show/82915) |
| [Reload Plus](https://addons.mozilla.org/addon/reload-plus/) | [✓] Supported since [5.2.0](https://addons.mozilla.org/en-US/firefox/addon/reload-plus/versions/5.2.0) | Unknown |
| [Scroll To Top](https://addons.mozilla.org/addon/scroll-to-top/) | Support request was [accepted](https://github.com/pratikabu/scrolltotop/pull/52), awaiting for release <sup>[[*]](#testing)</sup> | Unknown |
| [Send Tab to Device](https://addons.mozilla.org/addon/send-tab-to-device/) | [✓] Forked as [Send Tab to Device (Moon Edition)](https://github.com/JustOff/send-tab-to-device) | Unknown |
| [Self-Destructing Cookies](https://addons.mozilla.org/addon/self-destructing-cookies/) | [✓] Use alternatives or make a fork based on [0.4.11](https://addons.mozilla.org/en-US/firefox/addon/self-destructing-cookies/versions/0.4.11) <sup>[[*]](#testing)</sup> | [[1]](https://addons.mozilla.org/addon/cookies-exterminator/), [[2]](https://addons.palemoon.org/extensions/privacy-and-security/crush-those-cookies/) |
| [signTextJS plus](https://addons.mozilla.org/addon/signtextjs-plus/) | Add-on should be forked based on [0.8.6](https://addons.mozilla.org/en-US/firefox/addon/signtextjs-plus/versions/0.8.6) <sup>[[*]](#testing)</sup> | Unknown |
| [StylRRR](https://addons.mozilla.org/addon/stylrrr/) | Add-on should be forked based on [0.1.4](https://addons.mozilla.org/en-US/firefox/addon/stylrrr/versions/0.1.4) <sup>[[*]](#testing)</sup> | [[1]](https://addons.mozilla.org/addon/stylish/) |
| [YouTube ALL HTML5](https://addons.mozilla.org/addon/youtube-all-html5/) | [✓] Supported since  [3.1.1](https://addons.mozilla.org/en-US/firefox/addon/youtube-all-html5/versions/3.1.1) | [[1]](https://greasyfork.org/en/scripts/search?q=youtube) |
| [YouTube No Buffer](https://addons.mozilla.org/addon/youtube-no-buffer/) | [✓] Replaced by [YouTube Lazy Load](https://addons.palemoon.org/extensions/youtube-lazy-load/) (non-SDK) | Unknown |
<sup><a name="testing">[*]</a> : &nbsp;Can be temporarily installed using [Moon Tester Tool](https://addons.palemoon.org/extensions/moon-tester-tool/)<br><br><hr>

#### Below is the set of SDK-based extensions patched to run in Pale Moon 27.0

According to the **official position of the Pale Moon development team**, such patching should be considered as hacking, and they cannot and **will not provide any guarantees** that anything will work or keep working; **nor** will they provide **any support for anyone running an SDK extension** that has been hacked to make it to run with the toolkit modules. **That includes all support, also for general browser use**, because SDK-sourced extensions may break the browser if forced to run.

Please, use these addons only as last resort measure! Better ask the developer of the original version to provide non SDK-based solution. Don't try to install all from the list or the extension you never used before. [See also ...](https://forum.palemoon.org/viewtopic.php?f=16&t=13745)

| Original extension | Fix for PM27.0 | Status | Alternative |
| ------------------ | ------------ | ------ | ----------- |
| [Add URL to Window Title](https://addons.mozilla.org/addon/add-url-to-window-title/) | [Download](https://github.com/JustOff/pm27-sdk-addons/releases/download/0.0.1/add_url_to_window_title_advanced_keepass_usage-1.01-pm27.xpi) | Fully functional <sup>[[±]](#restart)</sup> | [[1]](https://addons.mozilla.org/addon/customize_titlebar_v2/) |
| [Decentraleyes](https://addons.mozilla.org/addon/decentraleyes/) | [Download](https://github.com/JustOff/pm27-sdk-addons/releases/download/0.0.1/decentraleyes-1.3.7-pm27.xpi) | Fully functional <sup>[[±]](#restart)</sup><sup>[[#]](#unstable)</sup> | Unknown |
| [I don't care about cookies](https://addons.mozilla.org/addon/i-dont-care-about-cookies/) | [Download](https://addons.palemoon.org/extensions/i-dont-care-about-cookies/) | Core functional, context menu disabled <sup>[[±]](#restart)</sup> | [[1]](https://www.kiboke-studio.hr/i-dont-care-about-cookies/abp/) |
| [Reddit Enhancement Suite](https://addons.mozilla.org/addon/reddit-enhancement-suite/) | [Download](https://github.com/JustOff/pm27-sdk-addons/releases/download/0.0.1/reddit_enhancement_suite-4.6.1-pm27.xpi) | Core functional, button disabled <sup>[[±]](#restart)</sup> | [[1]](http://userscripts-mirror.org/scripts/show/82915) |
| [Reload Plus](https://addons.mozilla.org/addon/reload-plus/) | [Download](https://github.com/JustOff/pm27-sdk-addons/releases/download/0.0.1/reload_plus-5.1.0-pm27.xpi) | Fully functional <sup>[[±]](#restart)</sup> | Unknown |
| [Scroll To Top](https://addons.mozilla.org/addon/scroll-to-top/) | [Download](https://github.com/JustOff/pm27-sdk-addons/releases/download/0.0.1/scroll_to_top-4.5.5-pm27.xpi) | Fully functional <sup>[[±]](#restart)</sup> | Unknown |
| [Self-Destructing Cookies](https://addons.mozilla.org/addon/self-destructing-cookies/) | [Download](https://github.com/JustOff/pm27-sdk-addons/releases/download/0.0.1/self_destructing_cookies-0.4.11-pm27.xpi) | Core functional, icon and menu disabled <sup>[[±]](#restart)</sup> | [[1]](https://addons.mozilla.org/addon/cookies-exterminator/), [[2]](https://addons.palemoon.org/extensions/privacy-and-security/crush-those-cookies/) |
| [signTextJS plus](https://addons.mozilla.org/addon/signtextjs-plus/) | [Download](https://github.com/JustOff/pm27-sdk-addons/releases/download/0.0.1/signtextjs_plus-0.8.6-pm.xpi) | Fully functional <sup>[[±]](#restart)</sup> | Unknown |
| [YouTube ALL HTML5](https://addons.mozilla.org/addon/youtube-all-html5/) | [Download](https://github.com/JustOff/pm27-sdk-addons/releases/download/0.0.1/youtube_all_html5-3.0.3-pm27.xpi) | Fully functional | [[1]](https://greasyfork.org/en/scripts/search?q=youtube) |
<sup><a name="restart">[±]</a> : &nbsp;Manual browser restart required, on disable or uninstall<br>
<a name="unstable">[#]</a> : &nbsp;Browser freezes and crashes were reported by some users</sup>

This software is provided by the copyright holders and contributors "as is" and any express or implied warranties, including, but not limited to, the implied warranties of merchantability and fitness for a particular purpose are disclaimed. In no event shall the copyright owner or contributors be liable for any direct, indirect, incidental, special, exemplary, or consequential damages (including, but not limited to, procurement of substitute goods or services; loss of use, data, or profits; or business interruption) however caused and on any theory of liability, whether in contract, strict liability, or tort (including negligence or otherwise) arising in any way out of the use of this software, even if advised of the possibility of such damage.
