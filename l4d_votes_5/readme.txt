L4D1/2 Vote Menu (Change map、Kick、Restart、Give HP、Alltalk)

-Image-
see l4d_votes_5.jpg

-ChangeLog-
v5.9
-Changes to fix warnings when compiling on SourceMod 1.11.
 
-ConVar-
cfg\sourcemod\l4d_votes_5.cfg
// 0=Off, 1=On this plugin
l4d_Votens "1"

// If 1, Enable All Talk Off Vote.
l4d_Votensalltalk2ED "1"

// If 1, Enable All Talk On Vote.
l4d_VotensalltalkED "1"

// If 1, Enable Give HP Vote.
l4d_VotenshpED "1"

// If 1, Enable Change Custom Map Vote.
l4d_Votensmap2ED "1"

// If 1, Enable Change Value Map Vote.
l4d_VotensmapED "1"

// If 1, Enable Restart Current Map Vote.
l4d_VotensrestartmapED "1"

// If 1, Enable ForceSpectate Player Vote.
l4d_VotesForceSpectateED "1"

// If 1, Enable Kick Player Vote.
l4d_VotesKickED "1"

// Players with these flags have kick immune. (Empty = Everyone, -1: Nobody)
l4d_VotesKick_immue_access_flag "z"

// Minimum # of players in game to start the vote
sm_vote_player_limit "2"

// pass vote percentage.
sm_votes_s "0.60"

-Command-
"sm_votes", "Open Vote Menu"
"sm_callvote", "open vote meun"
"sm_callvotes", "open vote meun"
(Adm only)"sm_restartmap", "Restart current level"
