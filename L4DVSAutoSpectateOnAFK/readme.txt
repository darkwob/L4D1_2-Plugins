Forces survivors and infected to spectate if they're AFK after certain time

-ChangeLog-
v2.2
- Remake Code
- Add more hints
- Fixed wrong timer
- Translation Support

v1.3.1
-original plugin from djromero: https://forums.alliedmods.net/showthread.php?p=761203

-Require-
1. left4dhooks: https://forums.alliedmods.net/showthread.php?p=2684862

-Convar-
cfg\sourcemod\L4DVSAutoSpectateOnAFK.cfg
// Check/warn time interval
l4d_specafk_checkinteral "1"

// Players with these flags have immune to be kicked while spec. (Empty = Everyone, -1: Nobody)
l4d_specafk_immune_access_flag "z"

// If 1, kick enabled on afk while on spec
l4d_specafk_kickenabled "1"

// time before kick (while already on spec after warn)
l4d_specafk_kicktime "30"

// If 1, player will still be forced to spectate and kicked whether surviros leave saferoom or not.
l4d_specafk_saferoom_ignore "0"

// time before spec (after warn)
l4d_specafk_spectime "15"

// Warn time before kick (while already on spec)
l4d_specafk_warnkicktime "60"

// Warn time before spec
l4d_specafk_warnspectime "20"
