Allows additional survivor players in coop/survival/realism when 5+ player joins the server
(When 5+ player joins the server but no any bot can be taken over, this plugin will spawn an alive survivor bot for him.)

-AlliedModder-
MultiSlots Improved Version: https://forums.alliedmods.net/showpost.php?p=2715546&postcount=248

-ChangeLog-
v5.2
- Remake Code.
- Translation support.
- Give items and set custom health to new 5+ player.
- Delete all items form survivor bots when they got kicked by this plugin.
- Spawn 5+ Survivor bots when round starts.
- This plugin will not auto move new 5+ player to survivor team if he is already in infected team.
- Spawn extra Medkits for 5+ survivors on new chapter/finale start
- If same player reconnect the server or rejoin survivor team to try get a second free bot, he will be a dead bot.
- Invincible time after new 5+ Survivor spawn by this plugin.
- Remove gamedata

v1.0
-Original Post: https://forums.alliedmods.net/showthread.php?p=1239544

-Require-
1. You still need to use [l4dtoolz](https://github.com/Accelerator74/l4dtoolz/releases) to unlock server slots limit
2. left4dhooks: https://forums.alliedmods.net/showthread.php?p=2684862
3. CreateSurvivorBot: https://forums.alliedmods.net/showpost.php?p=2729883&postcount=16
4. [INC] Multi Colors: https://forums.alliedmods.net/showthread.php?t=247770
5. To unlock all melee weapons in all campaigns, you MUST use [Mission and Weapons - Info Editor]("https://forums.alliedmods.net/showthread.php?t=310586") plugin.

-Conflicts-
-DO NOT modify cvar "survivor_limit" value above 4 in your cfg, otherwise the new 5+ player could spawn in saferoom
-If you have one of following plugins, please delete
1. bebop - additional coop players (20+ players possible): https://forums.alliedmods.net/showthread.php?t=110210"
2. SuperVersus: https://forums.alliedmods.net/showthread.php?p=830069
3. [L4D & L4D2] Bots Control In Coop Mode: https://forums.alliedmods.net/showthread.php?t=175060
4. ABM: A MultiSlots / SuperVersus Alternative: https://forums.alliedmods.net/showthread.php?t=291562

-Convars-
cfg\sourcemod\l4dmultislots.cfg
// How to join the game for new player.
// 0: Old method. Spawn an alive bot first -> new player takes over.
// 1: Switch new player to survivor team (dead state) -> player respawns.
l4d_multislots_join_survior_method "1"

// When 5+ new player joins the server but no any bot can be taken over, the player will appear as a dead survivor if survivors have left start safe area for at least X seconds. (0=Always spawn alive bot for new player)
l4d_multislots_alive_bot_time "0"

// Setup time interval the instruction message to spectator.(0=off)
l4d_multislots_spec_message_interval "25"

// Kick AI Survivor bots if numbers of survivors has exceeded the certain value. (does not kick real player, minimum is 4)
l4d_multislots_max_survivors "4"

// If 1, Spawn 5+ survivor bots when round starts. (Numbers depends on Convar l4d_multislots_max_survivors)
l4d_multislots_spawn_survivors_roundstart "0"

// If 1, when same player reconnect the server or rejoin survivor team but no any bot can be taken over, give him a dead bot. (0=Always spawn alive bot for same player)
l4d_multislots_no_second_free_spawn "0"

// Amount of HP a new 5+ Survivor will spawn with (Def 80)
l4d_multislots_respawnhp "80"

// Amount of buffer HP a new 5+ Survivor will spawn with (Def 20)
l4d_multislots_respawnbuffhp "20"

// (L4D2) First slot weapon for new 5+ Survivor (1-Autoshot, 2-SPAS, 3-M16, 4-SCAR, 5-AK47, 6-SG552, 7-Mil Sniper, 8-AWP, 9-Scout, 10=Hunt Rif, 11=M60, 12=GL, 13-SMG, 14-Sil SMG, 15=MP5, 16-Pump Shot, 17=Chrome Shot, 18=Rand T1, 19=Rand T2, 20=Rand T3, 0=off)
// GL = Grenade Launcher
// Rand T3 = M60 or Grenade Launcher
l4d_multislots_firstweapon "19"

// (L4D2) Second slot weapon for new 5+ Survivor (1- Dual Pistol, 2-Magnum, 3-Chainsaw, 4-Fry Pan, 5-Katana, 6-Shovel, 7-Golfclub, 8-Machete, 9-Cricket, 10=Fireaxe, 11=Knife, 12=Bball Bat, 13=Crowbar, 14=Pitchfork, 15=Guitar, 16=Random, 0=Only Pistol)
l4d_multislots_secondweapon "16"

// (L4D2) Third slot weapon for new 5+ Survivor (1 - Moltov, 2 - Pipe Bomb, 3 - Bile Jar, 4=Random, 0=off)
l4d_multislots_thirdweapon "4"

// (L4D2) Fourth slot weapon for new 5+ Survivor (1 - Medkit, 2 - Defib, 3 - Incendiary Pack, 4 - Explosive Pack, 5=Random, 0=off)
l4d_multislots_forthweapon "0"

// (L4D2) Fifth slot weapon for new 5+ Survivor (1 - Pills, 2 - Adrenaline, 3=Random, 0=off)
l4d_multislots_fifthweapon "0"

// (L4D1) First slot weapon for new 5+ Survivor (1 - Autoshotgun, 2 - M16, 3 - Hunting Rifle, 4 - smg, 5 - shotgun, 6=Random T1, 7=Random T2, 0=off)
l4d_multislots_firstweapon "6"

// (L4D1) Second slot weapon for new 5+ Survivor (1 - Dual Pistol, 0=Only Pistol)
l4d_multislots_secondweapon "1"

// (L4D1) Third slot weapon for new 5+ Survivor (1 - Moltov, 2 - Pipe Bomb, 3=Random, 0=off)
l4d_multislots_thirdweapon "3"

// (L4D1) Fourth slot weapon for new 5+ Survivor (1 - Medkit, 0=off)
l4d_multislots_forthweapon "0"

// (L4D1) Fifth slot weapon for new 5+ Survivor (1 - Pills, 0=off)
l4d_multislots_fifthweapon "0"

// If 1, allow extra first aid kits for 5+ players when the finale is activated, One extra kit per player above four. (0=No extra kits)
l4d_multislots_finale_extra_first_aid "1"

// If 1, allow extra first aid kits for 5+ players when in start saferoom, One extra kit per player above four. (0=No extra kits)
l4d_multislots_saferoom_extra_first_aid "1"

// Delete all items form survivor bots when they got kicked by this plugin. (0=off)
l4d_multislots_bot_items_delete "1"

// Invincible time after new 5+ Survivor spawn by this plugin. (0=off)
l4d_multislots_respawn_invincibletime "3.0"

-Commands-
**Attempt to join Survivors
	sm_join
	sm_js
	
**Attempt to add a survivor bot (this bot will not be kicked by this plugin until someone takes over) (Adm require: ADMFLAG_KICK)
	sm_muladdbot

-Q&A-
1. How could I control the number of bots spawned at the start?
set l4d_multislots_max_survivors whatever value you like.
// Kick AI Survivor bots if numbers of survivors has exceeded the certain value. (does not kick real player, minimum is 4)
l4d_multislots_max_survivors "8"

// If 1, Spawn 5+ survivor bots when round starts. (Numbers depends on Convar l4d_multislots_max_survivors)
l4d_multislots_spawn_survivors_roundstart "1" 

2. How to set 8+ players in coop?
https://github.com/fbef0102/Game-Private_Plugin/tree/main/Tutorial_%E6%95%99%E5%AD%B8%E5%8D%80/English/Game/L4D2/8%2B_Survivors_In_Coop#navigation

3. How to fix 5+ survivor bug ? For example: charger stop, witch attack wrong player, bot model change... etc
https://github.com/fbef0102/Game-Private_Plugin/tree/main/Tutorial_%E6%95%99%E5%AD%B8%E5%8D%80/English/Game/L4D2/8%2B_Survivors_In_Coop#navigation

