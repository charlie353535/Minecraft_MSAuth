# Minecraft_MSAuth
**An authentication server for Microsoft accounts on Minecraft.**

### How to use:

1. Create an Azure app of the type "web", set your redirect URI and a client secret.
2. Run like so: `java -jar mcauth_ms.jar [client ID] [client secret] [redirect URI]`
3. Clients can authenticate like so:  
    `https://login.live.com/oauth20_authorize.srf?client_id=YOUR_CLIENT_ID&response_type=code&redirect_uri=YOUR_REDIRECT_URI&scope=XboxLive.signin%20offline_access&state=STORAGE_ID`
4. You can reauthenticate using your refresh token with *no* user interaction like this:  
    `https://mc.charlie35.xyz/auth?code=REFRESH_TOKEN&state=STORAGE_ID&reauth=true`
5. You can retrieve client log-in info either by the response to the above page, or by GET'ing (these last 30s, and can be queried only once):  
    `/get?uid=STORAGE_ID`

**Note:** Storage ID is *not* required, and will be ignored if it is an invalid UUID.

### OR, If you want to authenticate a user with ZERO interaction with their user/pass:
1. Make a request to: `https://YOUR_SERVER/userpass?user=YOUR_MS_EMAIL&pass=YOUR_MS_PASS`
2. Done

I have a public instance on:
- `https://login.live.com/oauth20_authorize.srf?client_id=cbb2c2b0-3c23-422f-9b5b-329e9ba33c61&response_type=code&redirect_uri=https://mc.charlie35.xyz/auth&scope=XboxLive.signin%20offline_access&state=STORAGE_ID`
- `https://mc.charlie35.xyz/userpass?user=YOUR_MS_EMAIL&pass=YOUR_MS_PASS`
- (`mc.charlie35.xyz`)


You should know what you are doing when you use this. Don't bombard me with inane, basic questions regarding this software. \*_Charlie Moment_\*
