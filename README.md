# Minecraft_MSAuth
### An authentication server for Microsoft accounts on Minecraft.
<br>
#### How to use:<br>
Create an Azure app of the type "web", set your redirect URI and a client secret.
<br>
Run like so: ```java -jar mcauth_ms.jar <client ID> <client secret> <redirect URI>```
<br>
Clients can authenticate like so:<br>
<code>https://login.live.com/oauth20_authorize.srf?client_id=YOUR_CLIENT_ID&response_type=code&redirect_uri=YOUR_REDIRECT_URI&scope=XboxLive.signin%20offline_access&state=STORAGE_ID</code>
<br>
You can retrieve client log-in info either by the response to the above page, or by GET'ing (these last 30s, and can be queried only once):<br>
<code>/get?uid=STORAGE_ID</code>
<br>
Storage ID is *not* required, and will be ignored if it is an invalid UUID.
<br>
I have a public instance on: <br><code>https://login.live.com/oauth20_authorize.srf?client_id=cbb2c2b0-3c23-422f-9b5b-329e9ba33c61&response_type=code&redirect_uri=https://mc.charlie35.xyz/auth&scope=XboxLive.signin%20offline_access&state=STORAGE_IDM</code>
<br><br>
You should know what you are doing when you use this. Don't bombard me with inane, basic questions regarding this software.
