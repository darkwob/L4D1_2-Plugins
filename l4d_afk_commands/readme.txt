Adds commands to let the player spectate and join team. (!afk, !survivors, !infected, etc.), but no change team abuse.

-AlliedModder-
AFK and Join Team Commands Improved Version: https://forums.alliedmods.net/showpost.php?p=2719702&postcount=32

-ChangeLog-
v4.4
-Remake Code
-Add translation support.
-Update L4D2 "The Last Stand" gamedata, credit to Lux(https://forums.alliedmods.net/showthread.php?p=2714236)
-Add more convar and limit to prevent players from changing team abuse.
-Add more commands
-No change team abuse
-Player can go idle even if alone in server
-Allow alive survivor player suicides by using '!zs'
-Adm Command "sm_swapto <player> <team>", Adm forces player to swap team
-Compatible with r2comp_unscramble (https://forums.alliedmods.net/showthread.php?t=327711)
-Remove gamedata

v1.2
-Original Post: https://forums.alliedmods.net/showthread.php?p=1130434

-Detail-
* You can't go idle or use command to switch team if you are in one of below situation
1. You startle witch or witch attacks you.
2. You are capped by special infected.
3. You are a dead survivor.
4. Player can switch team until players have left start safe area for at least X seconds. (set time by convar below)
5. Cold Down Time in seconds a player can not change team again after he switches team.
6. Cold Down Time in seconds a player can not change team after he ignites molotov, gas can, firework crate or barrel fuel.
7. Cold Down Time in seconds a player can not change team after he throws molotov, pipe bomb or boomer juice.
8. Infected player can not change team when he has pounced/ridden/charged/smoked a survivor.
9. Cold Down Time in seconds an infected player can not change team after he is spawned as a special infected.


-Require-
1. left4dhooks: https://forums.alliedmods.net/showthread.php?p=2684862
2. [INC] Multi Colors: https://forums.alliedmods.net/showthread.php?t=247770
3. unscramble.inc: https://github.com/raziEiL/r2comp-standalone/blob/master/sourcemod/scripting/include/unscramble.inc

-Notice-
The plugin does not work until survivor has left the saferoom
倖存者出去安全區域之後此插件才會生效

-Convar-
cfg\sourcemod\l4d_afk_commands.cfg
// Cold Down Time in seconds a player can not change team again after he switches team. (0=off)
l4d_afk_commands_changeteam_cooltime_block "10.0"

// If 1, Dead Survivor player can not switch team.
l4d_afk_commands_deadplayer_block "1"

// Player can switch team until players have left start safe area for at least x seconds (0=off).
l4d_afk_commands_during_game_seconds_block "0"

// Cold Down Time in seconds a player can not change team after he ignites molotov, gas can, firework crate or barrel fuel. (0=off).
l4d_afk_commands_igniteprop_cooltime_block "15.0"

// Players with these flags have immune to all 'block' limit (Empty = Everyone, -1: Nobody)
l4d_afk_commands_immue_block_flag "-1"

// Players with these flags have access to use command to infected team. (Empty = Everyone, -1: Nobody)
l4d_afk_commands_infected_access_flag ""

// If 1, Player can not change team when he is capped by special infected.
l4d_afk_commands_infected_attack_block "1"

// If 1, Infected player can not change team when he has pounced/ridden/charged/smoked a survivor.
l4d_afk_commands_infected_cap_block "1"

// Cold Down Time in seconds an infected player can not change team after he is spawned as a special infected. (0=off).
l4d_afk_commands_infected_spawn_cooltime_block "10.0"

// If 1, Block player from using 'jointeam' command in console. (This also blocks player from switching team by choosing team menu)
l4d_afk_commands_pressM_block "1"

// Players with these flags have access to use command to spectator team. (Empty = Everyone, -1: Nobody)
l4d_afk_commands_spec_access_flag ""

// If 1, Allow alive survivor player suicides by using '!zs'.
l4d_afk_commands_suicide_allow "1"

// Players with these flags have access to use command to survivor team. (Empty = Everyone, -1: Nobody)
l4d_afk_commands_survivor_access_flag ""

// If 1, Block player from using 'go_away_from_keyboard' command in console. (This also blocks player from going idle with 'esc->take a break')
l4d_afk_commands_takeabreak_block "1"

// If 1, Block player from using 'sb_takecontrol' command in console.
l4d_afk_commands_takecontrol_block "1"

// Cold Down Time in seconds a player can not change team after he throws molotov, pipe bomb or boomer juice. (0=off).
l4d_afk_commands_throwable_cooltime_block "10.0"

// If 1, Player can not change team when he startle witch or being attacked by witch.
l4d_afk_commands_witch_attack_block "1"

// Players with these flags have access to use command to be an observer. (Empty = Everyone, -1: Nobody)
l4d_afk_commands_observer_access_flag "z"

-Command-
**Change team to Spectate
	"sm_afk"
	"sm_s"
	"sm_away"
	"sm_idle"
	"sm_spectate"
	"sm_spec"
	"sm_spectators"
	"sm_joinspectators"
	"sm_joinspectator"
	"sm_jointeam1"
	"sm_js"
	
**Change team to Survivor
	"sm_join"
	"sm_bot"
	"sm_jointeam"
	"sm_survivors"
	"sm_survivor"
	"sm_sur"
	"sm_joinsurvivors"
	"sm_joinsurvivor"
	"sm_jointeam2"
	"sm_jg"
	"sm_takebot"
	"sm_takeover"
	
**Change team to Infected
	"sm_infected"
	"sm_inf"
	"sm_joininfected"
	"sm_joininfecteds"
	"sm_jointeam3"
	"sm_zombie"
	
**Switch team to fully an observer
	"sm_observer"
	"sm_ob"
	"sm_observe"
	
**Survivor Player Suicides
	"sm_zs"
	
**Adm force player to change team (ADMFLAG_BAN)
	"sm_swapto", "sm_swapto <player1> [player2] ... [playerN] <teamnum> - swap all listed players to <teamnum> (1,2, or 3)"
