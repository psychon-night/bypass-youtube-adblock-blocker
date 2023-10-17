# bypass-youtube-adblock-blocker
A guide to blocking YouTube's anti-adblocking nonsense

# Supported Environments
- PC (Windows, Linux, Mac), using Firefox, Chrome, Edge, or another [chromium-based browser](https://en.wikipedia.org/wiki/Chromium_(web_browser)#Browsers_based_on_Chromium)
- Android using Firefox or Chrome*

* Untested, results may vary

# Pre-Requisites
- Fully up-to-date browser
- Chrome extensions enabled (Edge only, see [this page](https://support.microsoft.com/en-us/microsoft-edge/add-turn-off-or-remove-extensions-in-microsoft-edge-9c0ec68c-2fbc-2f2c-9ff0-bdc76f46b026#:~:text=Chrome))
- uBlock Origin: [Firefox](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/) [Chrome/Edge/Chromium](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- Request Interceptor: [Firefox](https://addons.mozilla.org/en-US/firefox/addon/request-interceptor/) [Chrome/Edge/Chromium](https://chrome.google.com/webstore/detail/request-interceptor/bfgblailifedppfilabonohepkofbkpm)

# How do I do it?

1. Open uBlock's settings and go to `Filter lists`. Make sure all filter lists are enabled, then click `Apply Changes`
2. Click `Purge all caches`, then hit `Update now`. Wait for all filter lists to be updated
3. Open Request Interceptor's settings. Sometimes this doesn't work. Please check [this section]() for help
4. Download [this JSON file](https://github.com/psychon-night/bypass-youtube-adblock-blocker/blob/main/request-interceptor-rules.json)
5. On Request Interceptor's settings, hit IMPORT. Select the JSON file you downloaded and upload it
6. Two rules should have appeared. Make sure they are both set to ON. There is also an additional toggle in the top-right of the page, make sure that is also enabled.
7. Click SAVE in the top-right of the screen
8. Go to any YouTube video and press the Ctrl, Shift, and R keys at the same time (you only need to do this the first time)

Once you're finished, it should look something like [this image](https://github.com/psychon-night/bypass-youtube-adblock-blocker/blob/main/Screenshot%20from%202023-10-16%2015-50-02.png)

# JSON didn't work
1. Open Request Interceptor. Sometimes this doesn't work. Try [this link (Firefox)](moz-extension://411c0429-1f7b-4a20-b4c5-9b9a6f8b8524/index.html) or [this link (Chromium)](chrome-extension://bfgblailifedppfilabonohepkofbkpm/index.html)
2. Click "New Rule Group" and create a new rule. Set it to "When Request's URL matches (regex)". Set the top box to `https://www.youtube.com/s/desktop/[A-Za-z0-9]+/jsbin/desktop_polymer_enable_wil_icons.vflset/desktop_polymer_enable_wil_icons.js`
6. Set the action to "Redirect to" and set the URL to `https://raw.githubusercontent.com/psychon-night/bypass-youtube-adblock-blocker/main/desktop_polymer_enable_wil_icons.js`
7. Create another rule, set it to "When request's URL equals". Set the top box to `https://raw.githubusercontent.com/psychon-night/bypass-youtube-adblock-blocker/main/desktop_polymer_enable_wil_icons.js`
8. Set the second rule's action to `modify response header`. Set the "name" box to `content-type`, and the "value" box to `text/javascript`
9. SAVE and ENABLE your rules
10. Go to any YouTube video and press the Ctrl, Shift, and R keys at the same time (you only need to do this the first time)

Happy YouTubing!

# HELP! Request Inteceptor's settings won't open!!

This is a known issue, the extension is poorly designed
For Firefox, open this link: moz-extension://411c0429-1f7b-4a20-b4c5-9b9a6f8b8524/index.html
For Chrome, Edge, and Chromium, use this link: chrome-extension://bfgblailifedppfilabonohepkofbkpm/index.html
