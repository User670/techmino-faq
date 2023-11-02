# General

## What is Techmino?
Techmino is a block stacking game developed by Chinese developer MrZ, using the Love2D engine. In addition to classic Sprint, Marathon and VS modes\*, it also has 49- and 99-player battle royale modes*, training modes to sharpen your skills, as well as a fully customizable custom mode for your practice and experimentation needs.

\* VS and Battle Royale modes on the singleplayer map are against AI players. <!--A separate multiplayer mode exists for you to play against other players.-->

## Multiplayer?
At the time of writing, the multiplayer server is not operational.

## Is this open source?
Yes. https://github.com/26F-Studio/Techmino 

## Can I upload a video of Techmino, or livestream me playing it?
Previously we demanded that you ask for permission before doing so, but the legality of such requirement has been questioned.

However, we do beg you that, if you decide to share any screenshots, videos or live streams of Techmino, please keep them within the Tetris community. We do not want too much publicity for the time being.

## What about Techmino Galaxy?
Techmino Galaxy is a sequel to Techmino. This FAQ only concerns the original Techmino game. You can join the Discord community or follow the Techmino Galaxy repository for information about the sequel.

# Downloading and Launching

## First of all, where do I get the game?
The [Github Releases page](https://github.com/26F-Studio/Techmino/releases) should have most f the versions you need.

If you live on the edge, [GitHub Actions](https://github.com/26F-Studio/Techmino/actions) builds a version for each commit, though be prepared for unstablities. You need a GitHub account to download from GitHub Actions.

For iOS, you can find Techmino on TestFlight: https://testflight.apple.com/join/SZOFUqFv⁠ . If it says the beta isn't accepting more testers, unfortunately it is not available at this time. Alternatively, you can sideload the `.ipa` file onto your device using [Sideloadly](https://sideloadly.io/).

## On macOS, trying to open the game shows a pop-up blocking it from opening.
If you get the pop-up below: 

![image](https://github.com/User670/techmino-faq/assets/22617255/d66091c9-17b6-4663-83b5-d9d4e36777d3)

This is because the Gatekeeper on macOS won’t let the user open any app that is not signed or notarized on default. However, there is an easy way to bypass this: control–click Techmino.app and select “Open” from the pop-up menu, then select “Open” from the window.

If you get this pop-up instead: 

![image](https://github.com/User670/techmino-faq/assets/22617255/457cbf61-75a9-479e-a8c0-f4f6f24bb96c)

Option-click Techmino.app, select “Get Info” from the menu, then check the “Override Malware Protection” checkbox. You should now be able to open it.

## I am using an ARM version of Linux. Why can’t I play Techmino on my device?
Unfortunately, the ARM distros of Linux are not yet supported by LÖVE, so you cannot do that. If you really want to play it on your device, we recommend you to use box64/box86 with Wine to run the Windows distro of the game. Also you cannot open .AppImage files using box64/86 directly.

## I am using an M1 Mac. Can I play Techmino on my device?
Yes! LÖVE supports M1 Macs. If you are using older versions that don’t support M1, just use Rosetta 2 (which is built within the system so you don’t have to do anything).

## I'm on an old version of the game, and all I see is a calculator or an elevator.
That was app lock - which has been removed.

Before 0.13.2: In the calculator, type 626=.

After 0.13.2: Press 6 and 26 on the elevator buttons, or F and Z on the keyboard.

After you gain access to the game, you can go to the settings and disable App Lock. 

# Gameplay

## I only see one mode on the map?
You need to play it in order to unlock other modes. Lines coming out from mode icons indicate whether this mode can unlock other modes.

To unlock subsequent modes, you need to reach rank D on a mode - this would be 1m 2s for Sprint 10L, or 3m 3s for Sprint 40L.

## My main menu only has big buttons for Sprint and Marathon.
If your main menu looks like this:

![image](https://github.com/User670/techmino-faq/assets/22617255/4f1f2a85-bbcc-450b-9d6c-2e80ea51e273)

You probably have enabled “Simplistic Mode.” In this mode, only a few essentials modes and functions are available. Simply go to the settings and uncheck the “Simplistic Mode” to fix it.

## Is this Guideline?
Close, but no. Some more important differences from Guideline are: it uses a custom rotation systems that is based on SRS but has more kicks, has all spin and O-spin, and has a different attack table.

## What are the AI players?
The game uses two AIs: Cold Clear and 9Stacker.
- [Cold Clear](https://github.com/MinusKelvin/cold-clear) is developed by MinusKelvin. It is capable of performing T-Spins, Back-to-Backs and Perfect Clears. It is reported to be laggy on low-end devices when playing Battle Royale modes.
- 9Stacker is a more "stupid" algorithm, capable of only finesse and hard dropping.

## Is there controller support?
Yes! Feel free to adjust button mappings in the settings.

## How can I access the in-game console?
You can do it by clicking or pressing the “TECHMINO” icon on the home page or pressing the “C” key on your keyboard several times. Note that external keyboards may not work correctly on iOS and iPadOS.

## I recall there used to be minigames in the game. Where are they?
They are now rebranded as "Applets" and are hidden in the Console. Press C on your keyboard or tap the Techmino logo a few times while on the main menu, and use the app command to access minigames (`app <applet code>` to launch it, `app -list` to show a list of them). Use the `exit` command in the Console to return to the game.

## How do I change language?
On the main menu, there is a button that reads "言/A" (pre-0.14.5) or shows an earth icon (0.14.5 and onwards). That's the select language button.

# Troubleshooting

## My game crashed without a blue screen!
If the crash happened while an AI player is loaded (eg, in a VS mode game or on the title screen), likely an issue of Cold Clear, the bot AI we use. We can't do much about it.
You can still try to ask around about the crash, especially when it happens without an AI on screen.

## My external keyboard isn’t working with Techmino!
Try plugging and unplugging your keyboard, or reconnecting your keyboard if you are using a Bluetooth keyboard. This kind of issue typically only happens on mobile devices. For iOS and iPadOS users, that is an issue we can not fix for now. This might be related to the iOS distro of LÖVE or how iOS recognises external keyboards. At the same time, you can still use the on-screen virtual keys.

## Why Techmino is displayed in portrait mode on iOS (especially on iPhone)?

![image](https://github.com/User670/techmino-faq/assets/22617255/30f7c67c-38db-43b3-9b46-5f049a1672f3)

Apparently, this is a bug that happens in iOS. The “Portrait” mode in settings seems to do nothing on iOS. Therefore, the only solution is to enter Techmino in landscape mode:
1. Swipe up from the bottom of the screen or double-tap the home button to enter App Switcher, then swipe up to quit Techmino. 
2. Disable the rotation lock if you haven’t already. 
3. Rotate your device to landscape mode. It is okay if the contents on the home screen don’t seem to be rotated to landscape view — this is normal as long as you hold the device in a landscape manner. 
4. Enter Techmino. Everything should be okay now.

Note that if you “swipe quit” the app again you may need to repeat the procedures above all over again.

# Technical questions

## How can I view the requirements for each mode?
First, go to our GitHub page (https://github.com/26F-Studio/Techmino/), then navigate to `.parts/modes` to find the mode file (`.lua`) you want to know. After that, look for a piece of the code that looks like this (this will going to be different for each mode, in this example, `sprint_40l.lua`):

```lua
if P.stat.row<40 then return end
    local T=P.stat.time
        return
            T<=26 and 5 or
            T<=36 and 4 or
            T<=52.6 and 3 or
            T<=92.9 and 2 or
            T<=183 and 1 or
            0
    end,
```

The first line means that if `P.stat.row` is less than `40` (which means that you didn’t finish the 40L sprint), your grade is not recorded. 

The variable’s name that goes after local is the category of the requirement (in this example, time (in seconds)). 

the `5`, `4`, `3`, `2`, and `1` correspond to `X`, `U`, `S`, `A`, and `B` grades in the game. 0 also means your grade is not recorded (in this example, when your time exceeds 183 seconds). 

## How can I perform O-Spins?
Remember that this trick only works in TRS.

To perform an O-spin in TRS, first, move the O block in an appropriate “hole,” then use the following rotations to do the trick: (F means 180 rotation)

```
O → Z: LRL
O → S: RLR
O → J: LLR
O → L: RRL
O → T: LLL & RRR
O → I: FFF
```

![ezgif-3-2df4b7cb11](https://github.com/User670/techmino-faq/assets/22617255/dfa019f7-afa6-4d39-ad2f-f31428a6e099)

You may also perform another kind of O-spin in BiRS (which doesn’t involve transformation) by holding the correct arrow keys (move left/move right/soft drop) and then rotating in the correct direction. More about BiRS in Zictionary. 

![ezgif-3-f3f0ca171f](https://github.com/User670/techmino-faq/assets/22617255/108a10d0-33a9-41f6-8beb-eac6b99d9c72)

Quick note: you may hold the transformed O block, and it will stay as the transformed block. However, if you perform a spin using this “O block,” it still counts as an O-spin.

## How should I calculate the attack in Techmino?
Please use this table as a reference.

![image](https://github.com/User670/techmino-faq/assets/22617255/50159656-8972-4416-a2df-855cbeafb0e3)

## How is B2B2B calculated in Techmino?
Use this table to calculate B2B2B meter (on the left of the playfield)

![image](https://github.com/User670/techmino-faq/assets/22617255/2040ee53-1abb-4f68-8216-b24415511eac)

## How can I transfer my data from one device to another?
Simply go to Statistics > Data Management, and you will see these buttons. Then you can copy and paste the data using your clipboard. 

![image](https://github.com/User670/techmino-faq/assets/22617255/8593a666-47ee-4f7c-bff6-20199a4f824c)

# Development

## How do I extract, view, or replace the game's assets and code?
The `Techmino.exe` file (Windows) or `game.love` file (anything else) are valid zip archives. Using a software like 7-Zip, you can view, extract or replace any file(s) in it, including assets and lua scripts.

For macOS users:
> Download the official distro of LÖVE here: https://love2d.org/
>
> Control-click ”Techmino.app” and select “Show Package Contents”. Go to ./Contents/Resources and you will find a file called “Techmino.love”. Rename the extension to “.zip” and unarchive using an unzipping tool. You can edit the files now. When you are done, re-archive the files (please choose “Store Directly” and “Excluding macOS Content Resource Fork” in your zipping app) and rename the extension to “.love”. Finally, drag the .love file to LOVE.app to run the game. 
>
> Please notice that you cannot just directly replace the .love file in Techmino.app. This is because all apps need to be notarised in order to run properly on macOS, and changing the files in the .app would destroy the notarisation, and the app would fail to launch.

## How do I make and import my own block skin?
This is an example block skin for your reference (smooth_mrz):

![image](https://github.com/User670/techmino-faq/assets/22617255/e3ffe4c1-35f8-4b6b-8f55-e113bb2207a6)

- The block skin is a png file with a dimension of at least 240 × 90.
- The image is divided into a 3 ×8 array of blocks, with each block having a dimension of 30× 30.
- The positions, functions, and colours of each block here can be seen in this image: 

![image](https://github.com/User670/techmino-faq/assets/22617255/9e571df3-e60c-4429-a000-6bf3e2203270)

Reference Zictionary for more information.

To import your skin into the game:

1. Make your block skin and export it into a png file.
2. Move you skin to ./media/image/skin/.
3. Added the following code into ./main.lua at around line 315, after SKIN.load{ (replace <SKINNAME> with the filename of the skin):

```lua
{name="<SKINNAME>",path='media/image/skin/<SKINNAME>.png'},
```

5. Start the game. You will find your skin appearing in the block skin list.

# Other things

## Who are the voice actors for the voice packs? What are the voice languages?
- [Miya](https://space.bilibili.com/846180) is a virtual live streamer who used to play a lot of block stacking games. Voice language: Japanese (line clears); Japanese, Chinese and Cat (others)
- Mono is an artist, however her online profile had been wiped clean. Voice language: Japanese
- Xiaoya is a fellow block stacker player. She introduces herself as "Xia Xiaoya, a brand new type of duck." Voice language: English (line clears); Chinese (others)
- [flore](https://space.bilibili.com/1223403016) is a fellow block stacker player, featured in [this article](https://github.com/User670/temp/blob/master/those_who_play_tetris.md). Voice language: English (line clears), various languages (others)
- [Miku](https://en.wikipedia.org/wiki/Hatsune_Miku) is a voice bank for the Japanese voice synthesizer Vocaloid. Voice language: Japanese
- [Zundamon](https://vocalsynth.fandom.com/wiki/Zundamon) is a voice bank for various voice synthesizer programs. Voice language: Japanese

While MrZ does not have a voice pack, there was a "Welcome to Tech" voice clip that was recorded by MrZ himself.

## Anti-addiction system?
Techmino has a built-in "anti-addiction" system that apply to some players, and it will block the players from playing after playing for 4 hours in a day. This system is a parody of [China's online gaming anti-addiction system](https://www.bbc.com/news/world-asia-50315960).

## I see an icon that is like the "thinking" emoji, but with a Z tetromino. What is this?
It means “Tetris”! Due to possible risk of receiving DMCAs from TTC, we have decided to replace all “Tetris” in the game with the emoji.

## What’s that purple screen?
Same as a blue screen crash. It may occasionally appear, as a small Easter Egg.

## How can I download the in-game soundtracks?
The Techmino OST is now available on SoundCloud! You can download the full soundtracks here free of charge (with a CC BY 3.0 License):

https://soundcloud.com/michael-gu-102967376/sets/techmino-the-ost-v2?utm_source=clipboard&utm_medium=text&utm_campaign=social_sharing











