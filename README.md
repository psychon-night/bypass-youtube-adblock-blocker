# bypass-youtube-adblock-blocker
A guide to blocking YouTube's anti-adblocking nonsense

# What does this work on?
PC. You need to be using a browser like Firefox or Chrome

# How do I do it?

1. Install uBlock Origin: [Firefox](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/) [Chrome/Edge](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
2. Open uBlock's settings, enable ALL filter lists and click "Apply changes"
3. Update their filter lists by clicking "Purge all caches" and then "Update now". Then, click "Apply changes" (if it isn't grayed out)
4. Download Request Interceptor: [Firefox](https://addons.mozilla.org/en-US/firefox/addon/request-interceptor/) [Chrome/Edge](https://chrome.google.com/webstore/detail/request-interceptor/bfgblailifedppfilabonohepkofbkpm)
5. Click "New Rule Group" and create a new rule. Set it to "When Request's URL equals"
6. Open [this document](https://pastefy.app/G1Txv5su/raw) and copy the bottom-most URL (it ends with .js). At the time of writing, this is `https://www.youtube.com/s/desktop/000d7185/jsbin/desktop_polymer_enable_wil_icons.vflset/desktop_polymer_enable_wil_icons.js`
7. Paste the URL into the "equals" (top) box of the rule you created
8. In the bottom box, paste `https://www.youtube.com/s/desktop/38b2ce1b/jsbin/desktop_polymer_enable_wil_icons.vflset/desktop_polymer_enable_wil_icons.js`
9. Click SAVE and ENABLE your new filter rule
10. Reload YouTube using `Ctrl+Shift+R`

# The YouTube URL you gave us doesn't work!!!! HELP!!!
It's possible YouTube did some stupid bullshit and pulled that file off their server. Oh well.

Use `https://raw.githubusercontent.com/psychon-night/bypass-youtube-adblock-blocker/main/desktop_polymer_enable_wil_icons.js` instead. They can't take that down ;)
