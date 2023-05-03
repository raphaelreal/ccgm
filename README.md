## PRE-SETUP INSTRUCTIONS

MAKE SURE YOU CLICK "Add Python 3 to PATH" IN THE INSTALLER
https://www.python.org/ftp/python/3.8.6/python-3.8.6-amd64.exe

2. Install .NET Redistributable (System restart may be required)
https://aka.ms/vs/17/release/vc_redist.x64.exe

3. Install Sandboxie 
https://github.com/sandboxie-plus/Sandboxie/releases/download/v1.6.7/Sandboxie-Plus-x64-v1.6.7.exe

4. Download and unzip CCGM
https://cdn.discordapp.com/attachments/1070050358749044776/1102381876083171328/CCGM_BETA_0.5.5.zip

5. Create a Discord server for your group!

## SETUP INSTRUCTIONS
1. Go to the install folder and run the CrustaceanInstaller.exe to install mapmod if you haven't already. Run the game once then close it when you see the main menu. 

NOTICE: If your computer doesn't have a graphics card, you'll need to follow the installation guide here instead of using CrustaceanInstaller.exe

https://github.com/o7Moon/CrabGame.MapMod/wiki/How-to-install-MapMod

2. Right click Crab Game in Steam and click manage -> browse local files. Navigate to Bepinex -> plugins and replace the mapmod.dll with the one in your install folder. This is a custom version of mapmod I've created to be compatible with CCGM. Even if you're not hosting custom maps, it's important to add as it controls maps and modes. 

3. Double click the install_requirements.bat file to install all the dependencies you need.

4. Leave the install folder and navigate to the CCGM folder. Open the discord_invite.txt file and place your Discord invite inside. I recommend using an invite shortening service if your group doesn't qualify for a real one. Try https://dsc.gg/ or https://invite.gg/

5. Configure your ccgm_config.json file. I'll show you how to do this under the config instructions.

## CONFIG INSTRUCTIONS
1. Open up the ccgm_config.json file in your preferred text editor. Towards the top you'll see "your server name here". Replace that text with the name of the server you want to show in game.

