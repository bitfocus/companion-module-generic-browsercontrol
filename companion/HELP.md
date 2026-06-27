# Browser Control

Control open instances of Chrome or Firefox via [Puppeteer](https://pptr.dev/) remote debugging.

> **Warning:** This module gives full automated access to your open browser window to potentially any device on your network. This means your saved data, cookies, history, open webpages, etc. It is strongly recommended for security reasons that you run this in a dedicated empty browser profile.

## Config
1. Start the browser with the steps below.
1. Select target browser from the module connection dropdown.
2. Enter the host IP address and remote debugging port.
3. (Optional) Set a keyword to match the target tab. This can also be set on a per-action basis.


### Chrome

Allow remote debugging in `chrome://inspect/#remote-debugging`. Optionally, create a new profile in the profile manager and restart Chrome in that profile. Allow the permission request that pops up when Companion connects.


### Firefox

Set `remote.active-protocols=1` in `about:config` and relaunch Firefox with these command line arguments:

**Mac**
<pre>open -a firefox --args --remote-debugging-port 9222 [--profilemanager]</pre>

**Linux**
<pre>firefox --remote-debugging-port 9222 [--profilemanager]</pre>

**Windows**
<pre>"%PROGRAMFILES%\Mozilla Firefox\firefox.exe" --remote-debugging-port 9222 [--profilemanager]</pre>


## Actions

- Click Element 
- Type Text 
- Navigate to URL 
- Go Back 
- Go Forward 
- Reload Page 
- Press Key 
- Scroll to Element 
- Select Dropdown 
- Check
- Hover Element 
- Close Tab 
- New Tab 
- Execute JS 
- Wait for Selector 
- Clear Input 
- Set Input Value 
