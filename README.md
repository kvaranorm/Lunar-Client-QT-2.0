FAQ
Q: Can I be banned for using this?
A: Lets break this into 2 types of bans:

Lunar: While LCQT is theoretically detectable on lunars end, as of right now they do not issue client bans.
Hypixel / Other Servers: LCQT does not send any information to the server. As long as you don't abuse any disabled mods (e.g chat macros) you will not be banned.
Q: What patches are included in the lcqt2 agent?
A: In case this goes out of date you can find them here.
However:

Cosmetics Unlocker: Unlocks cosmetics for paid Minecraft users.
Cracked Account: Allows Cracked Accounts to be used.
FPS Spoof: Spoof your FPS.
Freelook: Re-enables Freelook and AutoTextHotkey on servers.
NoHitDelay: Removes delay between hits.
Debug: Enables "Staff" Mods (Currently only X-Ray).
*Panorama Maker: Internal Use Only
*GeckoLib Debug Mod: Internal Use Only
Q: Why isn't cosmetics working on a cracked account?
A: Because of the way the cosmetics unlocker is implemented you have to be connected to lunars servers for it to work.
For obvious reasons lunars websocket server does not allow cracked accounts.
Note: Premium users on cracked servers, this is applicable to you as well.

Q: Why isn't my JRE working under Custom JVM?
A: Your JRE/JDK needs to be Java 17.

Q: How do I add a java agent?
A: Append the following to your JVM Arguments in Settings: -javaagent:/path/to/.jar
You must use forward slashes (/) or double backslashes (\) in your path.

Note: As always, use this at YOUR OWN RISK, I am not responsible for any damages that may occur.

Installation
Windows
Simply download and run the setup executable here.
If you prefer a portable version, download the zip.

Arch Linux
Use the AUR package: lunar-client-qt2.

macOS/Linux
If you are using Linux, be sure to have the Lunar Client-X.AppImage renamed to lunarclient in /usr/bin/. Alternatively, run lcqt2 with Lunar Client Qt ~/path/to/lunar/appimage.

Download the file: Linux or macOS.
Extract it anywhere (tar -xf os-portable.tar.gz)
Run the Lunar Client Qt executable
IMPORTANT: All 3 files which where inside the tar need to stay together.
You are allowed to move all 3 together, you're also allowed to create symlinks.

Building
Prerequisites
Rust Nightly
NPM
Building
LCQT2 is made up of 3 major components:

The injector - responsible for locating the launcher executable and injecting a javascript patch into it
The gui - contains the gui opened by pressing the syringe button, also contains the javascript patch used by the injector
The agent - java agent which implements all game patches
In order for lcqt to work properly all 3 components need to be built into the same directory.

$ ./gradlew installDist # builds all 3 components and generates a bundle in build/install/lcqt2
$ ./gradlew run # equivalent to ./gradlew installDist && './build/install/lcqt2/Lunar Client Qt'
./gradlew installDebugDist and ./gradlew runDebug do the same thing except they build the rust injector in debug mode.

Copyright © 2023 BestGamersHK - License
