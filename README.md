![Tahrovin Banner](img/Tahrovin.png)

First things first: **this list contains adult content and you must be of legal age in your country. This means 18+ in most countries, 21+ in others. It is up to you to be sure of the age requirement in your country. Tahrovin is a collection of different mods from various sources, it does not reflect the views or opinions of any mod author's featured in the list.**

***Having issues with the modlist? [FAQ \& Common Issues](#faq--common-issues)***

Support and general talk about Tahrovin resides on iAmMe's Discord:

[![DiscordButton](img/DiscordButton.png)](https://discord.gg/iammodlist)

# What is Tahrovin Grit ?
Tahrovin Grit is a fork of Tahrovin, a NSFW Skyrim VR modlist. It retains some of the eye-candy its predecessor is known for, but opts for more grounded outfits and slightly less intrusive NSFW mods. It also features light survival gameplay and aims towards a slower-paced character growth, reworking many gameplay mechanics to provide a well-balanced challenge throughout your playthrough.

# Before You Start
Before you dive in, there's a couple things you need to be sure of first:

## Hardware Requirements
The following specs are recommended for the best experience:
  * CPU: Intel 7th gen *OR* AMD Ryzen 3000 series 
  * RAM: 16GB of DDR4
  * GPU: RTX 2060 *or the AMD equivalent with at least 6GB of VRAM*

You will need at least `205GB` of disk space on an SSD for the installation. For the downloads, you will need an extra `86GB`- ideally you want *at least* `330GB` for temporary Wabbajack work space. It doesn't have to be an NVMe SSD, but a HDD of any kind will make the list painfully unplayable. 

**If your hardware is less powerful, try the performance tips [here](#my-performance-is-really-bad)**

**If you are using a Quest 2, there are a couple of performance recommendations that you can [find here](Oculus%20Performance%20Tips.md) if you are struggling to get the game to run well.**



## Accounts
In terms of accounts you will need:
  * Nexus Premium Account
  * LoversLab Account

Whilst you don't *need* a Nexus premium account to install the modlist, you'll have a considerably better time of it if you do.

# Installation
Please follow all of steps below if it is your first time installing this modlist, if you're updating you can [jump straight there](#updating-tahrovin).

## Preparation

### Install Microsoft Visual C++ Redistributable Packages
This package is a must as it is needed by MO2 - you may already have it if you've used MO2 before. If you do not have it, you want to download the x64 version under "Visual Studio 2015, 2017 and 2019".

[Download Visual C++ Redistributable Package.](https://docs.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)

### Setup your Page File
Skyrim modlists need a large amount of memory purely because of the amount of *stuff* in them - especially modlists on the larger side or with a lot going on, like Tahrovin. For the best experience, you should setup a pagefile of at least **20GB** - yes, even if you have a million GB of RAM. To setup your pagfile;

1. Hold down the *LEFT* Windows key and press **R**
2. Type in `systempropertiesadvanced` in the run box and then press ENTER
3. Under the "Performance" option, click the "Settings..." button
4. Switch to the "Advanced" tab
5. Under "Virtual Memory", click the "Change..." button
6. Uncheck `Automatically manage...` if it's checked
7. Select your *fastest* SSD in the list of drives
8. Check "Custom Size"
9. Set `Initial Size` to 20480
10. Set `Maximum Size` to 20480 also
    1.  *Note: you can set this up to 40000 if you have the space, this will let the pagefile expand to as large as 40GB*
11. Press the "Set" button
12. Press OK
13. Press APPLY and then OK
14. Restart your PC to apply the pagefile setting

### Setup your Shader Cache
Driver defaults from NVidia and AMD for shader cache size is limited to 4GB. Being this small can lead to rare crashes in heavily modified Skyrim installs. Increasing the shader cache size is done via the NVidia Control Panel (I assume the same for AMD users is true also but I don't have AMD hardware to check with). 

*These instructions are NVidia specific as it is the hardware I have.*

1. Open the NVidia Control Panel
2. Head to `Manage 3D Settings`
3. Scroll down in `Global Settings` to find the `Shader Cache Size` option
4. Set the Shader Cache to *at least* 10GB
5. Done

![Shader Cache](img/ShaderCache.png)

### Configuring Steam
In both global and game settings within Steam and Oculus settings you must ensure the following is set:
  * Supersampling is *OFF*
  * Render Resolution to 100% (1.0 if you're looking at Oculus settings)

### Disable Steam Overlay
The Steam overlay is known to cause issues for both Skyrim VR and regular Skyrim SE/AE, especially when using ENBs. I recommend you turn it off to be sure that it doesn't interfere in any way and you can do so by heading into Steam, right
clicking on Skyrim VR in your game library and clicking **Properties** > **General** > **Deselect "Enable Steam Overlay while in-game"**.

### Set game language to English
Wabbajack and some/most of the modding tools out there only support English language versions of Skyrim. Setting the language to English in Steam will stop issues like Wabbajack file verification failures when installing. As with disabling the overlay, right click on Skyrim VR in your game library and click **Properties** > **Language** > **Select English**.

### Change Steam's Updating Behavior
If for some reason Bethesda decide to release an update for Skyrim VR, everything will probably break. Well, not *everything* but something will definitely break until mods can be updated to suit. To stop this from happening, you need to tell Steam that you only want to update when you tell it to. You can do this by right clicking on Skyrim VR in your game library and clicking **Properties** > **Updates** > **Change Automatic Updates to "Only update this game when I launch it"**. Whilst you're in here, it's also recommended to disable Steam Cloud too.

### Clean current Skyrim VR installation
If you have not yet installed Skyrim VR, you can skip this part.

1. Right click on Skyrim VR in your game library and click **Properties** > **Local Files** > **Browse**. 
2. Uninstall the game via Steam - right click on Skyrim VR in your game library and click **Manage** > **Uninstall**.
3. Check the explorer window for any left over files - if there are any, delete them.
4. Open Windows start menu/search and type in `%LOCALAPPDATA%`.
5. Delete the Skyrim VR folder.
6. Head to `Documents\My Games` and delete the Skyrim VR folder.

### Install Skyrim VR
Once you've done the steps above, you can now set Steam to download Skyrim VR again but ***do not*** install Skyrim VR to a protected folder, such as `Desktop`, `Downloads` or `Program Files` of any kind. It's best to create a new, dedicated folder for it using the Steam Library function somewhere on the root of your drive such as `C:\SteamLibrary`. A lot of people have a dedicated secondary drive for their games, keeping the OS install separate; using this secondary drive will also work.

### Start Skyrim VR
That's right - start the game. You need to let the game do its initial start up jobs such as creating registry entries and generating default config files. Once you've gotten to the main menu you can close the game again.

## Wabbajack
Installing the list is straight forward, Wabbajack will do most of the heavy lifting for you - you only have to tell it where to put stuff. Grab the Tahrovin from the Wabbajack UI, once its downloaded the initial stuff it needs, Wabbajack will have 2 things for you to do - fill in the installation location and the download location. 

Set the installation location to a folder on the root of a drive, something like `C:\Tahrovin`. Do not install it to one of the protected folders as mentioned earlier. The download location will have likely been filled in for you too - ensure it matches the directory you set for the installation location, or if you have multiple Skyrim VR modlists installed, use a common download folder - this will stop you from having to redownload common mods across multiple modlists. 

Before you hit **GO**, a quick tip:

*To get the best performance with Wabbajack, it is recommended that you have the install folder for Wabbajack, the modlist folder and the downloads folder on an SSD; ideally the same SSD.* After the installation is complete, you can move the downloads folder to a storage HDD or other storage medium to save space on your game installation drive. It's not recommended to allow your drive to exceed 90% of its storage space used - Windows Explorer will show a red bar under your drive if you do go over 90% so you need to be sure that you have enough space on your installation drive so that you won't exceed this 90% storage level.

Once you have everything set in Wabbajack, hit **GO** and let it do its thing. It might take a while as there is a fair bit to download and the speed of this will depend on your internet performance as well as your CPU in the later stages for hashing and unpacking the downloads.

## Commonly Failing Downloads
Downloads from file hosts such as Google Drive and Mega can sometimes be a pain and refuse to download automatically via Wabbajack for reasons unknown. Any files that might give you trouble [can be found here for manual download](https://github.com/iAmMe27/Tahrovin/wiki/Commonly-Failing-Downloads).

Download these files and place them *as they are* into the same folder you told Wabbajack to put your downloads in. Let me reiterate just to be sure - **do not unzip the archives!**

## Troubleshooting
If you're having issues with installation, check the [troubleshooting page](Troubleshooting.md). 

# Post-Installation
Almost there but we're not out of the woods yet! After Wabbajack has given you the installation successful screen, you're free to close it. Navigate to the Tahrovin installation folder and run MO2 by double-clicking `ModOrganizer.exe`.

***DO NOT UNDER ANY CIRCUMSTANCES RUN LOOT. The load order is exactly as intended out of the box and you do not need to change it.***

## Stock Game
Tahrovin utilises the stock game feature offered by Wabbajack, meaning that Wabbajack will make a local copy of your Skyrim VR game files during the installation process. This means that your Steam installation of Skyrim VR is completely untouched, even by files that go in the game folder such as ENB files.

## Community Shaders
As a note the first time Community Shaders runs it will have to compile shaders, this may take a while and may look like SkyrimVR is frozen, just be patient. This process will also most likely be repeated any time you change mods in the list.
The Community Shaders Menu can be opened with END and from here you can toggle individual shaders on and off.

## Skyrim VR Upscaler Selection
Like in the previous section, Skyrim VR Upscaler options are found in MO2 under the `Skyrim VR Upscaler` separator. 

Remember, AMD and non-RTX GPU's must use **FSR** and not DLSS or DLAA.

![Upscaler Selection](img/UpscalerSelection.png)

## Creating a desktop shortcut
Nobody wants to be launching their game via multiple clicks, they want to be able to do it from the desktop! This is simple to do - open MO2, ensure **Tahrovin** is selected in the dropdown and click the "Shortcut" button. From the small dropdown menu, click "Desktop". Of course, you can always run from inside of MO2 by clicking the "Run" button instead.

![Desktop Shortcut Creation](img/DesktopShortcut00.png)

Done! You should now have a shortcut on your desktop which you can now run the modlist from. Don't run Skyrim VR from within Steam as it won't launch MO2's virtual file system to make a modded game instance.

## Swapping between SteamVR and OpenComposite Binaries
See Oculus performance tips
[Oculus Performance Tips](Oculus%20Performance%20Tips.md)

# Pre-Game Launch

**Before launching the game, make sure your VR headset is initialised and both controllers are connected. Launching the game, without both of these conditions met will be a bad time.**

## DLSS/FSR/XeSS

Refer to the [Skyrim VR Upscaler](#skyrim-vr-upscaler-selection) section.

## Optional mods

Before starting, you can make choices in the Optional sections of the list, colored in Orange in MO2. Pick a set of controller bindings, a defeat mod, a Vampire Lord body mod depending on your character's gender, and any of the other optional mods that interest you. Make sure to do so **before you start a new game** as enabling or disabling some of these mods mid-save can be a bad idea : 

- Vanilla Start : New games will start with the vanilla skyrim intro instead od throwing you straight into the Realm of Lorkhan
- Quickloot VR : Adds a looting menu similar to the one present in FO4
- Smalls : Adds underwear to bodies when you loot them, doesn't work well with Quickloot.
- Shadow of Skyrim - SL on defeat : Defeat system. Starts a sexlab scene whenever you are defeated by an enemy. It is integrated into the Shadow of Skyrim Nemesis system, but there's no configuration available to customize it. **Disable this if you don't want to get a forced sex scene on defeat.**
- Yamete Redux : Alternative defeat system. It will require manual MCM configuration and is known to be finnicky.
- CBPC VRSex - Sexlab Solutions Override : Will use the CBPC VRSex system instead of Sexlab to handle any sex interactions started by the Sexlab Solutions mod between the player and a female NPC, as long as the player is not in a victim context.
- Dragonborn speaks naturally : Grants the ability to use voice commands to do things such as equip spells and items, shout, or select dialogue options. Requires Windows speech recognition.
-  Occlusion FPS Boost : Should give you an FPS boost when outside, at the cost of some rare flickering in specific places (detected on some setups in the Windhelm bridge and on the College's bridge)
-  Daedric Bitchs : Optional followers 
-  Additemmenu : Lets you add items as you wish
-  Strafing Nerf : Reduces your speed when going backwards or strafing to the side, making it a bit harder to avoid attacks and run circles around your enemies

# Mod Setup

### *THIS STEP IS IMPORTANT! IF YOU DO NOT DO THIS STEP, YOUR GAME WILL NOT FUNCTION CORRECTLY!*

When starting a new game, create your character and once done, *DO NOTHING ELSE* and allow the mods to initialise. Once the notifications stop appearing in the top left of your view, you should calibrate VRIK by using the `VRIK Calibration Power` located in your powers menu. Do this while standing on a flat surface in game. Follow the instructions in the VRIK pop-up dialog to ensure you get this right, otherwise you might find yourself towering over everyone else or way too short. Don't worry about making it absolutely perfect, you can recalibrate at any time. After you've calibrated VRIK, head to the Mod Configuration Menu to start the mod setup.

The MCM setup is *mostly* automated and will run on its own after you've finished character creation. As mentioned, *DO NOTHING* until the window pops-up telling you to save.

When you are done, **save your game, go back to the main menu, then load that save** so the last few mods can load properly.

That done, there are optional configuration changes you may wish to make in the Mod Configuration Menu :

- The CBPC VRSex mod will create basic sex interactions with NPCs without taking control of the player, but requires the player to have a penis. If you wish to use it but are playing a female character, the mod can let your character grow a penis temporarily during VRSex scenes. Go to CBPC VRsex and check the "Auto-futa" option. Don't check the option if you are playing a male character, or a female character that is already permanently futa. *(Edit : Penis not required anymore, though you can still add it if you like)*
![VRSexMCM](img/VRSexAutofuta.jpeg)
- Creature animations may play if you selected a defeat mod among the optional NSFW mods, or if you use the Sexlab Enchantress spells. If you would like to disable them, go to Sexlab > Animation Settings > Allow Creature Animation.
![SexlabMCM](img/DisableCreatures.jpeg)
- Sexlab Romance will give you [Romance] dialog prompts to attempt to seduce any NPC by default. If you would like to limit this, disable the "Enable Dialogue for Male NPCs" and/or "Enable Dialogue for Female NPCs" options in the Sexlab Romance MCM.
![SexlabRomanceMCM](img/Romance.jpg)

## Controller Bindings
[Controller bindings can be found here](ControllerBindings.md)

## Essential VR mod tutorials
If this is your first time playing Skyrim VR, you may want to watch these tutorial videos to understand how some of the essential mods function.
- https://youtu.be/CEi7gwN8hgg
- https://youtu.be/Nd9A-_G2eXU

## Starting out
When you first start a new game, depending on your choice of optional mods, you may either play through the vanilla intro, or skip it and find yourself directly inside the Realm of Lorkhan where you will set up your character.

*If you chose the vanilla start, you will still be able to reach the Realm of Lorkhan during the intro from a crystal inside Helgen's keep.* 

The Realm of Lorkhan mod allows you to craft your character. You may pick a shrine and standing stone bonus to start with. Make sure to speak with Sera the Trainer to increase your starting skills as you wish. If you don't get a training dialog when talking to her, make sure you followed my earlier instructions by **saving your game, going back to the main menu then reloading.**

The training system offered by Sera the Trainer is available throughout all of Skyrim. Most NPCs will offer you training in a few skills they are skilled in. To train, you will need gold and Training Points (TP) which you will gain at each level up. This is the main way to increase your skills, as regular skill leveling has been drastically slowed down. You can check your available TP at any time through the Training Potential power. The gold required to train will change depending on factors such as your skill level, your trainer's skill level and your relationship with the trainer (friends charge less).

![SeraTrainer](img/TrainerSera.jpeg)

Sera the Trainer charges less gold for her training than most other trainers in Skyrim. Don't skip out on the opportunity to raise some of your skills here, but consider keeping at least a little bit of gold for later.

Once you teleport at one of the crystals, you'll be dumped into Skyrim in the place you chose. Make your choices wisely though - once you leave, you cannot return.

## CBPC VRSex
[CBPC VRSex](https://www.loverslab.com/files/file/29662-cbpc-vrsex/) is a mod to create basic sex interactions without taking control away from the player. ~~It requires the player to have a penis. If you are playing a non-futa female, you may use the "Auto-futa" option in the MCM to temporarily grow a penis during VRSex scenes.~~ Penis not required anymore, vagina on vagina collision works fine now. Though you can still use Auto-futa if you'd like.

If you wish to use that system, read the manual in your inventory or on the stand next to the "VRSex Training Dummy" NPC in the Realm of Lorkhan. Feel free to try out the mod on that Training Dummy to figure out how things work.

Upon opening the manual, you will be asked for an orientation which will activate the mod for either Male NPCs, Female NPCs, or both. If you choose Male or Female NPCs, entering an ostim or sexlab sex scene with the other gender will also give you a temporary 'disgust' debuff. If you choose both, you will never get a debuff but some VRSex buffs will be harder to obtain.

To start, I recommend activating the Incubus Arts power then groping the VRSex dummy until she collapses. You can either keep groping her while she's collapsed, or use the Molag Bal's Compulsion spell to force her to take a pose. There are only two poses at the moment, chosen at random. Just cast Molag Bal's Compulsion spell again to switch. Either way, if you keep groping her, your character should strip and get an erection. The mod will then detect collision between penis and vagina, so set yourself in the right position and start having sex. After a little while, you will receive bonuses depending on the level of your partner. If your partner is lower level than you are, this will likely only be a temporary stat boost, but a higher level partner may grant you a permanent point of health or magicka. Details on these bonuses are described in the VRSex Manual.

You can technically also use the Knockout Arts power instead of Incubus Arts, but a starting character will find it extremely hard to use. The knockout combo will only activate if you have 90 stamina. As parrying uses up your stamina, you will often find yourself parrying an enemy attack and ruining the combo. Before you start using Knockout Arts instead of Incubus Arts, either increase your warrior skills to learn Improved Knockout Arts or increase your stamina.

The third option, Molag Bal's Subjugation, is easier to use than both Incubus Arts and Knockout Arts but is entirely unavailable as a starting character and requires investing into Illusion.

## Sexlab and Ostim
Sexlab scenes are used in this list mostly in three situations : You are defeated by an enemy, you use Sexlab Enchantress spells, or you start a scene from Sexlab Solutions.
Sexlab scenes can be directed through gestures, similarly to vrik gestures, though if nothing is done they will complete automatically.

Ostim scenes are started by most of the other mods, such as the Romance mod, the follower mods or Amorous Adventures. 
Ostim scenes can be directed by using the Spell Wheel.

As long as there is penetration, you will still receive the bonuses from CBPC VRSex during Sexlab or Ostim scenes.

## Playing a mage
Being able to use magic is not a given in Tahrovin Grit and will require an investment. Your magicka regeneration in combat is faster, but your starting magicka is only 50 and you do not start with any spells (other than the various debug spells) unless you are one of the races granted a bonus spell (Breton, Dunmer, Altmer). Furthermore, you will find that spell books are prohibitively expensive for a starting character. You will still find spell books in the world as usual, but it may be tempting to sell them instead of learning the spell they contain.

Rather than spell books, your main way to acquire new spells will be through Spell Forging. To do so, you must first read the [Spellforge](https://www.nexusmods.com/skyrimspecialedition/mods/46482) book in your inventory. Let the spell library initialize, it will then display a menu. Pick the "Conjure Forge" option to learn the spell and close the menu.

If you want to start the game as a mage right away, I recommend doing the following : 
- Increase your magicka by picking the Mage, Lady or Atronach standing stones, otherwise you'll lack the magicka to even forge novice spells at first. As a more temporary measure, Julianos' shrine can also help. Note that Altmer already start with an extra 50 magicka and may not necessarily need to do that.
- Increase one of your magic skills to at least 20 at Sera the Trainer if possible. You should have enough gold and TP to raise a skill to 20 right away. This will allow you to learn a novice spell through Spellforge immediately.

Cast the "Conjure Spellforge" spell on the ground to summon the forge and select the bottom node to access the forge's main functions. Select the Resin Experimentation option.
![SpellforgeMain](img/SpellforgeMain.jpeg)

For every level you reach above 15 in a magic skill, you will receive School Theses upon using the Resin Experimentation option. Later, you will also be able to use this menu to create Arcane Resin by incinerating alchemy ingredients in the forge. If you've raised a magic skill to 20 earlier, you should immediately receive 10 school theses here.
![SpellforgeResearch](img/SpellforgeResearch.jpeg)

Exit the spellforge menu, use the middle node in the forge and select the school you have trained in.
![SpellforgeSelectSchool](img/SpellforgeSelectSchool.jpeg)

Once set, use the bottom node again and select Spell Forging > Synthesize spell selection. This will grant you a selection of all spells that match your specifications - here you should see all available Novice spells from your selected school, but later you can use the middle and top nodes in the forge to restrict that list further. Select a spell and exit the menu.
![SpellforgeSpellPick](img/SpellforgeSpellPick.jpeg)

You will automatically equip an "enkindle" ability that you can channel to drain your magicka to power the forge. If you have enough magicka (60 for a novice spell) and channeled the enkindle ability to completion, the forging process is finished and you will receive the spell. Don't worry, if you fail you can retrieve your school theses and resin by interacting with the forge (nothing is lost).

As you play, keep raising your magic skills to gain more school theses and learn more spells. You can also create Arcane Resin by experimenting with ingredients in the spellforge, which will work the same as School Theses but allow you to learn spells from any school. Read the spellforge mod description (https://www.nexusmods.com/skyrimspecialedition/mods/46482) for more details. Creating Arcane Resin through Spellforge usually requires powerful ingredients such as Nirnroot. However, some recipes work with large quantities of mundane ingredients (such as 10 units of Bone Meals). If you try to experiment with the wrong quantities, you will still learn the recipe for later, with the exact quantity needed. If you have a decently valuable alchemy ingredient, try to throw it in the Spellforge and see what happens !


Other changes compared to base Tahrovin : 
- Triumvirate has been removed
- [Balance adjustments for Apocalypse](https://www.nexusmods.com/skyrimspecialedition/mods/104987) deals with the worst offenders, such as turning Ocato's Recital into a series of perks or switching Ghostwalk from a novice to an expert spell.
- Two Darenii spell packs have been added, [Abyss](https://www.nexusmods.com/skyrimspecialedition/mods/83329) and [Arcane](https://www.nexusmods.com/skyrimspecialedition/mods/91602).
- [Thaumaturgy](https://www.nexusmods.com/skyrimspecialedition/mods/57138) rebalances enchanted items
- [Sexlab Enchantress](https://www.loverslab.com/files/file/9712-sexlab-enchantress-se) provides sexlab-related versions of the basic illusion spells. These spells do not replace the actual basic illusion spells here, there will usually be a regular version and an erotic version of the spell that can be learned separately.  
- The [Spellsiphon](https://www.nexusmods.com/skyrimspecialedition/mods/26627) magic system is available, but not immediately. To unlock the Spellsiphon Urn in your inventory, you will need at least 20 Restoration and either 20 Destruction or 20 Conjuration.
- Various other small additions : [Immersive Bend Will](https://www.nexusmods.com/skyrimspecialedition/mods/62233), [Perception](https://www.nexusmods.com/skyrimspecialedition/mods/7559), [NPCs react to Necromancy](https://www.nexusmods.com/skyrimspecialedition/mods/70428)[/Invisibility](https://www.nexusmods.com/skyrimspecialedition/mods/91480).
- Sexlab Eager NPCs has been removed, and [Sexlab Romance](https://www.loverslab.com/topic/127240-sexlab-romance-se/) has been added.

## Playing a warrior
The main change you will notice as a warrior is that vanilla blocking has been removed entirely in favor of [Pseudo Physical Weapon Collision and Parry](https://www.nexusmods.com/skyrimspecialedition/mods/100781). To block with a shield, you no longer simply have to hold the shield in front of you. You must intercept the enemy's attack with it, while holding the trigger button. If you have a timed-block perk, you can trigger it by pressing the trigger to block at the moment of impact. Weapons no longer block at all, they can only use the Pseudo-physical parry system by intercepting the enemy's attack. By moving the weapon or shield fast enough as you parry or block, you may even stagger the enemy. Blocking with a shield will cost Stamina instead of Health. Parrying with a weapon will cost stamina if you are slow, but if you move the weapon fast enough you will regain Stamina instead of losing it. If you are out of Stamina, weapon parrying becomes impossible and shield blocking starts to use Health instead.

You will also be able to block and parry arrows and spell projectiles by intercepting them physically. While holding trigger, projectiles will be slowed at the cost of a bit of magicka, making that process easier.

The settings for pseudo-physical parry are less forgiving than the ones in base Tahrovin. You will not be able to parry by simply standing still, make sure to move your weapon as you intercept.

You can throw humanoid enemies either by yanking them with both hands, or by yanking their foot. This requires a fair amount of stamina, but not only will it make the enemy vulnerable, if they have 50% health or less it will also give you a brief window while they are down during which you will be able to strip them of their weapon and/or armor, by either grabbing them with both hands or using the gravity glove. Some of the new perks in Light and Heavy armor will make you better at throwing enemies around.

All attacks, even basic ones, cost a bit of stamina depending on the type of weapon being used (less stamina for daggers, more for two-handed weapons, and even more for two-handed weapons wielded with one hand). When out of Stamina, you will be slower and deal significantly less damage. It might be better to pace yourself and focus on defense when you start running low - remember that a fast enough parry will also help you regain Stamina.

[Weapon Throw VR](https://www.nexusmods.com/skyrimspecialedition/mods/31374) is present, but is meant to be used only with specific throwing weapons. These weapons are cheap, disposable and relatively weak in melee, but much more effective when thrown. They can be bought in shops or crafted.

Finally, you will no longer be able to do power attacks unless you are able to pay the full stamina cost.

## Playing a thief
Pickpocketing and lockpicking are harder than usual if you're unskilled, but easier if you do raise your skills. [More NPC Pocket Money](https://www.nexusmods.com/skyrimspecialedition/mods/31375) adds a bit of extra gold to citizens for you to steal. [Lock-related Loot](https://www.nexusmods.com/skyrimspecialedition/mods/11342) makes sure that Expert-level chest whose lock you just picked doesn't contain three gold pieces and a sweetroll. [Broken picks](https://www.nexusmods.com/skyrimspecialedition/mods/95275) makes it so breaking your lockpick will throw you out of the lockpicking minigame and force you to start from scratch - make sure to check for patrolling guards ! [Mum's the word NG](https://www.nexusmods.com/skyrimspecialedition/mods/77409) ensures that low-value loot will no longer be flagged as stolen and can be sold anywhere. Even for the more valuable loot, you will no longer have to join the thieves' guild to sell it : anything recognizably stolen can now be sold at any Khajiit caravan.

Some of the perk changes from the usual [Vokriinator](https://www.nexusmods.com/skyrimspecialedition/mods/26702) stuff will impact thieves. Most importantly, the Pickpocket and Lockpicking Mastery perks will now allow you to train both skills at once for the price of one. [Disguise](https://www.nexusmods.com/skyrimspecialedition/mods/133426) adds a series of Speech perk that allows you to disguise your identity and can be very useful to evade bounties or avoid getting them in the first place.

## Leveling
Instead of increasing your level by raising your skills, the [Experience](https://www.nexusmods.com/skyrimspecialedition/mods/17751) mod lets you increase your level as you adventure, exploring Skyrim and accomplishing quests. The leveling curve has been modified to provide a slower-paced experience.

Levels and skills have not been decoupled however. As explained earlier, you will be able to train your skills as you wish each level thanks to [Trainers Galore](https://www.nexusmods.com/skyrimspecialedition/mods/20360) and its [Training Points](https://www.nexusmods.com/skyrimspecialedition/mods/103092) addon. Almost every NPC can now train you in a few skills as long as you have the gold and the Training Points. Note that any buffs or penalties you may receive to experience gain will also apply to training. It is also important to note that improving your relationship with a trainer will make the gold cost of training cheaper, but that more skilled trainers will charge more.

Skyrim's regular skill leveling is not gone, but is now much slower. Your skills start at 5. You may be able to progress through the lower levels of skill entirely on your own, but you will have a hard time going further without seeking training.

At higher levels, you may have a hard time finding a sufficiently-skilled trainer. In that case, scrolls of the Ethereal Instructor are sold by many merchants, and can be crafted at a tanning rack. They are fairly expensive but can be an alternative way to find proper training by summoning Master-level trainers.

## Crafting and Economy
You may notice that the only crafting workstations you are able to use from the start are the Tanning Rack and the Smelter. Otherwise, you will need to increase your skills first. Smithing workstations require a smithing skill of 15. Alchemy and Enchanting workstations require their skill at 20.

Until you learn to craft for yourself, smiths and enchanters of skyrim can do the work for you thanks to Honed Metal. Tempering services are the cheapest ones, crafting services are in the middle, and enchanting services are fairly expensive. Prices will of course depend on the equipment being tempered/crafted, but also on the artisan - the more skilled they are, the more gold they'll ask for. There will be a noticeable bump in prices for even cheaper item when the artisan reaches a skill of 40 and again at 79. If you ask Eorlund Gray-Mane to craft an iron dagger, it's going to cost you a lot more than asking Adrianne Avenicci.

[Durability VR](https://www.nexusmods.com/skyrimspecialedition/mods/76830) makes weapons, armor and clothing slowly degrade as you use them. This is a slow process, but using the same equipment for a very long time without maintaining it will eventually break it. To keep the equipment in good condition, you will have to temper it. Many of the armors you will receive from enemy loot will also be degraded and require tempering before you can use them. The better-tempered the equipment and the more skill you have with it, the slower the degradation. Magic weapons also degrade more slowly and artifacts are extremely resilient. 

At first, you may not be able to temper your equipment due to the smithing skill requirement, but you will still be able to repair your equipment yourself through [Immersive Smithing](https://www.nexusmods.com/skyrimspecialedition/mods/72298). Go to a forge and equip the Blacksmith Hammer in your inventory. The ingame tutorial should guide you through the process. Careful however, not even Immersive Smithing will be able to repair enchanted equipment without the Arcane Blacksmith smithing perk ! Until then, you will need the services of a more skilled blacksmith to repair enchanted gear.

Once you have 15 smithing you will be able to temper clothing as well at the armor table to repair it or extend its durability, using Linen Wraps. **Repairing Enchanted Clothing requires either the Arcane Blacksmith perk, just like with armor or weapons, or an Enchanting skill of at least 50.**

[Trade and Barter](https://www.nexusmods.com/skyrimspecialedition/mods/23081) alters the prices at which items are bought and sold, making it more difficult to make money through trade and making the various gold sinks (training, equipment maintenance, defeat...) more meaningful.

If you're short on gold and lacking leads on how to make more, [Missives](https://www.nexusmods.com/skyrimspecialedition/mods/17576) quests can help you get back on track. Simply check the quest bulletin board that can be found in any major city. If a missive board doesn't give you a list of quests immediately on your first activation, wait a few moments and try again.

You can also make some gold by playing [Triple Triad](https://www.nexusmods.com/skyrimspecialedition/mods/42522), but that will require an initial investment to buy the board and cards.

## Survival and needs
Tahrovin Grit uses [Sunhelm](https://www.nexusmods.com/skyrimspecialedition/mods/39414) and a stripped-down version of [Campsite](https://www.nexusmods.com/skyrimspecialedition/mods/22353) for its Survival elements. Eat, drink and sleep regularly to keep yourself in top condition, and avoid staying out in the cold too long without adequate protection. 
Buy or craft a tent at a tanning rack to sleep out in the wild - but be wary of night ambushes from [Sands of Time Sleeping Encounters](https://www.nexusmods.com/skyrimspecialedition/mods/8257) !

If you have enough firewood in your inventory, you can use it by selecting it in your inventory to create campfires and warm yourself up. By setting a tent near trees, you may turn it into a Wood-chopping tent and get some more firewood for your campfire, but make sure you have a Woodcutter's axe to chop the wood !

Fast travel is disabled, but can still be employed through one-shot scrolls of Rapid Transportation, available at general vendors, court wizards, and generally any merchant that would sell soulgems. These scrolls can also be crafted by converting common soulgems at a Tanning Rack. Using this method regularly can be expensive until late game though - until then, there are now more carriage routes available thanks to [Carriage and Ferry Travel Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/8379). 

Consider buying a horse when able, but take care not to get them killed. A horse will also be useful to carry more things : Thanks to [Horse Storage](https://www.nexusmods.com/skyrimspecialedition/mods/3838) you can access your horse's inventory by sneaking while activating them. You can also call your horse at any time while you are outside with the [Call your Horse](https://www.nexusmods.com/skyrimspecialedition/mods/49595) power.

Animals will drop a little bit more loot, and their pelts are now a bit more valuable. It will not necessarily always be better to turn it all into leather. 

Cooking is now a bit easier as most recipes won't use up Salt Piles anymore. You still need to keep a salt pile in your inventory, it just won't be used up every time you cook something.

## Enemies and encounters
Encounter zones have been slightly increased, and new enemies have been added with [Hand-Placed Enemies](https://www.nexusmods.com/skyrimspecialedition/mods/59249). [Locational Encounter Zones](https://www.nexusmods.com/skyrimspecialedition/mods/85212) ensures that even in the overworld, enemies will match the level of their encounter zone.
New random overworld encounters have been added through [Extended Encounters](https://www.nexusmods.com/skyrimspecialedition/mods/44810).

[Dragon Combat Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/56082) makes dragons smarter and grants them powerful new abilities. Their attacks are also generally stronger, and they have extra resistance to attacks that do not come directly from you.

## Death
[Shadow of Skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/65136) means death is not the end. Upon defeat, you will generally be assaulted by the victor in a Sexlab Scene. In most cases they will become your Nemesis and grow in power. Meanwhile, you will receive a penalty : either (100*your level) in gold, or a dragon soul if you don't have the gold, or one or more permanent points of health (depending on your level) if you don't have the soul either (note that you will be able to regain permanent health points through CBPC VRSex). You will also receive a situational or random debuff.

It's not all bad however - going back and defeating your Nemesis will not only grant you some experience, but it will also transform that debuff into a related permanent buff, up to a total maximum of 5 buffs and debuffs from this mod.

Note that if your followers are still fighting when you are defeated, they will have a 60-second grace period where they can still save you. If they manage to finish the fight during that period, you will not suffer any penalties.

## Followers
When a follower falls in combat, they will not get back up by themselves until the combat is over. If you want them back in the fight, you can heal them with healing spells, or with a potion.
To feed a potion to a follower, simply put it in your hand with Spellwheel, put it in your follower's mouth and let it drop.
You can also simply throw the potion at the ground next to the follower to apply the effect.

While followers may be a powerful asset, having too many of them may be detrimental to your own growth. If you have two or more followers, you will get less experience from exploring, clearing areas, or completing quests and objectives. The more followers you have, the less experience you will get: 
- 1 follower : No EXP penalty
- 2 followers : -10% EXP from quests, -30% EXP from exploring and clearing areas
- 3 followers : -20% EXP from quests, -70% EXP from exploring and clearing areas
- 4+ followers : -30% EXP from quests, no EXP from exploring and clearing areas

The Leadership speech perk will allow you to bring more followers without a penalty.

Daegon has been removed but new followers have been added : [Misty Skye](https://www.nexusmods.com/skyrimspecialedition/mods/16374) and [M'rissi](https://www.nexusmods.com/skyrimspecialedition/mods/9666).

## Quests
The encounter zones for the main quest, starting from Bleak Falls Barrow, have been increased. I would not recommend trying to get through it at level 1. The reason for this is that going through the main quest would unlock dragons, and you do *not* want to fight a dragon at level 1 in this list. On the other hand, who knows - if you can manage to get through Bleak Falls Barrow even at a low level, maybe you'll be able to handle yourself against a dragon just fine.

Delaying the main quest doesn't mean Alduin will stay put forever. After 90 days, if you haven't finished the main quest, Alduin will come seeking to destroy you. This will be an easier fight than the actual, full-powered Alduin you will have to fight in the main quest, but you should still make sure you have grown strong enough to fend him off. Once you do, you will have 20 more days before he seeks you out again. Take care and don't slack off on your training : every time he comes back, Alduin will be even more powerful !

Besides that, a few quests have been added : [Amorous Adventures](https://www.loverslab.com/topic/109518-amorous-adventures-34-sse-for-lovers-lab/) (with the player text revision), [The forgotten city](https://www.nexusmods.com/skyrimspecialedition/mods/1179), [The chain of time](https://www.nexusmods.com/skyrimspecialedition/mods/95062), [Midwood Isle](https://www.nexusmods.com/skyrimspecialedition/mods/28120), [Fortune's Tradehouse](https://www.nexusmods.com/skyrimspecialedition/mods/22755), [The shadow of Meresis](https://www.nexusmods.com/skyrimspecialedition/mods/38167), [Meridia's Order](https://www.nexusmods.com/skyrimspecialedition/mods/102584), [Identity Crisis](https://www.nexusmods.com/skyrimspecialedition/mods/39634), and many of [jayserpa's vanilla quest expansions](https://www.nexusmods.com/skyrimspecialedition/users/5201727) have been integrated.

## Other changes
- [Mundus](https://www.nexusmods.com/skyrimspecialedition/mods/33411) is the standing stone overhaul
- [Aetherius](https://www.nexusmods.com/skyrimspecialedition/mods/26686) is the race overhaul
- [Alchemy Potions and Food Adjustments](https://www.nexusmods.com/skyrimspecialedition/mods/5877) is the alchemy overhaul 
- [Quickloot VR](https://www.nexusmods.com/skyrimspecialedition/mods/102094) reduces the amount of menus
- [Reading is good](https://www.nexusmods.com/skyrimspecialedition/mods/42026) means you no longer need to hold on to these skill books forever
- [Voiced books of skyrim](https://www.nexusmods.com/skyrimspecialedition/mods/94436) means you can pop an audiobook while traveling.
- [Onyx Weathers](https://www.nexusmods.com/skyrimspecialedition/mods/36227) replaces the weather mod, with much brighter nights. If that's not enough, I've added a lantern from Eld-beri II to your inventory.
- [Skyshards](https://www.nexusmods.com/skyrimspecialedition/mods/60748) adds mysterious stones for you to hunt down throughout skyrim. Every 3 shards absorbed will grant an experience reward - small at first, but which will get larger every time. Every 15 shards absorbed will grant an extra perk.

## Gameplay advice
- The recommended difficulty for this list is Adept. The mods will provide plenty of difficulty on their own. If you still want to alter the difficulty, consider using the Simply Balanced MCM.

- When training, be on the lookout for experience modifiers. For example, having read skill books will grant you experience modifiers that make your training more effective. However, training while exhausted will make your training less effective. If you are careless, you might not get a full skill level out of it.

- Before you attempt to take down a dragon, make sure you have a good ranged attack. Dragons will absolutely murder you in melee unless you block, parry, or ward against every one of their melee attacks, including when they land on you. Even if you can survive a dragon in close quarters, they will not simply stand by while you hack at them.

- You can open a container normally instead of using Quickloot by keeping the interact button pressed for a second or two.

- CBPC VRSex grants a number of bonuses if you have sex with a higher level character than you, including a permanent point of health or magicka. If you spot a strong enemy and you're not in refractory cooldown, try to take her down nonlethally if you can !

- Sexlab Romance grants you an experience buff on a successful attempt, which can be useful before a training session. It takes many factors into account to calculate whether the target is receptive to your advances : Your speechcraft skill, your relationship with the seduction target, your faction, the target's natural proclitivites, and so on. Notably, cold approaching someone you don't have at least a friendly relationship with is much more likely to fail. Accomplishing a quest for an NPC will often set their disposition to friendly - you'll be able to tell as their greetings change. Of course, if your speechcraft is high enough or there are enough other factors in play, you may not need to bother making friends first. If they turn you down, you can still keep trying again the next day (with worse odds of success).

- When trading, consider which merchants to buy from and sell to.
  - Specialists (blacksmiths, alchemists, court mages) will have better prices than generalist shops. Fences (which includes Khajiit caravans) are particularly expensive.
  - Merchants will offer you discounts if you belong to the same guild, and further discounts if you are guild leader. You will also receive another discount if you are Thane of the city.
  - In big cities like Windhelm or Solitude, you will sell for more but also have to buy for more. The reverse is true in small towns like Riverwood.
  - You will have better prices with merchants of the same race, while merchants of hostile races (such as an argonian and a dunmer, or an altmer and a stormcloak nord) will have worse prices.
  - You will have better prices if the merchant is on friendly terms with you, which can usually be accomplished by completing a task for them. This will also override the "racism" factor entirely.

- NPC Mages can be tricky opponents, especially at low level. Keep in mind that, thanks to [Blade and Blunt](https://www.nexusmods.com/skyrimspecialedition/mods/34549), you can often stagger mages by power-attacking them while they are casting a spell. Once you've staggered them once, there'll be a period where you won't be able to stagger them again. You can also parry most projectiles - including projectile spells - with your weapon or shield. Holding trigger will make the projectiles slightly slower as they approach at the cost of a little magicka, helping you parry. Of course, this doesn't work on area spells.

- You will find a bunch of extra options for lingerie, skimpy clothing and accessories available for crafting at the tanning rack. If you'd rather not have to deal with all that, you can just remove the Tahrovin Lingerie Book from your inventory. If you've lost the book, you can just craft it again at a tanning rack.

## The Extra Quests Profile
When I play Skyrim, I usually like to load it up with a bunch of quests I haven't played before. When my playthrough is done, I'll remove the ones I stumbled upon and add a bunch of new ones for the next playthrough.

Since I'm going to do that for myself anyway, I figured I might as well leave it in for the people who want a lot more quests around ! While I have personally played through all the modded quests in the main profile to ensure they work well and fit the Grit vision, the extra quests profile is completely untested. I can't guarantee the extra quests are good, fit in well, or even if they work fine in VR. It *should* be okay, and I will have done as much patching and research as possible without actually playing through the quests, but who knows !

Safe to say, **only select the Extra Quests profile if you don't mind some potential jank** ! If something doesn't work with this profile, get back to me on Discord and I'll see if I can make a patch.

As I play through more quests, some will eventually be switched from the Extra Quests profile to the main Grit profile and others will likely be added.

## Listing of new and altered perks

Various perks have been modified from base Vokriinator or added. This is a listing so you know more or less what to expect.

| Modified perk  | Skill | Description |
| ------------- | ------------- | ------------- |
| All mastery perks  | All | Prerequisites are now 20/40 instead of 0/20  |
| Adrenaline  | Alchemy 80 | Now increases movement speed by 15% instead of 10% |
| Soul siphon  | Enchanting 20 | Now traps 15% of the victim's soul instead of 5% and works on all killing blows. |
| Staff recharge  | Enchanting 40/70 | Prerequisite lowered to 40, added a second level at enchanting 70 that recharges 20 points per second |
| Iron Fist  | Light Armor 20 | Doesn't work while wearing heavy gauntlets |
| As a leaf  | Light Armor 30 | Also unlocks double jump |
| Windrunner  | Light Armor 50 | Now increases movement speed by 15% instead of 10% |
| Lockpicking Mastery | Lockpicking 20/40 | Weaker/All locks are easier to pick and increases carry weight by 50/100 points. Receiving training in Lockpicking also increases the Pickpocket skill if it is lower. |
| Pickpocket Mastery | Pickpocket 20/40 | Adds 20/40% to your pickpocket chance and increases carry weight by 50/100 points. Receiving training in Pickpocket also increases the Lockpicking skill if it is lower. | 
| Lawless World  | Pickpocket 30 | Petty crimes are slowly forgotten, allowing your bounties for non-violent crimes to decay at a rate of 20% of your Pickpocket skill level each hour. |
| Sneak mastery  | Sneak 20/40 | Increases sneaking effectiveness by 20/40% instead of 15/30% |


| New perk  | Skill | Description |
| ------------- | ------------- | ------------- |
| Light weapon throw | One-handed 40 | You can throw any one-handed weapon, dealing 120% of their regular melee damage. They will return to your hand automatically. |
| Heavy weapon throw | Two-handed 40 | You can throw any two-handed weapon, dealing 120% of their regular melee damage. They will return to your hand automatically. |
| Whirlwind shield | Block 40 | Power attack or Bash to create a whirlwind, reducing strike and arrow damage by 80% and negating spells for 2s. Getting hit within the first 0.4s will stagger the attacker. |
| Mighty grip | Heavy Armor 20/60/100 | Grabbing a character under 60/140/250 Health while your weapons are unsheathed will ragdoll them. |
| Antimagic shell | Heavy Armor 20/50/80 | If wearing all Heavy Armor, increases Magic Resistance by 10/20/30%. |
| Steel fist | Heavy Armor 20 | Increases unarmed damage by 5% of your current Stamina when using unarmed attacks in combat while wearing heavy gauntlets. Requires two free hands. |
| Heavy/Light rider | Heavy Armor/Light armor 30 | Horses you ride move 50% faster and regenerate Stamina faster. |
| Tireless march | Heavy Armor 40/70 | Regenerate 2%/4% of your maximum stamina per second when standing still or walking (but not running or sprinting) while wearing all Heavy Armor. |
| Wrestler | Heavy Armor/Light armor 40 | Characters ragdolled through yanking or Mighty Grip can be looted with the gravity glove even if they are above 50% health. Stamina cost for grabbing enemies is reduced by 70%. |
| Body toss | Light armor 20/80 | Stamina cost of yanking and foot yanking is reduced by 50/90%. |
| Athletics | Light armor 30/70 | Movement speed increased by 10/20% when not wearing Heavy Armor. |
| Marathon runner | Light armor 40 | Sprinting doesn't cost any stamina when outside of combat if not wearing Heavy Armor. |
| Foe flinger | Light armor 60 | You may yank others off their feet with only one hand. |
| Leadership | Speech 20/40 | One/Two of your followers does not count towards XP penalties for having multiple followers. |
| Disguise | Speech 20 | Grants the Disguise power. While enabled, can disguise as a member of various factions by donning that faction's gear while out of sight. You will lose bounties obtained while in disguise if you escape unrecognized.  |
| Method actor | Speech 60/100 | You are 50/99% less likely to be discovered when disguised.  |
| Sharp Eye | Sneak 30 | Grants the at-will powers "Spot Detection" which outlines humanoids within 150 feet detecting you for 30 seconds, and "Night Eye" which grants improved night vision for 120 seconds. |

# FAQ & Common Issues

## My game won't start even after a fresh install!
Check in your `Tahrovin\Stock Game` folder for an `openvr_api.dll` file. If this file is not present, your game cannot start. To solve this, copy the `openvr_api.dll` file from your Skyrim VR Steam installation folder into your `Tahrovin\Stock Game` folder and relaunch.

When using ENB Organizer, **always** disable an option *then* enable another. Not doing this will mess up the files.


## There's a black square / weirdly textured square in the middle of my view
Press END to open the Skyrim Upscaler menu and toggle TAA off and then back on again, the square will go away after this. It may or may not come back next session, just follow the same steps again.
If it's coming back too often, you can prevent it completely by just keeping TAA off in the upscaler menu.

## I get an OpenComposite error when launching the game?
Like this?

![](https://i.imgur.com/3zYQXNz.png)

If you are getting an error message like the screenshot when launching the game, you have OpenComposite enabled for a non-Oculus headset or you are using VirtualDesktop. Disable OpenComposite, enable SteamVR.

## I Crashed!
Giving me that little info is not helpful. 

Make sure you excluded your Tahrovin folder in your antivirus software. If you use an aggressive antivirus package such as Webroot, Bitdefender, Avast etc etc, I urge you to get rid of it and just use Windows Defender.

Please upload (drag and drop the file into the `#tahrovin-support` Discord channel) the most recent crash log from your `Documents\My Games\Skyrim VR\SKSE` folder.

If you have modified Tahrovin, ignore the previous advice and keep to the `#tahrovin-modifications` Discord channel. I will not help you with modified lists in official support categories - less because I don't want to and more because I cannot.

## Where's my UI?
Raise your left hand, palm facing upwards, to activate the compass and your stat bars. Raise your right hand in the same way for your needs bars. If you wish, equip the soul gauges in your inventory and assign them to stats. When it asks for hand offset, I recommend you set the offset to **3**.

## Is there a way for me to see myself?
Go to the VRIK MCM and Activate the Selfie mode. Then, raise your right, left, or both hands above your head depending on your choice and rotate your wrist to turn your character. If you put your hand down, your character should stay in selfie mode - re-raise your hand to disable.

## How do I change my or an NPC's body?
Obody. Default VRIK gesture is Right Thumbstick click + Controller Down. Want to change the Obody gesture? [Read this.](https://github.com/iAmMe27/Tahrovin/wiki/Changing-Autobody-Hotkey)

## Playing in Seated Mode
Tahrovin features the `Auto Sneak and Jump` mod which relies on your movement in real life to jump and crouch, therefore making it not very useful to you if you prefer to play in seated mode. Unless you'd like to try sneaking everywhere you go, you should be fine to disable this mod from the "Gameplay Mods" section in MO2.

## My performance is really bad!
Your CPU or GPU is too weak. Or, you don't have XMP enabled for your RAM.

This will probably happen if you ignored the minimum specifications I wrote near the top of this readme.

There are still a few things you can do to slightly increase performance : 
- Switch from SteamVR to OpenComposite
- Switch from Skyrim Upscaler VR - DLAA to either Skyrim Upscaler VR - DLSS if your GPU allows it, or Skyrim Upscaler VR - FSR 
- Disable everything in the CS Resources section. However, if you are playing an existing game, do not disable Eld-beri.
- Disable everything in the ReShade section
- Activate VR FPS Stabilizer - Occlusion FPS boost
- Reinstall Faster HDT-SMP - VR XML and select AVX or AVX2 if your CPU supports it

## Loading takes too long!
Shouldn't have put the modlist on a HDD - I did warn you earlier in this very readme.

## I have grey hands/Vive wands in game!
Create a new file in the Stock Game folder and name it `opencomposite.ini`. In that file, write a single line consisting of:

`admitUnknownProps=true`

Save, close, relaunch game.

## I can't move!
You started Tahrovin before making sure your controllers were connected. Restart the game.

## I CTD on launch!
Well, that could be a multitude of things. Make sure you Tahrovin folder is added to your antivirus exceptions/allow list and try again.

If you have some heavily aggressive antivirus program such as Webroot, Bitdefender etc, get rid of it.

If you have a non-RTX Nvidia GPU, I ask you to refer to the [DLSS/FSR/XeSS](#dlssfsrxess) section again.

## Can I add XYZ?
I don't know, can you?

# Updating Tahrovin
When an update is released, please always check the [changelog](Changelog.md) first. You may not need to update your modlist but if there is anything that resolves game breaking issues, it'll be noted in the changelog. Backup your saves before you commit to any updates, Wabbajack doesn't usually touch save files, it does has the ability to delete them if it wanted to.

If you have added anything to this modlist at all, Wabbajack will also delete those. You should know how to stop it from doing this if you're going to add stuff to modlists but if you don't, you have to prepend your mod name with `[NoDelete]` - this will make Wabbajack ignore these files. You will need to reinstall these mods and re-sort their load order after an update though, so I hope you kept backup information on where they went in the load order!

All that aside, updates are basically the same as an installation except you have to ensure that you have the "Overwrite" checkbox ticked in Wabbajack.

# Uninstalling Tahrovin
No fancy uninstallation needed, you can just delete the Tahrovin folder and it'll be gone. There'll be no files left inside your Steam installation folder because Tahrovin uses the stock game feature of Wabbajack.

# Thank You's
Many thanks to the Wabbajack team for making this possible at all, to iAmMe for making the original Tahrovin, and to Neochiken for continuing it.