![Beschreibung des Bildes](https://cdn.discordapp.com/attachments/1069433394624204981/1071250376197673000/image.png)

2. Give your server a shortName. This is used to interact with your server through Discord and is used in the database. The shortName cannot have any spaces!

![Beschreibung des Bildes](https://cdn.discordapp.com/attachments/1069433394624204981/1071252588227477616/image.png)

3. Give your server an inviteColor. This is the color of the invite embed that will be posted in your Discord. Make sure to use hexadecimal format! (Default is green, I chose a light blue)

![Screenshot3](https://cdn.discordapp.com/attachments/1069433394624204981/1071256680156909618/image.png)

4. Setup a sandboxName. This is the name of the sandbox CCGM will run in. A sandbox is important so that you can host multiple servers!

NOTICE: If you are only hosting one server and you plan to play on the account you're hosting with, erase the text and leave it empty.  This will disable the sandbox feature. Playing the game through a sandbox can cause you issues.
Should look like "sandboxName": ""

![Screenshot4](https://cdn.discordapp.com/attachments/1069433394624204981/1071260116936044726/image.png)

5. Create a sandbox under the same name as your sandboxName. Make sure you enable "Add 'Run Sandboxed' to the explorer context menu".

NOTICE: Not required if you're only hosting one server and you plan on playing the game with the account you're hosting with.
 
![Video](https://cdn.discordapp.com/attachments/1103081221916987393/1103172331507023872/creating_sandbox.gif)

6. Make modes empty by removing all of the ones. Now open your game and click "start game -> maps and modes". Read the modes left to right, top to bottom. If you want a mode type in "1" otherwise type in "0".

![Screenshot5](https://cdn.discordapp.com/attachments/1069433394624204981/1071842245877186690/image.png)

7. Do the same thing with maps. Empty it by removing all the ones. Read the maps left to right, top to bottom. Type in "1" if you want that map otherwise type in "0"

8. Set maxPlayers, this option is the maximum amount of players that can play on your server. Now set requiredStartPlayers, this option is the amount of players required to be on your server before the !start command can be used. The !start command ready's up all players and starts the game. If their are not enough players for the !start command to be used, moderators must wait 1 minute before using it.

![Screenshot6](https://cdn.discordapp.com/attachments/1069433394624204981/1071844680171532338/Discord_hWb3zW3PiA.png)

9. Next up is gameModeSettings, this section gives you control of all of CCGM's custom game mode options. The first configurable settings are for CrabFight, so we'll start with that. The value angerProbability is the chance of Tantan becoming angry as a percentage between 0 - 100. When Tantan is angry, he will do combination attacks like spikes + body slam and others.

![Screenshot69](https://cdn.discordapp.com/attachments/1069433394624204981/1072013054033797140/image.png)

10. Set the randomizeHealthProbability value. Like angerProbability your value should be a number between 0 - 100. This is the chance that Tantan's health is randomized. We'll set the minimum health and max health values later.

11. Set the randomizeSnowballDamageProbability value. This is the chance that player's snowball damage will be modified.

12. Set the maxAngerCrabBalls value. When Tantan is angry, this is the maximum number of crab balls / spikes he can spawn. I recommend keeping this value below three unless you want Tantan to become a dark-souls boss.

13. Set the snowballDamageMultiplierMin and the snowballDamageMultiplierMax values. When randomizeSnowballDamage is active CCGM will pick a number between these values. Imagine you set min to 0.5 and max to 3. CCGM randomly picks the damageMultiplier 2.0. Now if a player does 2 damage to Tantan with a snowball CCGM will multiply 2 damage by 2.0 resulting in 4.0 damage.
 
14. Set the randomizeHealthMin and the randomizeHealthMax values. When randomizeHealth is active CCGM will pick a number between these values. Tantan's default health is 100 so keep that in mind when considering a number.

Now we're done with crabFight settings, here's what mine look like so far:

![Proof](https://cdn.discordapp.com/attachments/1069433394624204981/1072019284869533746/image.png)

15. Next up is blockDropSequenceProbability. This is the chance of the block drop game mode being modified with a special sequence.

16. The chaosMode setting defines if chaos mode should be active (true or false). Chaos is a lot to type about here but the gist is this: players will have access to a points shop and random events will happen. Players can purchase weapons with points and earn points by playing or winning.

17. The customMaps setting defines if your server includes custom maps (true or false). If you want to use custom maps, you will have to setup your own Github repo. I have tutorials for installing mapmod, creating your own maps and setting up your own Github repo on harpys Discord server: discord.gg/ccgm

18. The tagSwapProbability setting allows you to define the chance of the tag game mode's maps to be randomized. This means players can end up on maps that don't originally allow for the tag game mode. Right now these maps are defined internally and cannot be customized. I'll add customization for this setting later.


19. The snowBrawlSwapProbability setting allows you to define the chance of the snow brawl game mode's maps to be randomized. This means you can play snow brawl on maps that don't originally allow for it. If the map does not have snowballs CCGM will give players snowballs periodically. The maps that are possible to play on are not customizable at this time. I'll add customization later.

20. The sumoModeProbability defines the chances of king of the hill game mode's maps to be randomized. This means you can play king of the hill on maps that don't originally allow for it. The idea behind sumo mode is that players fight to hit each-other out of the map with bats. Therefor sumo-mode only takes place on maps with out of bounds regions. Like steps 18 and 19, the map customization for this setting isn't available at this time.

We're now done with the gameModeSettings section. Here's what mine looks like:

![Proof2](https://cdn.discordapp.com/attachments/1069433394624204981/1072028405631037500/image.png)

21. Now we need to create a leaderboardWebHook for your server. Create a text channel for your leaderboard then go to the channel's settings. Click on "integrations" and "create webhook". Give your web hook a name and a profile picture then "Copy Webhook URL". Now you can copy paste it into your  leaderboardWebHook config setting.

![DC](https://cdn.discordapp.com/attachments/1069433394624204981/1072329272687079525/image.png)

22. Next up is your tips setting. Each tip is surrounded by quotes and if another tip follows, it should end with a comma. If the tip is the last tip, no comma should be added. If a tip includes a new line character "\n" the bot will post a new line. If a tip includes the text "{discordInvite}" the bot will replace that text with the invite code inside of your "discord_invite.txt" file. Here's an example of my text settings:
 
![LOL](https://cdn.discordapp.com/attachments/1069433394624204981/1072338442605834290/atom_zXufMX42t8.png)

23. Next setting is ownerId. This will be your Discord user ID. To get it, make sure you have Developer mode enabled by going to your settings -> Advanced. Then right click your profile picture in chat and "Copy ID".

![LOL33](https://cdn.discordapp.com/attachments/1069433394624204981/1072380744044924958/image.png)

24. For ownerRoleId you'll need to create a role in your Discord that only you the owner have. Now left click your profile in your server and right click your owner role and "Copy ID".

![SER](https://cdn.discordapp.com/attachments/1069433394624204981/1072382348835958834/image.png)

25. Now for adminRoleId create a role for your admin's and only give this role to users you trust the most. Copy it's ID and paste it in place of the zeros.
 
26. The adminPerms describes what perms your admins will be granted when they're promoted. You can add or remove these as you please.

![IMAGE](https://cdn.discordapp.com/attachments/1069433394624204981/1072383859334844436/Discord_iylYbrVLFv.png)

27. For moderatorRoleId create a role for your moderators and only give this role to users you trust. Copy it's ID and paste it in place of the zeros.

28. The moderatorPerms describe what perms your moderators will be granted when they're promoted. You can add or remove these as you please.

![888](https://cdn.discordapp.com/attachments/1069433394624204981/1072588604142014545/image.png)

29. For remoteCommandsId you'll need to create a new text channel for your remote commands. This channel will allow you and your team to send commands to your server from Discord. Right click the channel and copy it's ID.

![29](https://cdn.discordapp.com/attachments/1069433394624204981/1072589603728527371/image.png)

30. For banLogsId you'll create a text channel for your ban logs. All bans will be logged here. Copy it's ID and paste it in place of the zeros.

31. For userReportsId you'll create a text channel for your user reports. When players use the !report command in game your moderation team will receive a notification here. Copy it's ID and paste it in place of the zeros.

Here's what my ID's look like:

![31](https://cdn.discordapp.com/attachments/1069433394624204981/1072591315142983720/image.png)

32. Next is inviteCodesWebHook. You'll create a text channel for your invite codes so players can easily find your servers. Then you'll create a webhook for this text channel. Copy your webhook URL and paste it as the value. If you don't remember how to do this, refer to step #21.

![32](https://cdn.discordapp.com/attachments/1069433394624204981/1072592012924170451/image.png)

33. We're almost done, next up is discordBotToken. This is what will allow your Discord bot to login. First you need to create a Discord bot, you can do this by heading over to https://discord.com/developers/applications and clicking on "New Application". Give your bot a name and a profile picture. This bot will receive moderator commands, log reports and bans.

![33](https://cdn.discordapp.com/attachments/1069433394624204981/1073303941359599667/chrome_Oxvo2Xku99.png)

34. Now head over to the Bot section and click on "Add Bot"

![34](https://cdn.discordapp.com/attachments/1069433394624204981/1073304542336262175/chrome_ZpzwW69YqS.png)

35. Scroll down to "Privileged Gateway Intents" and enable all of the settings. This will ensure the bot has the permissions it needs now and for potential future updates.

![35](https://cdn.discordapp.com/attachments/1069433394624204981/1073305373425020978/chrome_FKuSohDnSc.png)

36. Click on save then scroll up to the Token section and copy your token. If this option is not available, reset your token then it will be. Paste this into your ccgm_config file.

![36_1](https://cdn.discordapp.com/attachments/1069433394624204981/1073306285300256798/chrome_tkVDn0y0lx.png)
![36_2](https://cdn.discordapp.com/attachments/1069433394624204981/1073306285564506202/DkhvtbRACv.png)

37. Now we need to invite your Discord bot to your group. To do this head over to "OAuth2 -> URL Generator". In Scopes click on "Bot" and in Bot Permissions click on "Administrator".

![37](https://cdn.discordapp.com/attachments/1069433394624204981/1073307081869897888/chrome_HDc21MESRb.png)

38. Scroll to the very bottom and copy the "Generated URL". Paste it into a new tab on your web browser. Now you can invite the bot to your group!

![38](https://cdn.discordapp.com/attachments/1069433394624204981/1073307603532251217/chrome_9B0Nhcb5M1.png)
![38_2](https://cdn.discordapp.com/attachments/1069433394624204981/1073307603901358121/chrome_oKZxpMDanW.png)

39. For discordInfoBotToken you will need to repeat steps #33 - #38 and create a second Discord bot. This bot will handle your leaderboards as well as your invite codes. When you're done, copy the token and paste it into your ccgm_config

![39](https://cdn.discordapp.com/attachments/1069433394624204981/1073308427599753246/atom_khIE0H6CXC.png)

40. Finally, for steamApiKey head over to https://steamcommunity.com/dev/apikey and create a new one. If one is already there and you didn't create it, change your Steam password and revoke this key. Your shit is hacked fam. Copy your api key and paste it into your ccgm_config.

![40](https://cdn.discordapp.com/attachments/1069433394624204981/1073309279165091850/chrome_3yuloQM6S4.png)

41. Now you're done! 

If you're hosting multiple servers:
Run Steam in each of the sandboxes you've created under a different login 
(see this message for how to configure multiple servers in your ccgm_config) ⁠setup-guide⁠ 

If you're hosting one server and are planning to play on the account you're hosting with
Run Steam normally, sandbox is not required.

Now start up CCGM
To do this, open the "web_server.bat", "discord_bot.bat" and "discord_bot_info.bat" files. Now you can head over to your commands channel and type in "!start shortName" (mine is bigchungus so I did "!start bigchungus"). 

If you need help with commands, say !help in your Discord and the bot will give you assistance.

NOTE #1: If you want to host multiple servers you'll need to make a copy of your server's config (not the entire thing) then you'll need to configure the new one to your liking by following steps #1 - #22 

![Vid2](https://cdn.discordapp.com/attachments/1103081221916987393/1103175333261365358/adding_another_server.gif)

NOTE #2: If you're hosting multiple servers or you're hosting on a VPS I recommend enabling batchmode for Crab Game. This will make the game draw no graphics (removing the need for your VPS to have a graphics card) and it'll save on CPU and RAM.

To do this, right click your game in Steam go to "properties" and add "-batchmode" to the launch options.
You will need to do this with each Steam account you have open in a sandbox. 

![Vid3](https://cdn.discordapp.com/attachments/1103081221916987393/1103175333651431466/enabling_batchmode.gif)
