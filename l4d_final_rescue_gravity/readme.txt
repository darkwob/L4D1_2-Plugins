Set client gravity after final rescue starts just for fun.

-Changelog-
v1.6
AlliedModders Post: https://forums.alliedmods.net/showthread.php?p=2711374

-ConVar-
// 0=Plugin off, 1=Plugin on.
l4d_final_rescue_gravity_allow "1"

// If 1, change all clients' gravity to normal when finale vehicle is coming.
l4d_final_rescue_gravity_escape_ready_off "1"

// (L4D2)Which zombie class can also obtain the gravity, 0=None, 1=Smoker, =Boomer, 4=Hunter, 8=Spitter, 16=Jockey, 32=Charger, 64=Tank. Add numbers together.
l4d_final_rescue_gravity_infected_class "127"

// (L4D1)Which zombie class can also obtain the gravity, 0=None, 1=Smoker, 2=Boomer, 4=Hunter, 8=Tank. Add numbers together.
l4d_final_rescue_gravity_infected_class "15"

// Turn off the plugin in these maps, separate by commas (no spaces). (Empty = none).
l4d_final_rescue_gravity_map_off "c5m5_bridge;c13m4_cutthroatcreek"

// Turn on the plugin in these game modes, separate by commas (no spaces). (Empty = all).
l4d_final_rescue_gravity_modes ""

// Turn off the plugin in these game modes, separate by commas (no spaces). (Empty = none).
l4d_final_rescue_gravity_modes_off ""

// Turn on the plugin in these game modes. 0=All, 1=Coop, 2=Survival, 4=Versus, 8=Scavenge. Add numbers together.
l4d_final_rescue_gravity_modes_tog "0"

// Set Gravity value. (1.0=Normal, >1.0=High, <1.0=Low)
l4d_final_rescue_gravity_value "0.25"

// Interval (in sec.) to set gravity for client
l4d_final_rescue_gravity_interval "2"



