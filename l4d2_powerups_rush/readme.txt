When a client pops an adrenaline (or pills), various actions are perform faster (reload, melee swings, firing rates)

-ChangeLog-
AlliedModders post: https://forums.alliedmods.net/showpost.php?p=2748223&postcount=15
v2.2.1
-Remke code
-Fixed error
-Fixed Memory leak
-Powerup returning to normal when player changes team or dies
-Adrenaline makes you react faster to knockdowns and staggers (Combine with [L4D2]Adrenaline_Recovery: https://forums.alliedmods.net/showthread.php?p=2606439)
-Message display type (chat or hint box or center text)
-(L4D2)Set adrenaline effect time longer then default 15s

v2.0.1
-original plugin from Dusty1029: https://forums.alliedmods.net/showthread.php?t=127513

-Require-
1. left4dhooks: https://forums.alliedmods.net/showthread.php?p=2684862

-Related Plugin: 
Killing Adrenaline by NoroHime: https://forums.alliedmods.net/showthread.php?p=2770300

-Convar-
cfg/sourcemod/l4d2_powerups_rush.cfg
// (L4D2) If 1, set adrenaline effect time same as l4d_powerups_duration (Progress bar faster, such as use kits faster, save teammates faster... etc)
l4d_powerups_add_adrenaline_effect "1"

// If 1, players will be given adrenaline when leaving saferoom? (0 = OFF)
l4d_powerups_adren_give_on "0"

// (1.0 = Minspeed(Default speed) 2.0 = 2x speed of recovery
l4d_powerups_animspeed "2.0"

// How are players notified when connecting to server about the powerups? (0: Disable, 1:In chat, 2: In Hint Box, 3: Chat/Hint Both)
l4d_powerups_broadcast_type "1"

// Changes how countdown timer hint display. (0: Disable, 1:In chat, 2: In Hint Box, 3: In center text)
l4d_powerups_coutdown_type "2"

// How long should the duration of the boosts last?
l4d_powerups_duration "20"

// Changes how activation hint and deactivation hint display. (0: Disable, 1:In chat, 2: In Hint Box, 3: In center text)
l4d_powerups_notify_type "1"

// If 1, players will be given pills when leaving saferoom? (0 = OFF)
l4d_powerups_pills_give_on "0"

// The luckey change for pills that will grant the boost. (1 = 1/1  2 = 1/2  3 = 1/3  4 = 1/4  etc.)
l4d_powerups_pills_luck "3"

// If 1, enable this plugin ? (0 = Disable)
l4d_powerups_plugin_on "1"

// If 1, players will be given either adrenaline or pills when leaving saferoom? (0 = OFF)
l4d_powerups_random_give_on "0"

// The interval between bullets fired is multiplied by this value. WARNING: a short enough interval will make SMGs' and rifles' firing accuracy distorted (clamped between 0.02 ~ 0.9)
l4d_powerups_weaponfiring_rate "0.7"

// The interval for swinging melee weapon (clamped between 0.3 ~ 0.9)
l4d_powerups_weaponmelee_rate "0.45"

// The interval incurred by reloading is multiplied by this value (clamped between 0.2 ~ 0.9)
l4d_powerups_weaponreload_rate "0.5714"

-Command-
**Adm gives Adrenaline to all Survivors. (ADMFLAG_CHEATS)
sm_giveadren

**Adm gives Pills to all Survivors. (ADMFLAG_CHEATS)
sm_givepills

**Adm gives Random item (Adrenaline or Pills) to all Survivors. (ADMFLAG_CHEATS)
sm_giverandom

