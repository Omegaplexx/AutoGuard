<p align="center"> <img width="100" height="100" alt="1000130680" src="https://github.com/user-attachments/assets/25274802-5b61-467e-bbac-805937e21712" /></p>

# AdGuard + VPN

**AutoGuard** is a [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm) project that automates [AdGuard for Android](https://adguard.com/adguard-android/overview.html) to bring together VPN and ad blocker on non-rooted devices.

## The issue
If you're using AdGuard in *Local VPN* mode, you cannot use any other VPN apps at the same time.

You may say, "But [AdGuard VPN](https://play.google.com/store/apps/details?id=com.adguard.vpn) can work with it."

Sure, it works with AdGuard in *Integrated mode*, but what if you use [Hiddify](https://github.com/hiddify/hiddify-app)/[NekoBox](https://github.com/MatsuriDayo/NekoBoxForAndroid)/[Shadowsocks](https://github.com/shadowsocks/shadowsocks-android)/other client? AutoGuard acts as an *Artificial Integrated mode* for these apps.

## It doesn't support any VPN

**Only those VPN clients (apps) are supported that can work in proxy mode!**

This means that any one-button commercial VPNs from Play Store, such as Planet VPN, Turbo VPN, ExpressVPN, NordVPN and so on, **are not supported**. Unfortunately, I can't do anything about it.

## How to use

1. [Import AutoGuard to Tasker](https://taskernet.com/shares/?user=AS35m8lewGrrfIKiVE6Udvw%2FuM8FTsRvubfS55EvDtqqmwbbZ2yvPcuUOF5RJL0ubo8B9Q%3D%3D&id=Project%3AAutoGuard%3A+AdGuard+%2B+VPN)
2. Give it permission to work in background
3. Add Tasker and your VPN app to AdGuard's filtering exclusions
4. [Enter the AdGuard automation password](#password)
5. [Enter your VPN app's proxy server type and port](#type-and-port)

### Password

Open AdGuard, go to **Settings** → **General** → **Advanced** → **Automation**. Copy the password and paste into AutoGuard.

<details>
<summary>Screenshots</summary>

<img width="1080" height="1080" alt="1000118731" src="https://github.com/user-attachments/assets/43aab56b-e0bf-4da4-9895-774d59ad2657" />
<img width="1080" height="1080" alt="1000118735" src="https://github.com/user-attachments/assets/1b9234f6-5906-49c2-9b49-de2c240512ce" />
<img width="1080" height="1080" alt="1000118736" src="https://github.com/user-attachments/assets/5f590b42-caf3-4c96-a23c-dd8a87feddc9" />
<img width="1080" height="1080" alt="1000118739" src="https://github.com/user-attachments/assets/2adf6f57-59bd-4a9f-bf37-8a1cbad60448" />
<img width="1080" height="1080" alt="1000118743" src="https://github.com/user-attachments/assets/3fe11fcc-c8bc-4185-948f-f49d1f25158e" />
The password can simply be <b>1234</b>. It doesn't have to be that long.
</details>

### Type and port

Switch your VPN client to the **proxy only** mode, then enter its inbound local proxy type and port into AutoGuard.

<details>
<summary>Shadowsocks-based clients</summary>
<br>
For Shadowsocks, SagerNet, Matsuri, NekoBox, husi, Exclave etc.
<br><br>
Exclave as an example.
<br><br>
Open sidebar, go to <b>Settings</b>. Set <b>Service mode</b> to <b>Proxy only</b>.

![1000118844](https://github.com/user-attachments/assets/90fd4cd6-dd3c-42aa-986b-f8335f8f1586)

Scroll down, check your <b>SOCKS5 port</b>. You can also enable HTTP server if you want.

![1000118849](https://github.com/user-attachments/assets/25a935ef-636a-4847-a413-071e1c7d783c)

Enter it into AutoGuard. You can enter HTTP server port if you enabled it.

![1000118859](https://github.com/user-attachments/assets/729dfae0-1beb-4be0-bb1d-7278a4e953c5)
</details>

<details>
<summary>v2rayNG</summary>
<br>
Open sidebar, go to <b>Settings</b>, scroll down. Remember the value in <b>Local proxy port</b>.
 
![1000129802](https://github.com/user-attachments/assets/6fd0fa23-2c61-4ac1-af72-a77b275e96dd)

In <b>Mode</b> select <b>Proxy only</b>.
![1000129803](https://github.com/user-attachments/assets/5790980d-0bc0-412c-96f4-430e962260f1)

Enter the port to AutoGuard, set any type you want.
![1000129805](https://github.com/user-attachments/assets/1aaacaf6-138d-4b40-9a6d-4293b297a046)
</details>

<details>
<summary>Hiddify</summary>
<br>
Open <i>Settings → Inbound</i>. In <b>Service mode</b> select <b>Proxy service only</b> and remember the value in <b>Mixed port</b>.

![1000131269](https://github.com/user-attachments/assets/4f524b0f-afd0-435d-88a3-0ea2617dff55)


Enter it to AutoGuard. Choose any type you want.
![1000130792](https://github.com/user-attachments/assets/bab3e8a4-5b6d-4993-ac30-a709431962f2)
</details>

<details>
<summary>Karing</summary>
<br>
Open <b>Settings</b>, disable <b>Novice Mode</b>. Scroll down, select <b>TUN</b> and disable it.

![1000130827](https://github.com/user-attachments/assets/e01d8708-96cf-4474-b08a-8745bc848293)
![1000130828](https://github.com/user-attachments/assets/90e47281-c09c-4eba-8734-3208d25dfaf6)
![1000130829](https://github.com/user-attachments/assets/c604aadf-59f8-4073-b414-1ab7106cbc8a)

Return to <b>Settings</b>, select <b>Port</b>.
![1000130832](https://github.com/user-attachments/assets/a5d9daf3-ceaa-430d-8e92-ae8bd4f84421)

Enter to AutoGuard the <b>Rule Based</b> one or the <b>Proxy All</b> port.
![1000130834](https://github.com/user-attachments/assets/b17747dd-5d71-4dc7-bcc9-73978ce2cc74)

Choose any type.
![1000130837](https://github.com/user-attachments/assets/73e89811-3fc4-445a-9243-e09b07da2eb2)
</details>

<details>
<summary>WG Tunnel</summary>
<br>
In <b>Settings</b>, set <b>App mode</b> to <b>Proxy</b>.
 
![1000129843](https://github.com/user-attachments/assets/3bc33db8-7486-4200-8df2-3f7238d94f60)

Tap on <b>App mode</b>, enable SOCKS5 and/or HTTP proxy type(s). Enter `127.0.0.1:` and any port you want.

![1000129844](https://github.com/user-attachments/assets/d5dac1a1-7ea6-4ff5-bab2-c630a01cfb9f)

Enter type and port to AutoGuard.

![1000129846](https://github.com/user-attachments/assets/ba58988c-ed30-47fa-85e3-14df5e6802bf)
</details>

<details>
<summary>InviZible Pro</summary>
<br>
AdGuard can be integrated with Tor.
<br><br>
On the main screen, in the three-dots dropdown menu select <b>Proxy Mode</b>.

![1000129834](https://github.com/user-attachments/assets/e1d8c8f2-0382-46f4-a94f-932922120667)

Open sidebar, go to <b>Tor Settings</b>. Scroll down to the proxy options. Enable SOCKS or/and HTTP type(s).
![1000129833](https://github.com/user-attachments/assets/f3ae785c-d2c9-4196-a447-4892124e26cb)

Tap on <b>SOCKS Port</b> or <b>HTTP Tunnel Port</b> to see it.
![1000129832](https://github.com/user-attachments/assets/1ea607e3-a40b-4224-bffa-c013f6342961)

Enter it into AutoGuard.
![1000130700](https://github.com/user-attachments/assets/d530f6ca-24a1-4216-9dba-7a4b2d81ab27)
</details>

<details>
<summary>ByeByeDPI</summary>
<br>
Go to <b>Settings</b>, set <b>Mode</b> to <b>Proxy</b>.
 
![1000130809](https://github.com/user-attachments/assets/77f6c87a-1049-4c11-9720-32c9f0ce19e0)

Check the value in <b>Port</b>. Enable <b>HTTP proxy</b> if you want.
![1000130810](https://github.com/user-attachments/assets/4cf29476-05d3-48d5-bcdc-9be2b724bd62)

Enter the port to AutoGuard and select SOCKS5/SOCKS4 as server type. You can select HTTP if you enabled it.
![1000130819](https://github.com/user-attachments/assets/7927a2b0-5ca9-4a68-bc63-5c708604534f)
</details>

<details>
<summary>Clash Meta for Android Alpha</summary>
<br>
Open <i>Settings → Network</i>, disable <b>Route System Traffic</b>.

![1000131239](https://github.com/user-attachments/assets/69190591-4d05-4a42-8877-92ded53a1c24)
Go to <i>Settings → Override</i>, choose any <b>HTTP Port</b> and <b>Socks Port</b> you want.
![1000131240](https://github.com/user-attachments/assets/40d7fae1-bf54-4934-8bc6-95d2af50eb1b)
Enter it to AutoGuard. Both SOCKS5/4 types are good for Socks Port.
![1000131259](https://github.com/user-attachments/assets/ac2e1616-c663-4678-98bf-1633afd7ce06)
</details>

<details>
<summary>Orbot</summary>
<br>
AdGuard + Tor
<br><br>
Start connection to see SOCKS5/HTTP ports.
 
![1000131207](https://github.com/user-attachments/assets/98e6edc0-84eb-4f12-b920-62f4efa0d28b)

Go to <i>More</i> tab. Remember one of the port values, then go to <i>Orbot Settings → General</i>
![1000131211](https://github.com/user-attachments/assets/4d834998-6144-4aac-8cfb-93a745eb99b6)

Enable <b>Power User Mode</b>. It's equivalent to Proxy Only Mode.
![1000131218](https://github.com/user-attachments/assets/1bdaa497-5643-4ef2-a5e5-3460a0cb359d)

Enter one of the port values to AutoGuard and select the appropriate type.
![1000131225](https://github.com/user-attachments/assets/81ca845f-5adb-42cf-b535-c34c63859ad8)
</details>

## AdGuard v3.x support (Legacy)

AutoGuard can work with old AdGuard versions (v3.6.11 and below). Enable **Legacy mode** in AutoGuard's Advanced Settings.

## Screenshots

<img width="1080" height="1080" alt="1000118721" src="https://github.com/user-attachments/assets/3afcae89-6897-4726-b2fa-73c9820abbd0" />
<img width="1080" height="1080" alt="1000118722" src="https://github.com/user-attachments/assets/33742af6-fe2b-4fc4-b21d-97d1a3efb918" />
<img width="1080" height="1080" alt="1000118723" src="https://github.com/user-attachments/assets/6122c1fe-be2c-4d40-a595-d2260719f8aa" />
