# AdGuard + VPN

**Documentation is still in development**

AutoGuard is a [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm) project and Android app that automates [AdGuard for Android](https://adguard.com/adguard-android/overview.html) to bring together VPN and ad blocker on non-rooted devices.

**But isn't there [AdGuard VPN](https://play.google.com/store/apps/details?id=com.adguard.vpn) already?**

Sure, it can work with AdGuard in Integrated mode, but what if you use [Hiddify](https://github.com/hiddify/hiddify-app)/[NekoBox](https://github.com/MatsuriDayo/NekoBoxForAndroid)/[Shadowsocks](https://github.com/shadowsocks/shadowsocks-android)/other client? AutoGuard acts as an artificial Integrated mode for these apps.

## It doesn't support any VPN
**Only those VPN apps are supported that can work in a proxy mode!**

This means that any one-button commercial VPNs from Play Store, such as Planet VPN, Turbo VPN, ExpressVPN, NordVPN and so on, **are not supported**. Unfortunately, I can't do anything about it.

## How to use
 
1. Install AutoGuard as app / import it to Tasker
2. Give it permissions
3. Add it to AdGuard's filtering exclusions
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

Switch your VPN app to the **proxy only** mode, then enter its inbound local proxy type and port in AutoGuard.

<details>
<summary>Shadowsocks-based clients</summary>
For Shadowsocks, SagerNet, Matsuri, NekoBox, husi, Exclave etc.
<br><br>
Exclave as an example.
<br><br>
Open sidebar, go to Settings. Set Service mode to <b>Proxy only</b>.

![1000118844](https://github.com/user-attachments/assets/90fd4cd6-dd3c-42aa-986b-f8335f8f1586)

Scroll down, check your SOCKS5 port. You can also enable HTTP server if you want.

![1000118849](https://github.com/user-attachments/assets/25a935ef-636a-4847-a413-071e1c7d783c)

Enter it into AutoGuard. You can enter HTTP server port if you enabled it.

![1000118859](https://github.com/user-attachments/assets/729dfae0-1beb-4be0-bb1d-7278a4e953c5)
</details>

<details>
<summary>WG Tunnel</summary>
In Settings, set App mode to <b>Proxy</b>.
 
![1000129843](https://github.com/user-attachments/assets/3bc33db8-7486-4200-8df2-3f7238d94f60)

Tap on App mode, enable SOCKS5 and/or HTTP proxy type(s). Enter `127.0.0.1:` and any port you want.

![1000129844](https://github.com/user-attachments/assets/d5dac1a1-7ea6-4ff5-bab2-c630a01cfb9f)

Enter type and port to AutoGuard.

![1000129846](https://github.com/user-attachments/assets/ba58988c-ed30-47fa-85e3-14df5e6802bf)
</details>

<details>
<summary>InviZible Pro</summary>
AdGuard can be integrated with Tor.
<br><br>
On the main screen, in the three-dots dropdown menu select <b>Proxy Mode</b>.

![1000129834](https://github.com/user-attachments/assets/e1d8c8f2-0382-46f4-a94f-932922120667)

Open sidebar, go to <b>Tor Settings</b>. Scroll down to the proxy options. Enable SOCKS or/and HTTP type(s).
![1000129833](https://github.com/user-attachments/assets/f3ae785c-d2c9-4196-a447-4892124e26cb)

Click on SOCKS Port or HTTP Port to see it.
![1000129832](https://github.com/user-attachments/assets/1ea607e3-a40b-4224-bffa-c013f6342961)

Enter it to AutoGuard. Choose SOCKS4, SOCKS5 or HTTP for proxy type. HTTPS is not supported by InviZible Pro.
![1000130700](https://github.com/user-attachments/assets/d530f6ca-24a1-4216-9dba-7a4b2d81ab27)
</details>

## Support

AutoGuard's APK supports Android 5.0 (Lollipop) and above. It can work with AdGuard v4.0+ and with old versions (v3.6.11 and below). Enable Legacy mode for v3 support.

## Screenshots

<img width="1080" height="1080" alt="1000118721" src="https://github.com/user-attachments/assets/3afcae89-6897-4726-b2fa-73c9820abbd0" />
<img width="1080" height="1080" alt="1000118722" src="https://github.com/user-attachments/assets/33742af6-fe2b-4fc4-b21d-97d1a3efb918" />
<img width="1080" height="1080" alt="1000118723" src="https://github.com/user-attachments/assets/6122c1fe-be2c-4d40-a595-d2260719f8aa" />
