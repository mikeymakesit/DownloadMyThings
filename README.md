## DownloadMyThings

The purpose of this tool is to enable the bulk download of all my Things I've posted on Thingiverse.  I can recapture photos, models, tags and descriptions of Things that I haven't saved locally.  Given this information I can do a variety of things such as:

* Keep a local copy of my Things
* Upload my designs to other sites
* Close my Thingiverse account without losing my own IP

## Instructions

Given that this tool runs locally on your system, the OAuth "Implicit Grant" flow works fine.

1. Log on to Thingiverse in your web browser.
2. Browse to the following URL which will prompt you to allow this app to interact with your account:
https://www.thingiverse.com/login/oauth/authorize?client_id=1b0592dcb5966d8142d7&response_type=token
3. Using Developer Tools in your browser (or something) check the HTTP 302 response for the issued Access Token.
4. Update your local config file with the issued Access Token.  **Note the Access Token is a secret and you should protect it like your Thingiverse password!**
5. Run the tool to see your options and get downloading!

```
./dlthings -h
```

