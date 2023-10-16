# bypass-youtube-adblock-blocker
A guide to blocking YouTube's anti-adblocking nonsense

# What does this work on?
PC. You need to be using a browser like Firefox or Chrome

# How do I do it?

1. Install uBlock Origin: [Firefox](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/) [Chrome/Edge](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
2. Open uBlock's settings, enable ALL filter lists and click "Apply changes"
3. Update their filter lists by clicking "Purge all caches" and then "Update now". Then, click "Apply changes" (if it isn't grayed out)
4. Download Request Interceptor: [Firefox](https://addons.mozilla.org/en-US/firefox/addon/request-interceptor/) [Chrome/Edge](https://chrome.google.com/webstore/detail/request-interceptor/bfgblailifedppfilabonohepkofbkpm). Open the extension.
5. Click "New Rule Group" and create a new rule. Set it to "When Request's URL matches (regex)". Set the top box to `https://www.youtube.com/s/desktop/[A-Za-z0-9]+/jsbin/desktop_polymer_enable_wil_icons.vflset/desktop_polymer_enable_wil_icons.js`
6. Set the action to "Redirect to" and set the URL to `https://raw.githubusercontent.com/psychon-night/bypass-youtube-adblock-blocker/main/desktop_polymer_enable_wil_icons.js`
7. Create another rule, set it to "When request's URL equals". Set the top box to `https://raw.githubusercontent.com/psychon-night/bypass-youtube-adblock-blocker/main/desktop_polymer_enable_wil_icons.js`
8. Set the second rule's action to `modify response header`. Set the "name" box to `content-type` and the value to `text/javascript`
9. SAVE your rules, then ENABLE them

Once you're finished, it should look something like [this image](https://github.com/psychon-night/bypass-youtube-adblock-blocker/blob/main/Screenshot%20from%202023-10-16%2015-50-02.png)

# I don't want to do it manually...
Starting from newer versions of Request Interceptor, you can IMPORT rules. Download [this JSON file](https://github.com/psychon-night/bypass-youtube-adblock-blocker/blob/main/request-interceptor-rules.json) and click IMPORT on the request interceptor page. Then, upload the JSON file
