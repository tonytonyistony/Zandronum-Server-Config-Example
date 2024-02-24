# Doom-Zandronum-Server-Setup
```

// ███████╗███████╗██████╗ ██╗   ██╗███████╗██████╗     ██╗   ██╗ █████╗ ██████╗ ██╗ █████╗ ██████╗ ██╗     ███████╗███████╗
// ██╔════╝██╔════╝██╔══██╗██║   ██║██╔════╝██╔══██╗    ██║   ██║██╔══██╗██╔══██╗██║██╔══██╗██╔══██╗██║     ██╔════╝██╔════╝
// ███████╗█████╗  ██████╔╝██║   ██║█████╗  ██████╔╝    ██║   ██║███████║██████╔╝██║███████║██████╔╝██║     █████╗  ███████╗
// ╚════██║██╔══╝  ██╔══██╗╚██╗ ██╔╝██╔══╝  ██╔══██╗    ╚██╗ ██╔╝██╔══██║██╔══██╗██║██╔══██║██╔══██╗██║     ██╔══╝  ╚════██║
// ███████║███████╗██║  ██║ ╚████╔╝ ███████╗██║  ██║     ╚████╔╝ ██║  ██║██║  ██║██║██║  ██║██████╔╝███████╗███████╗███████║
// ╚══════╝╚══════╝╚═╝  ╚═╝  ╚═══╝  ╚══════╝╚═╝  ╚═╝      ╚═══╝  ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝╚═╝  ╚═╝╚═════╝ ╚══════╝╚══════╝╚══════╝

// Admin List
// The admin list contains a list of IPs who are considered to be administrators on the
// server. Administrators can bypass the sv_maxclients limit and connect to the server
// even when its full (up to the maximum of 64). Additionally, these administrators cannot be issued votekicks on.
//sv_adminlistfile "adminlist.txt"

// AFK Rules
// If set, inactive (AFK) players will be forced to spectators after the specified number of minutes.
// 0 = Disabled by default
//sv_afk2spec 1

// Air Movement
// Defines the control a player has over his direction while in the air.
// See https://wiki.zandronum.com/Air_Control for how this is affected by the Compat_Limited_AirMovement flag.
// 0.00390625 Default
//sv_aircontrol 0.00390625

// BanFromGame ACS function. - https://wiki.zandronum.com/BanFromGame
// (development version 3.2-alpha and above only) Allows mods to ban players using the BanFromGame ACS function.
//sv_allowacsbanfunction false

// Private Messages
// Determines if clients are allowed to send private messages to each other or the host of the server.
// 0 = Disabled, 1 = Allow all (default), 2 = Allow Team Only
//sv_allowprivatechat 2

// Voice Chat
// (development version 3.2-alpha and above only) Controls whether voice chat is enabled.
// 0 = Disabled, 1 = Allow All (default), 2 = Allow Team Only, 3 = Players and spectators chat separately.
//sv_allowvoicechat 0

// (development version 3.2-alpha and above only) Enables proximity-based voice chat.
// False is default
//sv_proximityvoicechat true

// (development version 3.2-alpha and above only) Controls the distance at which proximity voice chat is no longer audible.
// 200 is default
//sv_maxproximityrolloffdist 150

// (development version 3.2-alpha and above only) Controls the distance at which proximity voice chat will begin rolling off (becoming quieter).
// 200 is default
//sv_minproximityrolloffdist 150

// Terminator or Hellstone Mover Timer (seconds)
// Determines the amount of time the Terminator sphere or the Hellstone remains dropped before it is moved to a random map spot.
// 0 = Disabled, 30 is default
//sv_artifactreturntime 0

// Whitelist Mode
// Defines a whitelist, a list of IPs exempt from bans, this allows server admins to let innocent people caught within range ban enter the server.
//sv_banexemptionfile "whitelist.txt"

// Blacklist Mode
// Defines a blacklist, a list of banned IPs unwanted on the server. Anyone, whose IP is on this list, may not connect unless they are also on the whitelist.
// sv_banfile "banlist.txt"

// Banlist Memory Reparse
// If set, the banlist, as well as the whitelist and the adminlist, are automatically reparsed from their files into memory every this many seconds.
// 0 is default. Files are only reparsed at server startup or manually. Useful for multi-server clusters.
//sv_banlistreparsetime 30

// Broadcast to LAN
// Whether the server will broadcast to the local area network.
// True by default
//sv_broadcast false

// Allow Cheats
// Whether clients can use cheat commands on the server. Use with care! This CVar is not saved to the configuration and will be reset upon restarting the server.
// Disable by default
//sv_cheats true

// Message Colors
// Whether color codes are stripped in the server console. This does not affect chat messages sent to other clients.
// 0 = Removes colors (default), 1 = Allow, 2 = Leaves the \c<x> format in messages.
//sv_colorstripmethod 1

// Coop Damage Multiplier
// Damage multiplier applied to all damage players recieve from monsters.dealt to players by monsters with this value.
// 1.0 is default
//sv_coop_damagefactor 1.25

// Coop Voodoo Dolls - https://doomwiki.org/wiki/Voodoo_doll
// Whether Voodoo dolls are supported online.
// True by default
//sv_coopspawnvoodoodolls false

// Coop Unassign Voodoo Dolls
// When set, all voodoo dolls are spawned when the map is loaded, no matter if the corresponding player is in the server or not. Furthermore, the dolls are not assigned to any player in this mode.
// Because of this they dont receive any damage and cant pick up any items, but this approach is more resistant to problems caused by ingame joining / leaving.
// True by default
//sv_coopunassignedvoodoodolls false

// Coop Voodoo Doll Count
// Controls how many players does the voodoo doll cater for. Unassigned dolls are spawned for players 1 to N, where N is the value of this CVar.
// Dolls for players with a player number bigger than N are not spawned.
// 64 is default
//sv_coopunassignedvoodoodollsfornplayers 32

// Server Country Location - https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3#Officially_assigned_code_elements
// Sets the country of the server, which will be presented to server browsers. Note that not all servers browsers support this feature and will use IP geolocation instead.
// "automatic" default
//sv_country "USA"

// Default DMFlags
// When true, the server will automatically set certain dmflags for certain game modes.
// For deathmatch and team games (CTF, skulltag, one-flag CTF, etc), these flags are: weapons stay, items respawn, no monsters, no crouching, double ammo.
// In cooperative, these flags are cleared.
// For duel, these are exactly the same as the deathmatch ones with the addition of players spawning furthest from other players.
// True is default
//sv_defaultdmflags false

// Autohealth Options
// Certain items for Heretic, Hexen and Strife have the ability to auto-trigger when the players health drops below a certain percentage.
// Setting this CVAR to true will disable that behavior.
// False is default
//sv_disableautohealth true

// Spying Permissions
// When false, this allows clients to spy on other players, even if they would be allowed to do so otherwise. This CVar is a flag on dmflags2.
// False is default
//sv_disallowspying true

// Suicide Permissions
// Players may not kill themselves with the Z kill command. This is a flag on dmflags2.
// False is default
//sv_disallowsuicide true

// Players may not Z kill themselves.
// False is default
//sv_nokill true

// Monster Item Drop Settings
// Controls how items from monsters are dropped on the floor; whether in Doom or in Strife style. The Strife style generally tosses dropped items farther away.
// 0 = Game Vanilla (default), 1 = Standard Style, 2 = Strife Style
//sv_dropstyle 2

// Dual Countdown Timer
// How many seconds the warm up lasts before a duel starts.
// 10 seconds is default
//sv_duelcountdowntime 20

// Enforce Banlist
// Whether the banlist is actually enforced or not.
// True is default
//sv_enforcebans false

// Enforce Master Banlist
// Whether the server enforces the master servers banlist. Servers may opt out of the master banlist enforcement by setting this to false, though such servers will not be broadcasted on the master.
// True is default
//sv_enforcemasterbanlist false

// Fast Weapon Settings
// How fast weapons fire.
// 0 - Game Vanilla (default), 1 = 1 Z tic per weapon frame, 2 = 1 tic per frame, frames without codepointers are skipped. (that is quite fast)
//sv_fastweapons 1

// Gravity Settings
// How strong gravity is present in the game world. Higher values creates stronger gravity, lesser values create lighter gravity.
// 800 is default
//sv_gravity 700

// Prevent Player Item Drops
// If set, clients may not  drop items. Items may never be dropped in duels.
// False is default
//sv_nodrop true

// CTF Return Timer
// How long will a flag or skull remain on the ground when dropped before it is automatically returned back to its original position.
// 15 seconds is default
//sv_flagreturntime 30

// Server Password Settings. False by default
// Whether clients must supply a join password in order to join the game. Clients without the proper join password may still spectate freely.
//sv_forcejoinpassword true
//sv_joinpassword "changeme"

// Whether clients must supply the correct password in order to connect to the server.
// Unlike the join password, clients cannot enter the server at all without the correct password, enforcing stricter privacy.
//sv_forcepassword true
//sv_password "changeme"

// Display Email Address
// This CVar allows the ability for the clients to send an e-mail to the administrator of the server.
// Empty field is default
//sv_hostemail "test@test.com"

// MOTD
// Sets a message of the day on the server, a welcome message printed on clients upon connection. Generally used to display rules and/or admin contact information.
// Empty field is default
//sv_motd "Thanks for joining my Zandronum server"

// Website Info
// Sets a website which defines a website for this server. Launchers will use this field as the primary download location for any PWADs they do not have.
// However, this only works if the website features direct download links for WADs
// upload services such as SpeedyShare and FileFront do not and the clients must manually download the required files from them.
// Empty field is default
//sv_website ""

// Server Name
// A given name for the server. This is the display name the server has on the master server list.
// For server admins who host multiple server, you will want to set this flag in your server executable/script. Example: +sv_hostname "Unnamed Zandronum server"
// This allows for making a more generalized server config for common games server. You then call this config file in your script. Example: +exec this_config.cfg
//sv_hostname "Unnamed Zandronum server"

// Invasion Countdown
// How many seconds of warm-up time before the invasion game starts and when the next wave begins.
// 10 is default
//sv_invasioncountdowntime 5

// Invasion Wave Limit
// If set, the wave limit set in a map definition takes precedence over the wavelimit CVar.
// True is default
//sv_usemapsettingswavelimit false

// Monster Kill Requirements
// How much of the monsters have to be killed before the level can be exited. This is a percentage value. DMFlags2 sv_killallmonsters 131072 has to be set for this to be actually enforced.
// 100% is default
//sv_killallmonsters_percentage 99

// Client Command Settings
// Enables/Disables the client commands flooding protection and prevents clients from Repeatedly using Commands over and over again.
// Setting this to false will disable all restrictions on commands and new commands may be used right after the previous ones.
// True is the default
//sv_limitcommands false

// Last Man Standing Warmup
// How many seconds of warm-up time before a new LMS match starts.
// 10 is default
// sv_lmscountdowntime 15

// Log File Settings
// Append: If a logfile with the exact same name is present, the server will merely add into the log file without over writing the previous logfile.
// False is default
//sv_logfile_append true

// Name Timestamp: When generating a new log file, the server will append the time and date to the end of the logfile name.
// True is default
//sv_logfilenametimestamp false

// Entry Timestamp: The server logfile is written containing time stamps at every new line. This does not affect the server console.
// True is default
//sv_logfiletimestamp false

// Entry Timestamp+Date: The current date will be prepended to the per-line timestamp of the logfile in the format of "YY:MM:DD".
// False is default
//sv_logfiletimestamp_usedate true

// Measure Bandwidth
// Measures how much bandwidth is used for both ACS scripts and actor classes. The console command dumptrafficmeasure prints the results.
// This is useful mostly for mod developers for identifying and debugging bandwidth hogs. See https://wiki.zandronum.com/Measuring_outbound_traffic for a tutorial.
// False by default
//sv_measureoutboundtraffic true

// Map Rotation
// The server will use a map rotation list to determine the campaign instead of any other method. The server will advance go to any other map that was not specified in the list.
// True by default
//sv_maprotation false

// Mark Chat Lines
// All chat messages within the server console contain a CHAT tag before the typed message from the clients.
// This can be very useful for reading the logfiles or for making bots that parse chat messages.
// False by default
//sv_markchatlines true

// Max Players
// The server only allows this many clients to connect to the server. If the server is full, any new clients will not be able to connect.
// Note: in older versions, the maximum supported amount of players was 32 and was increased to 64 in the 1.0 release.
// Since older mods may assume the limit to remain 32, the default remains 32.
//sv_maxclients 64

// This many players can join the game, the rest are forced to spectate. Compare sv_maxclients. The same logic for the default also applies.
// 32 is default
//sv_maxplayers 64

// Max Players per IP
// How many players with the same IP can enter the server.
// 2 is default
//sv_maxclientsperip 4

// Max UDP Packet Size
// How much data, in bytes, can be stored in an UDP packet. If packet size is small while network usage is high, this can cause the server to overload during transmissions of the small packets.
// However, if the packet size is too large, newly connecting clients may not be able to process the packets quickly enough.
// 1024 is default
//sv_maxpacketsize 2048

// Max Teams
// Maximum amount of teams allowed. This CVar can be increased to allow 3 or 4 team matches. However, this only works if the map supports as many teams as desired.
// 2 is default
//sv_maxteams 3

// Team Start Location
// If set, team starts will be used as possible deatmatch starts in deathmatch gamemodes with teams. (TDM, TLMS)
// False is default
//sv_useteamstartsindm true

// Minimize to Tray
// The server console window will be minimized and hidden into the system tray. (Windows only)
// True is default
//sv_minimizetosystray false

// ╔═════════════════╗
// ║ VOTING SETTINGS ║
// ╚═════════════════╝

// Minimum Voters
// How many players are needed in the server in order to call a vote.
// 1 is default
//sv_minvoters 2

// Votes Cooldown
// Sets the cooldown between votes, in minutes. This stops players from flooding the server with votes.
// If set to 0, the cooldown is disabled and a vote may be called immediately after a prior one.
// 5 is default
//sv_votecooldown 1

// This CVar allows to manage how votes take place.
// 0 = Voting Enabled (default), 1 = Voting disabled. 2 = Players only can vote.
//sv_nocallvote 2

// Disables all Z changemap votes. However, map votes may still be called unless sv_nomapvote is set.
// False is default
//sv_nochangemapvote true

// Disables all votes to change the duel limit.
// False is default
// sv_noduellimitvote true

// Disables all DMFlag votes.
// True is default
//sv_noflagvote false

// Disables all votes to force players to Spec by voting.
// False is default
//sv_noforcespecvote true

// Disables all votes to change the frag limit.
// False is default
//sv_nofraglimitvote true

// Disables all votes to kick players.
// False is default
//sv_nokickvote true

// Disables all Z map votes. However, changemap votes may still be called unless sv_nochangemapvote is set.
// False is default
//sv_nomapvote true

// Disables all Z nextmap votes. However, nextsecret votes may still be called unless sv_nonextsecretvote is set.
// False is default
//sv_nonextmapvote true

// Disables all Z nextsecret votes.
// False is default
//sv_nonextsecretvote true

// Disables all votes to change the point limit.
// False is default
//sv_nopointlimitvote true

// Disables all votes to change the time limit.
// False is default
//sv_notimelimitvote true

// Disables all votes to change the LMS win limit.
// False is default
//sv_nowinlimitvote true

// If set, the hold time set in a map definition takes precedence over sv_possessionholdtime, if unset, the server CVar has the last word.
// True is default
//sv_usemapsettingspossessionholdtime false

// WAD Authentication
// If set, the server uses an authentication mechanism to ensure clients have the correct WADs.
// Even without this CVar set, the map is always verified. A server host should have no reason to disable this CVar aside of LAN play or testing.
// True is default
//sv_pure false

// Master Server Query Timer
// Server browsers query the servers on the master list for information such as ping, players, game settings, WADs used, etc.
// This CVar defines a flood throttle for this - a launcher client may not query the server again for this many seconds. This can help prevent DDoS attacks.
// 10 is default
//sv_queryignoretime 15

// Random Coop Starting Points
// If true, in cooperative game modes players are spawned at random player starts instead of the one designated for them.
// False is default
//sv_randomcoopstarts true

// Random Map Reotation
// If set, the server will randomize the map rotation list instead of advancing through maps in sequence. Only meaningful if sv_maprotation is set too.
// False is default
//sv_randommaprotation true

// Respawn Delay Timer
// How long a player must wait (in seconds) after dying before they can respawn. This doesnt apply to players who are spawn telefragged.
// 1 is default
//sv_respawndelaytime 2

// Show Server Queries
// If set, this CVar will display the IPs of clients quering the server. These clients are not joining the game, this is the server browser quering the servers for information.
// This CVar can be useful for debugging whether the server is on the master and whether clients can connect to it.
// False is default
//sv_showlauncherqueries true

// Show Warning Messages
// If set to true, some certain warning messages are shown. May cause flooding the log for certain mods and should only be used for debugging purposes.
// False is default
//sv_showwarnings true

// Show Console Timestamps
// When true, the server console will contain a timestamp for all messages within the server console.
// False is default
//sv_timestamp true

// Timestamp Format Settings
// Formatting option for sv_timestamp:
// 0 = HOURS:MINUTES:SECONDS (24 Hour Format) (default)
// 1 = HOURS:MINUTES:SECONDS AM/PM
// 2 = HOURS:MINUTES:SECONDS am/pm
// 3 = HOURS:MINUTES (24 Hour Format)
// 4 = HOURS:MINUTES AM/PM
// 5 = HOURS:MINUTES am/pm
//sv_timestampformat 1

// Smart Aiming
// This value will affect the behaviour of auto-aiming
// 0 = Autoaim will always target the nearest shootable thing. (default)
// 1 = Tries to avoid shooting at allies and non-monster things.
// 2 = Auto-aim will never aim at friends.
// 3 = Auto-aim will only aim at a hostile monster
//sv_smartaim 1

// Smooth Players
// If non-zero, enables the skip correction which tries to smooth the movement of players who are lagging on the servers end through extrapolation.
// The value represents the number of tics the server will try extrapolating a player, for up to 3 tics maximum.
// 0 is default
//sv_smoothplayers 1

// Sudden death
// When the time limit is hit and all teams have the same amount of score, this CVar causes sudden death to commence.
// The first team to score wins the game no matter what the pointlimit is set to.
// If unset, the game ends immediately once the timelimit hits and if teams have the same amount of score, the match is declared a draw.
// True is default
//sv_suddendeath false

// Survival Warp-up Timer
// Amount of warm-up in seconds in survival games.
// 10 is default
//sv_survivalcountdowntime 20

// Unlimited pickups
// When true, this allows players to pickup ammunition past maximum amounts.
// False is default
//sv_unlimited_pickup true

// Public Server?
// If set, the server will identify itself to the master server and is broadcasted in the server list. If this variable is false, the server will remain private.
// True is default
//sv_updatemaster false

// Tic Buffering
// Instead of processing all commands of a client immediately, they are stored in a "ticbuffer".
// During each server tic, the server processes up to two sets of commands in this buffer for each client.
// This limits players to only executing 2 tics worth of shooting and movement commands per each server tic. This limits how jittery laggy players will be.
// Because each clients own displayed position is predicted, under any reasonable internet conditions the way a client perceives his own movement will be the same whether this variable is on or off.
// For all stable releases this variable is forced on. For experimental builds it is changeable.
// True is default
//sv_useticbuffer false

//  ██████╗ ██████╗ ███╗   ██╗███████╗ ██████╗ ██╗     ███████╗    ██╗   ██╗ █████╗ ██████╗ ██╗ █████╗ ██████╗ ██╗     ███████╗███████╗
// ██╔════╝██╔═══██╗████╗  ██║██╔════╝██╔═══██╗██║     ██╔════╝    ██║   ██║██╔══██╗██╔══██╗██║██╔══██╗██╔══██╗██║     ██╔════╝██╔════╝
// ██║     ██║   ██║██╔██╗ ██║███████╗██║   ██║██║     █████╗      ██║   ██║███████║██████╔╝██║███████║██████╔╝██║     █████╗  ███████╗
// ██║     ██║   ██║██║╚██╗██║╚════██║██║   ██║██║     ██╔══╝      ╚██╗ ██╔╝██╔══██║██╔══██╗██║██╔══██║██╔══██╗██║     ██╔══╝  ╚════██║
// ╚██████╗╚██████╔╝██║ ╚████║███████║╚██████╔╝███████╗███████╗     ╚████╔╝ ██║  ██║██║  ██║██║██║  ██║██████╔╝███████╗███████╗███████║
//  ╚═════╝ ╚═════╝ ╚═╝  ╚═══╝╚══════╝ ╚═════╝ ╚══════╝╚══════╝      ╚═══╝  ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝╚═╝  ╚═╝╚═════╝ ╚══════╝╚══════╝╚══════╝

// AutoAim Settings - http://zdoom.org/wiki/Autoaim
// When the integer is greater than zero, this changes the precision of AutoAim.
// This feature that was also included in both Doom and Doom2, allows the players to use AutoAim for horizontal purposes.
// While before, the Doom engine did not allow players to view angles in a horizontal sense.
// As ZDoom does allow this behavior in the software renderer, but the software renderer does not allow the players to view at extreme angles as opposed to GZDooms OpenGL renderer.
// 0 = 0° (Never), .25 = .25° (Very Low), .5 = .5° (Low), 1 = 1° (Medium), 2 = 2° (High), 3 = 3° (Very High), 35-56 = 35°-56° (Always)
//autoaim 35

// Allow Bot Chat
// This CVar allows or disallows the bot from ever talking within the game.
//bot_allowchat true

// Bot Skill
// Changes the skill level of the Zandronum bots.
// 0 = Easiest, 1 = Easy, 2 = Average. 3 = Hard, 4 = Nightmare
//botskill 3

// Buckshot Mode
// This modifier restricts players to use only the Super Shotgun. Fast paced close combat is guaranteed.
//buckshot true

// Chat Sounds
// This CVar allows the client to change the sound when a new chat message is sent to all clients.
// 0 = Disabled, 1 = Default Sounds, 2 = Doom2 Sounds, 3 = Doom Sound
//chat_sound 2

// Color in Messages
// Allows the user to toggle if colors are processed in player names and chat messages.
// 0 = Disallow All, 1 = Allow All, 2 = Only allow colors from the clients name, but not the chat messages.
//con_colorinmessages 2

// Crash Log Settings
// When the value of adjusting how Zandronum automatically treats all crash reports.
// 0 = Crashdump files are not generated, 1 = Crash dialog window is displayed, 2 = Crashdump files are generated within a specific directory that is defined in the CrashLog_Dir
//crashlogs 2
//crashlog_dir "F:\Zandronum\CrashDump"

// Demo Compression
// Enable or disable demos from being compressed.
//demo_compress true

// Pure Demo
// Enable or disable demo authentication. With this enabled, protected lumps and maps will be checked to prevent demo playback with bad WADs.
// If demo authentication fails, the list of WADs the demo was recorded with is printed as a hint for the user.
//demo_pure true

// FOV Setting - https://zdoom.org/wiki/FOV
// Alter users FOV
// Default value is 90
//fov 90

// Master Server Hostname
// Sets the value for sending discoverable packets to the Zandronum Master Server.
// When the individual server or clusters of servers are publicly available to the Zandronum player base (whether official or another community),
// this sends a discovery packet to the server along with other information and notifies that the server(s) are available.
// Official Zandronum Master Server: master.zandronum.com
//masterhostname "master.zandronum.com"

// Max View Pitch
// Limits the maximum pitch of freelook. Can be used to limit OpenGL players freelook to the same as Software by setting MaxViewPitch to 56.
//maxviewpitch 90

// Draw Weapon Sprite
// When set to false, the players weapon that is displayed on HUD will be hidden and not rendered.
r_drawplayersprites true

// Spectating Message
// When the value is true, this will display a "Spectating - Press USE to join" message while spectating. However, when false, this message is not displayed.
//r_drawspectatingstring true

// Max Particles
// When the value is greater than zero, this allows and controls how many particles that can be displayed and rendered. If the integer is zero, no particles will be displayed and rendered.
// Default is 4000
r_maxparticles 10000

// ╔════════════════╗
// ║ CLIENT OPTIONS ║
// ╚════════════════╝

// Multiple Announcers
// When true, this will allow more than one announcement to be played. However, if false only one announcement will be played at a time.
//cl_allowmultipleannouncersounds true

// Allow Frag Announcements
// When true, the announcer will repeat how many frags are left in a competitive game mode. Such occasions for this settings being, both opponents are three frags before reaching the FragLimit.
// Additionally, if the winning player suicides or losses a frag during the game, the announced frags left will be stated again.
//cl_alwaysplayfragsleft true

// Backup Move/Weapons Commands
// Specifies how many backup copies of old move or weapon select commands (up to three) the client will send to the server per tic.
// This is useful if the client is suffering from noticeable packet loss, but due to the increased outbound net traffic, its recommended that it only be enabled in those cases.
//cl_backupcommands 0

// Cap FPS
// When true, the game is limited to 35 FPS, as it was originally in Doom. When false, the game frame rate will be as high as your machine is capable of.
// You can use this in conjunction with vid_vsync to control whether or not the maximum frame rate is restricted to your monitors refresh rate.
//cl_capfps false

// Dont Restore Frags
// When false, the clients frag count will be stored and used again when playing on the same server again after disconnecting from a server.
//cl_dontrestorefrags false

// Draw Coop Info
// When enabled, this will display the status of other players (health, armor, weapon, and ammo) in cooperative related game modes and team based game modes.
//cl_drawcoopinfo true

// Hit Scan Decal Hack
// When true, decals should properly display when the bullet puff impacts a wall.
//cl_hitscandecalhack true

// Icons On Heads - https://wiki.zandronum.com/Player_statuses
// When true, the player is able to see the icons over other players head, including the clients player.
//cl_icons true

// Names On Heads
// When false, the other players name will not be shown on the HUD. By default, this is set to true.
//cl_identifytarget true

// Medal Permission - https://wiki.zandronum.com/Skulltag_medals
// When true, the player can view own and other players medals if earned ingame.
//cl_medals true

// Old School Free-Look
// When false, this increases the Softwares freelook to +/-56 degrees and thus allowing the client to view at extreme angles that were never possible before.
//cl_oldfreelooklimit false

// Reset CVars After Leaving Server
// When true, any CVars that were modified by ConsoleCommand will be restored to their original values upon exiting the game.
// This is used to prevent mods from changing a users settings permanently, even maliciously. Note that manually changing a CVars value still archives the new value, as expected.
cl_protectcvars true

// Respawn with Fire Button
// When true, this will allow the players to respawn without having to press the spacebar or any binded key for +use.
//cl_respawnonfire true

// Show Commands from Server - Debugging
// Displays all of the commands that is coming from the server to the player.
//cl_showcommands true

// Fullscreen Voting
// This CVar allows the user to view further information regarding the called vote. When true, this will display who called the vote, what the vote effects, and the users that
// have casted their votes. However, when false, the called vote will only display what the vote effects, and how many players voted.
//cl_showfullscreenvote false

// Larger Frag Messaging
// When true and a player fragged an opponent, a large message will appear in the middle of the HUD stating that a player was fragged,
// but also displays if the client himself was fragged by another player. (e.i Tiger was fragged by Rivecoder!)
//cl_showlargefragmessages true

// Skins Settings
// Used to toggle certain skins or to disable skins. However, if the client does not have the SkullTag Fun Skin Pack, this CVar will not make any noticeable changes
// 0 = Disable all skins, but only display the normal Doom player skin.
// 1 = Allow all skins available.
// 2 = Disable cheat skins (Hissy, Doomcrate, Romero, and Daisy}
//cl_skins 2

// Window Active Sounds
// If enabled, the Windows client will keep playing sound as normal when the client is not the currently active application.
//cl_soundwhennotactive true

// Spectator Speedy
// Controls the speed of movement while spectating. Default is 1.
//cl_spectatormove 2

// Start Game as Spectator
// When true, forces the client to spectate the game before automatically joining ingame once connected to the server. When this CVar is false, the client is automatically forced to join in the game.
//cl_startasspectator true

// Zandronum HUD
// When true, this CVar will allow the use of the Zandronum HUD to be displayed. This HUD can display flag, skull, terminator, and who possess the Hell Stone information during the game play.
// However when the value false the standard Doom HUD will be used instead. This will only display the current health/ammor and ammunition for the selected weapon.
//cl_stfullscreenhud true

// Tick Settings
// This value is how many tics it takes the client to update the positions of other clients based on server data. In between server data updates, other client positions are extrapolated
// as traveling in their current directions at their current velocities. The lower the value, the higher bandwidth consumption will be.
// The values that can be used are limited to only 1 tic, 2 tics, and 3 tics.
// Time measured in tics; Doom tics 35 == 1 sec
// Default value is 3 tics
//cl_ticsperupdate 3

// Unlagged Settings
// When False, the clients own hitscan weapon hits will not use unlagged reconcilation, regardless of the servers Unlagged CVar.
//cl_unlagged true

// Weapons Cycle Settings.
// When true, this CVar will cycle through the clients weapons that are available in inventory while using the WeapNext and WeapPrev CCMD.
// However, when this is false, the client will scroll through a specified weapon order.
//cl_useoriginalweaponorder true

// ╔════════════╗
// ║ GL OPTIONS ║
// ╚════════════╝

// Sprite Billboard Mode
// This CVar controls how Sprites are rendered in the OpenGL environment.
// 0 = y axis billboard is only rendered. (PAPER THIN SPRITES!)
// 1 = x/y axis billboard is rendered.
gl_billboard_mode 1

// Interpolate Model Frames
// MD2/DMD/MD3 model frame interpolation
gl_interpolate_model_frames true

// Enable/Disable OpenGL
// Disables the OpenGL renderer and forces the Software renderer, but Zandronum must restart in order to make such changes.
//gl_nogl true

// Particle Style
// This CVar controls how particles are rendered in the OpenGL environment.
// 0 = Square, 1 = Round, 2 = Smooth
gl_particles_style 2

// OpenGL Texture Settings
// 0 = RGBA8, 1 = RGGB5_A1, 2 = RGBA4, 3 = RGBA2, 4 = COMPR_RGBA, 5 = S3TC_DXT1, 6 = S3TC_DXT3, 7 = S3TC_DXT5
gl_texture_format 1

// High Quality Resize Mode
// This controls how detailed the renderer is set by.
// 0 = None, 1 = Scale2x, 2 = Scale3x, 3 = Scale4x, 4 = HQ2x, 5 = HQ3x, 6 = HQ4x
gl_texture_hqresize 6

// Texture HQ Resize Max Input Size
// If the texture and/or sprite width or height exceeds the value of this CVar, then the texture or sprite will not be upsampled while using the Scale algorithm. [Default: 512]
//gl_texture_hqresize_maxinputsize 512

// Texture HQ Resize
// This specifies which should be rendered while using the Scale algorithm. [Default: 0]
// Upsample everything if plausible from the GL_Texture_HQResize_MaxInputSize CVar Sprites and Fonts only should be upsampled
//gl_texture_hqresize_target 0

// Use Models
// If true, this enables the use of 3D Models. All ACTORS will be replaced with available 3D Models. But if the ACTOR does not have a 3D Model, then it will remain using standard SPRITES.
gl_use_models true

// Video Compatibility
// This CVar reverts the OpenGL to version 1.1 to be the renderer. However, use this CVar if the graphics card is having difficulty with the current version (2.1).
// Some features will not be rendered within the map, for example, horizon lines.
//gl_vid_compatibility false

// Video Renderer
// Allows the user to toggle between video renderers of either OpenGL or Software mode.
// 0 = Software mode (Basic, limited, like Doom), 1 = OpenGL mode (eyecandy)
vid_renderer 1


//   ██████╗  █████╗ ███╗   ███╗███████╗    ███╗   ███╗ ██████╗ ██████╗ ███████╗███████╗
//  ██╔════╝ ██╔══██╗████╗ ████║██╔════╝    ████╗ ████║██╔═══██╗██╔══██╗██╔════╝██╔════╝
//  ██║  ███╗███████║██╔████╔██║█████╗      ██╔████╔██║██║   ██║██║  ██║█████╗  ███████╗
//  ██║   ██║██╔══██║██║╚██╔╝██║██╔══╝      ██║╚██╔╝██║██║   ██║██║  ██║██╔══╝  ╚════██║
//  ╚██████╔╝██║  ██║██║ ╚═╝ ██║███████╗    ██║ ╚═╝ ██║╚██████╔╝██████╔╝███████╗███████║
//   ╚═════╝ ╚═╝  ╚═╝╚═╝     ╚═╝╚══════╝    ╚═╝     ╚═╝ ╚═════╝ ╚═════╝ ╚══════╝╚══════╝

// ╔════════════════════════════╗
// ║ COMPETITIVE GAME MODIFIERS ║
// ╚════════════════════════════╝

// Buckshot Mode
// This modifier restricts players to use only the Super Shotgun. Fast paced close combat is guaranteed.
//buckshot true

// InstaGib Mode
// A modifier that causes everyone to spawn with a railgun, with no other items spawning.
// The railgun is powerful enough that in one hit, it will instantly kill you with so much damage that youre gibbed (hence "instagib".)
//instagib true

// ╔═══════════════════════════╗
// ║ GLOBAL GAME MODE SETTINGS ║
// ╠═══════════════════════════╝═════════════════════════════╗
// ║ More game setting are at the bottom of this config file ║
// ╚═════════════════════════════════════════════════════════╝

// Handicap Settings
// When used, the players health will be decreased to the new value specified when spawned.
// For example, if the players handicap is set to 20, then the players health when spawned will be set as 80.
// Expression: 100-20=80
//handicap 20

// Switch Weapons on Pickup
// When toggled, the player can either never automatically switch weapons on pickup, switch if the weapon is higher ranked, or always switch.
// 0 = Never, 1 = Only Higher Ranked, 2 = Always
//switchonpickup 0

// Friendly Fire Settings
// Sets the team damage (friendly fire) factor between players within the same team or allies in cooperative.
// 0.00 means friendly fire disabled, 1.00 means full team damage, 0.50 is half damage etc.
//teamdamage 0.00

// Turbo Settings
// Sets the speed of the player. If less than a hundred the player will move slow, but if the value is greater than a hundred the player will move fast.
// The standard value is 100.
//turbo 100

// Frag Limit - Applies to Deathmatch, Terminator and Duel
// When the value is greater than zero, players in a Deathmatch related game mode must reach the FragLimit quota.
// When the FragLimit has been reached, players are advanced to the next map. However, if the Duel CVar is true, players can only advance to the next match once the DuelLimit has been reached.
//fraglimit 50

// Time Limit - Applies to Deathmatch, Terminator, Possession, LMS, CTF, Skulltag, Duel and Domination
// When set, the players within the game have a certain amount of minutes to complete the game. This CVar works mainly for competitive game modes, omitting cooperative game modes.
//timelimit 5

// Points Limit - Applies to Possession, CTF, Skulltag and Domination
// This sets how many points are needed in order to win the game. This CVar is mainly used for CTF and SkullTag game modes.
//pointlimit 5

// Max Lives - Applies to LMS, Survival and Invasion Lives
// In LMS, survival, and invasion the default value of 0 is intepreted as one life.
// In invasion, setting this variable above 0 will cause the game to become survival invasion, setting it to 0 results in normal invasion with unlimited lives.
// 0 is default
//sv_maxlives 2

// ╔═══════════════════╗
// ║ COMPETITIVE MODES ║
// ╚═══════════════════╝

// ╔═══════════════════════════════╗
// ║ DEATHMATCH OR TEAM DEATHMATCH ║
// ╚═══════════════════════════════╝
// The classic game mode: simply shoot as many players as you see. The game ends when a player hits the frag limit, or the time limit is reached.
// Check global game mode settings for additional settings.
// Choose only one.
//deathmatch true
//teamplay true

// ╔════════════╗
// ║ TERMINATOR ║
// ╚════════════╝
// In the Terminator game mode, the Terminator sphere is spawned in a random spot.
// Once a player has picked up the sphere, that player will become the Terminator, and will have 200% health, 200% armour, and permanent quad damage!
// The Terminator can easily be identified by the Terminator icon atop the players head.
// When the Terminator is killed, the player that killed the Terminator will gain 10 frags, and the Terminator sphere is dropped, ready to be picked up again.
// Check global game mode settings for additional settings.
//terminator true

// ╔═══════════════════════════════╗
// ║ POSSESSION OR TEAM POSSESSION ║
// ╚═══════════════════════════════╝
// In Possession, the Hellstone will spawn at a random location. When a player picks up the Hellstone, they must stay alive for a certain amount of time in order to gain a point.
// However, the player with the Hellstone will lose all of their weapons, rendering them defenceless! The Hellstone will be dropped if the player holding it dies, allowing it to be picked up again.
// Choose only one.
//possession true
//teampossession true

// Possession Match Cooldown
// How many seconds of warm-up time before a new possession match starts.
// 10 is default
//sv_possessioncountdowntime 15

// Possession Hold Timers
// How long a player must hold the Hellstone before scoring. The time is measured by seconds.
// Check global game mode settings for additional settings.
// 30 is default
//sv_possessionholdtime 25

// ╔═══════════════════════════════════════════════════╗
// ║ LAST MAN STANDING (LMS) OR TEAM LAST MAN STANDING ║
// ╚═══════════════════════════════════════════════════╝
// In Possession, the Hellstone will spawn at a random location. When a player picks up the Hellstone, they must stay alive for a certain amount of time in order to gain a point.
// However, the player with the Hellstone will lose all of their weapons, rendering them defenceless! The Hellstone will be dropped if the player holding it dies, allowing it to be picked up again.
// Choose only one.
//lastmanstanding true
//teamlms true

// LMS Win Limit
// When a value is greater than zero, players or teams in the Last Man Standing game mode will have a certain amount of wins to accomplish before advancing into the next map.
// However, if the integer is zero, the map will never change.
// Check global game mode settings for additional settings.
//winlimit 5

// LMS Allowed Weapons - https://wiki.zandronum.com/LMSFlags
// Allows the use to toggle what weapons are available in the Last Man Standing game mode. This CVar uses values from other LMSFlags.
// Each weapon you want to allow, you add the values together. Example: Pistol = 1, Shotgun = 2, 1 + 2 = lmsallowedweapons 3
// 1 = Pistol, 2 = Shotgun, 4 = SSG, 8 = Chaingun, 16 = Minigun, 32 = Rocket Launcher, 64 = Grenade Launcher, 128 = Plasma Gun, 256 = Railgun, 512 = Chainsaw
//lmsallowedweapons 1023

// LMS Spectator Settings
// Add values together. like above.
// 1 = Allows spectators to chat with other players that are still alive.
// 2 = Allows spectators to view and spy on other players that are still alive.
//lmsspectatorsettings 3

// ╔════════════════════════════════════════╗
// ║ CAPTURE THE FLAG (CTF) OR ONE-FLAG CTF ║
// ╚════════════════════════════════════════╝
// In Capture The Flag (CTF), you and your team must pick up the flag from the other teams base, and carry the flag back to your teams flag to gain a point.
// Not only that, but yu still have to defend your teams flag, and make sure that your flag carrier safely scores a point for the team.
// If the carrier dies while holding the flag, the flag will be dropped allowing enemies to pick it up and allies to return it back to base.
// Check global game mode settings for additional settings.
//ctf true
//oneflagctf true

// ╔══════════╗
// ║ SKULLTAG ║
// ╚══════════╝
// Skulltag (ST) is a game mode similar to CTF. Unlike CTF, however, skulls are used instead of flags, and these skulls must be placed (tagged) on your temas score pillar located
// somewhere on the map. Some maps may even have multiple pillars, and each pillar may be worth different amounts of points.
// Check global game mode settings for additional settings.
//skulltag true

// ╔══════════╗
// ║   DUEL   ║
// ╚══════════╝
// Duel is effectively one-on-one Deathmatch. Two players fight against each other, while other players wait in line to play the winner.
// To win in a duel game, you must frag the other player until you reach the frag limit.
//duel true

// Duel Map Round Limit
// When set to a value greater than zero, the server will go to the next map after the duel limit quota has been reached.
// Check global game mode settings for additional settings.
//duellimit 5

// ╔════════════╗
// ║ DOMINATION ║
// ╚════════════╝
// In Domination, there are various domination points around the map, indicated by a giant beam of light, for your teams to capture.
// If nobody is controlling the point, then the light is white. To take control of the point simply walk over it and its yours!
// Every 3 seconds, your team receives 1 point for each point under your control.
// Check global game mode settings for additional settings.
//domination true

// ╔═══════════╗
// ║ TEAM GAME ║
// ╚═══════════╝
// A basic team game mode for extensive customisation by mods. Consult the documentation for a mod for instructions on how to set it up.
//teamgame true

// ╔═══════════════════╗
// ║ COOPERATIVE MODES ║
// ╚═══════════════════╝

// Enemy Skill Settings
// Sets the difficulty of the overall game when monsters are present. This CVar is usually is intended for cooperative based games.
// 0 = Im too young to die, 1 = Hey, not too rough, 2 = Hurt me plenty, 3 = Ultra-Violence, 4 = Nightmare!, 5 = Black Metal (Brutal Doom ONLY)
//skill 5

// ╔═════════════╗
// ║ COOPERATIVE ║
// ╚═════════════╝
// The standard co-operative mode: fight with your friends to defeat the armies of hell.
//cooperative true

// ╔══════════════════════╗
// ║ SURVIVAL COOPERATIVE ║
// ╚══════════════════════╝
// A twist on co-operative in which each player has a set amount of lives. If you run out of lives, you cant respawn until the next map.
// If everyone runs out of lives, you lose and have to start again.
// Check global game mode settings to set your lives. "sv_maxlives"
//survival true

// ╔══════════╗
// ║ INVASION ║
// ╚══════════╝
// A co-operative game mode in which there are multiple increasingly difficult waves of monsters to fight. Can be combined with sv_maxlives to create Survival Invasion.
// Check global game mode settings to set your lives. "sv_maxlives"
//invasion true


//  ██████╗ ██████╗ ██╗   ██╗████████╗ █████╗ ██╗         ██████╗  ██████╗  ██████╗ ███╗   ███╗
//  ██╔══██╗██╔══██╗██║   ██║╚══██╔══╝██╔══██╗██║         ██╔══██╗██╔═══██╗██╔═══██╗████╗ ████║
//  ██████╔╝██████╔╝██║   ██║   ██║   ███████║██║         ██║  ██║██║   ██║██║   ██║██╔████╔██║
//  ██╔══██╗██╔══██╗██║   ██║   ██║   ██╔══██║██║         ██║  ██║██║   ██║██║   ██║██║╚██╔╝██║
//  ██████╔╝██║  ██║╚██████╔╝   ██║   ██║  ██║███████╗    ██████╔╝╚██████╔╝╚██████╔╝██║ ╚═╝ ██║
//  ╚═════╝ ╚═╝  ╚═╝ ╚═════╝    ╚═╝   ╚═╝  ╚═╝╚══════╝    ╚═════╝  ╚═════╝  ╚═════╝ ╚═╝     ╚═╝
// ╔═══════════════════════════════════════════════════════════════════════════════════════════════╗
// ║ The settings below should be used to change the Brutal Doom settings for your players         ║
// ║ like blood amount or to adjust the performance and game play experience.                      ║
// ║ To use these settings, you need to load the latest Brutal Doom v22 pk3 in your server script. ║
// ║ If you are not using brutal doom, make sure all configurations are commented out.             ║
// ╚═══════════════════════════════════════════════════════════════════════════════════════════════╝

// ╔═════════════════════╗
// ║ PERFORMANCE OPTIONS ║
// ╚═════════════════════╝

// Is this a Zandronum server?
// Uncomment this is required to make changes to some Brutal Doom settings.
// 0 = Yes
isrunningzandronum 0

// Blood Amount (Server).  (Value: 1|2|3|4|666)
// Requires: isrunningzandronum 0
// Set to Low by default. Uncomment to change setting.
// 1 = Low, 2 = Normal, 3 = Lots, 4 = Extreme, 666 = Comical
zdoombrutalblood 3

// Gore Janitor  (Server) - Makes gibs disappear after 30 seconds. (Value: 0|1)
// Requires: isrunningzandronum 0
// Disabled by default. Uncomment to change setting.
// 1 = Yes
//zdoombrutaljanitor 1

// Permanent spent casings. (Value: 0|1)
// Set to No by default. Uncomment to change setting.
// 1 = Yes
bd_infinitecasings 1

// Water Ripple Effects. (Value: 0|1)
// Set to No by default. Uncomment to change setting.
// 0 = Yes
bd_disablewaterripples2 0

// Destructible bodies (Does not affect Mancubi and Revenant corpses).  (Value: 0|1)
// Set to Yes by default. Uncomment to change setting.
// 1 = No
//BD_DestructibleBodies 1

// Flashlight beam v21 or v22. WARNING - v21 can be more performance heavy. (Value: 0|1)
// Set to v22 by default. Uncomment to change setting.
// 1 = v21
//bd_flashlight 1

// Map Enhancement System
// Improves several maps with better textures, new decorations and sometimes new enemies.
// 0 = Enabled (Default), 1 = Disabled
//bd_disablemapenhancements 1

// MES - Disable Voxels
// Disable voxel decorations to prevent crashes on Android.
// 0 = Yes, 1 = No (Default)
//bd_voxeldec 0

// Brutal Dooms Bosses
// Reworks supported Icon of Sin maps and bosses.
// Disable this option if it causes problems on certain custom wads.
// 0 = Enabled (Default), 1 = Disabled
//BD_NOBOSSES 1

// Vanilla Monsters
// Disables new enemy AI and new attacks.
// 0 = No (Default), 1 = Yes
//bd_classicmonsters 1

// Advanced Decorations
// Fancy particle effects for torches and lamps.
// 0 = Enabled (Default), 1 = Disabled
//bd_disabledecorations 1


// ╔═══════════════════╗
// ║ HEADSHOT SETTINGS ║
// ╠═══════════════════╩══════════════════════════════════════════════════════════════╗
// ║ Headshot Detection Guide                                                         ║
// ╠══════════════════════════════════════════════════════════════════════════════════╣
// ║ This option will dictate what kind of headshot detection method enemies like the ║
// ║ Mancubi, Archviles, Hell Nobles, Revenants and Cyberdemons will use!             ║
// ╠═══════════════════════════════╦══════════════════════════════════════════════════╩═══════════════════════════════════════════╗
// ║ Dynamic(Default)              ║ Bigger enemies will prioritize using the old detection system as long                        ║
// ║                               ║ they are below a very low ceiling or if the map hasnt been been detected as a slaughter map! ║
// ║                               ║                                                                                              ║
// ║ Semi-force Blood Type only    ║ Bigger enemies will use the less precise but less intensive blood                            ║
// ║                               ║ detection for headshots! However enemies that are spawned below very low ceiling will spawn  ║
// ║                               ║ with the old headshot hitbox in order to not get stuck in place!                             ║
// ║                               ║                                                                                              ║
// ║ Force headshot hitboxes only! ║ Bigger enemies will always use the more precise and performance                              ║
// ║                               ║ intensive headshot detection even if the map is detected as a slaughter map.                 ║
// ╚═══════════════════════════════╩══════════════════════════════════════════════════════════════════════════════════════════════╝
// Headshot Detection. (Value: 0|1|2)
// 0 = Dynamic(Default), 1 = Semi-force Blood Type only, 2 = Force headshot hitboxes only
//BD_NoHeadshots 1


// ╔═══════════════╗
// ║ LEVEL OPTIONS ║
// ╠═══════════════╩═════════════════════════════════════════════════════════════════════════════╗
// ║ Mapset used. (Value: 0|1|2|3|4|5|6|7|8|9|10|11)                                             ║
// ║ This option is NOT AUTOMATIC and requires to be MANUALLY TOGGLED before starting            ║
// ║ a new game on one of the supported wads!                                                    ║
// ║ NOTE: Use one of the three "Doom II" Mapsets for any wads not listed below. (Value: 1|6|10) ║
// ╠═══════╦════════════════════════════════════╦════════════════════════════════════════════════╩════════════════════════════════════════════════════════════════════════════════════════════════╗
// ║ Value ║ Supported WAD                      ║ Sprite Replacements                                                                                                                             ║
// ╠═══════╬════════════════════════════════════╬═════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════╣
// ║ 1     ║ DOOM II (Brutal Doom Nazis)        ║ Wolfenstein SS with Brutal Dooms Nazis.                                                                                                         ║
// ║ 6     ║ DOOM II (Brutal Wolfenstein Nazis) ║ Wolfenstein SS with their ZioMcCalls Brutal Wolfenstein counterparts.                                                                           ║
// ║ 10    ║ DOOM II (Former Marines)           ║ Wolfenstein SS with a Zombie Marine variant.                                                                                                    ║
// ║ 7     ║ Ancient Aliens                     ║ Mancubi with Ancient Mancubi;Arachnotrons with Ancient Arachnotrons;Wolfenstein SS with Cloaked Marines;Commander Keens with Alien guardians    ║
// ║ 9     ║ Eviternity                         ║ Barons of hell with Cyber Bruisers;Commander keens with Astral Cacodemons;The Helper Dog with Nightmare Demons;Icon of Sin with the Archangelus ║
// ║ 2     ║ Scythe II                          ║ Wolfenstein SS with Evil Marines;Commander Keens with Afrits                                                                                    ║
// ║ 3     ║ Going Down                         ║ Wolfenstein SS with the Mother Demon                                                                                                            ║
// ║ 4     ║ Epic 2                             ║ Wolfenstein SS with Cloaked Aliens                                                                                                              ║
// ║ 5     ║ Bloodstain                         ║ Wolfenstein SS with SMG Zombies                                                                                                                 ║
// ║ 8     ║ TNT:Revilution                     ║ Replaces Wolfenstein SS and Commander keens with stationary turrets                                                                             ║
// ║ 11    ║ Jenesis                            ║ Wolfenstein SS with Zombie Shotgun                                                                                                              ║
// ╚═══════╩════════════════════════════════════╩═════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════╝
// bd_WadCheck 10


// ╔══════════════════╗
// ║ GAMEPLAY OPTIONS ║
// ╚══════════════════╝

// Rocket Launcher backblast/knockback.
// 0 = No, 1 = Yes (Default)
//bd_rocketbackblast 0

// Aiming Mode. (Value: 0|1|2)
// 0 = Both (Default), 1 = Toggle, 2 = Hold
//bd_AimMode 2

// Damaging lava splashes.
// 0 = Yes (Default), 1 = No
//bd_LavaSplashes 1

// Footstep Sounds
// 0 = No, 1 = Yes (Default)
//bd_footstepsounds 0

// Spawn Demon Spheres
// 0 = Yes (Default), 1 = No
//bd_disabledemonspheres 1

// Rescuable Marines
// 0 = Yes (Default), 1 = No
//bd_disablefriendlymarines 1

// Shootable rocket ammo
// 0 = No (Default), 1 = Yes
//bd_shootablerocketammo 1

// ╔═══════════════════════════╗
// ║ EXTREME GAMEPLAY MODIFIER ║
// ╚═══════════════════════════╝

// BDV21 Cacodemons - Cacodemons can be killed with a single SSG blast. (Value: 0|1)
// Disabled by default. Uncomment to change setting.
// 1 = Enabled
//bdv22_Caco 1

// Agile Posessed - Let zombies dodge your attacks by jumping or rolling. (Value: 0|1|2|3|4)
// Disabled by default. Uncomment to change setting.
// 0 = Disabled, 1 = Rarely, 2 = Sometimes, 3 = Often, 4 = Always (Dont)
// bd_AgileZombies 1

// Extra Enemies - Restores spawnable Pistol Zombies ,SMG Zombies and Scientists. (Value: 0|1)
// Disabled by default. Uncomment to change setting.
// 0 = Enabled
// bd_disablenewenemies 0

// Ledge Climbing - Allows you to mantle ledges. (Value: 0|1)
// Disabled by default. Uncomment to change setting.
// 1 = On
//bd_mantling 1

// Infinite Sprint (Tactical only) - Removes stamina consumption while sprinting. (Value: 0|1)
// Off by default. Uncomment to change setting.
// 0 = On
// bd_InfiniteSprin 1

// Reloading for all weapons. (Value: 0|1)
// Enabled by default. Uncomment to change setting.
// 1 = Disabled
//bd_reloading 1

// Assault Rifles burst fire. (Value: 0|1)
// Enabled by default. Uncomment to change setting.
// 1 = Disabled
//bd_V21AR 1

// Auto-Reload for all weapons. (Value: 0|1)
// Enabled by default. Uncomment to change setting.
// 0 = Off
//bd_autoreload 0

// Spectres drop blurspheres. (Value: 0|1)
// Enabled by default. Uncomment to change setting.
// 1 = Disabled
//BD_NODEMONBlur 1

// Demon Strength Rune. (Value: 0|1)
// Enabled by default. Uncomment to change setting.
// 1 = Disabled
// NoDemonStrenght 1

// ╔═════════════════════════╗
// ║ WEAPON SPAWNER SETTINGS ║
// ╚═════════════════════════╝

// ╔════════════════════════╗
// ║ Backpacks weapons list ║
// ╠════════════════════════╩═════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════╗
// ║ Limited - Submachine Gun,Assault Shotgun,Grenade,Launcher,Railgun,BFK10K,Flamethrower,Incendiary Launcher,Nuke Launcher                                      ║
// ║ Expanded - Submachine Gun,Assault Shotgun,Grenade,Launcher,Railgun,BFK10K,Flamethrower,Incendiary Launcher,Nuke Launcher,Dragon Slayer,MP40,MG42,Devastators ║
// ║ 1 = Backpacks Only, 3 = Limited (Default), 2 = Expanded                                                                                                      ║
// ╚══════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════╝
//BD_AmmoPackCheck 1

// Customize Chainsaw Spawner. (Value: 0|1|2)
// 0 = Randomized, 1 = Chainsaw Only (Default), 2 = Axe Only
//bd_disablechainsawspawn 2

// Customize Shotgun Spawner. (Value: 0|1|2)
// 0 = Randomized, 1 = Shotgun Only (Default), 2 = Revolver Only
//BD_ShotgunSpawner 2

// Customize Super Shotgun Spawner. (Value: 0|1|2)
// 0 = Randomized, 1 = Super Shotgun Only (Default), 2 = Assault Shotgun Only
//bd_disablessgspawn 2

// Customize Chaingun Spawner. (Value: 0|1|2|4)
// 0 = Randomized, 1 = Chaingun Only (Default), 2 = SMG Only, 4 = Assault Rifle Only
//bd_disablechaingunspawn 4

// Customize Rocket Launcher Spawner. (Value: 0|1|2)
// 0 = Randomized, 1 = Rocket Launcher Only (Default), 2 = Grenade Launcher Only
//bd_disablerocketlauncherspawn 2

// Customize Plasma Rifle Spawner. (Value: 0|1|2)
// 0 = Randomized, 1 = Plasma Rifle Only (Default), 2 = Railgun Only
//bd_disableplasmaspawn 2

// Customize BFG9000 Spawner. (Value: 0|1|2|3)
// 0 = Randomized, 1 = BFG 9000 Only (Default), 2 = BFG10K Only, 3 = Unmaker Only
//bd_disablebfgspawn 3

// Enable MG42?. (Value: 0|1)
// Replaces the BFG with a MG42 in Doom 2s map31.
// We recommend disabling this when playing other wads.
// 0 = Yes, 1 = No (Default)
//BD_NoMg42 0

// Disable Demons weapons?
// Removes Revenants Launchers and Mancubis Flame Cannons pickups.
// 0 = No (Default), 1 = Yes
//BD_NODEMONWEAPONS 1

// ╔═══════════════════════╗
// ║ SCREEN EFFECT OPTIONS ║
// ╚═══════════════════════╝

// Screen Effects
// Screen Effects on HUD, (Blood Splashing, Bullet Holes etc.)
// 0 = Yes (Default), 1 = No
//bd_ScreenFX 1

// Blood Trail Splash
// Blood Splashing when Enemies are bleeding out.
// If Screen Effects is disabled, this option will also be disabled.
// Does not work for the BDv21 Mode.
// 0 = Yes (Default), 1 = No
//bd_BloodTrail 1


//  ██████╗ ███╗   ███╗███████╗██╗      █████╗  ██████╗ ███████╗
//  ██╔══██╗████╗ ████║██╔════╝██║     ██╔══██╗██╔════╝ ██╔════╝
//  ██║  ██║██╔████╔██║█████╗  ██║     ███████║██║  ███╗███████╗
//  ██║  ██║██║╚██╔╝██║██╔══╝  ██║     ██╔══██║██║   ██║╚════██║
//  ██████╔╝██║ ╚═╝ ██║██║     ███████╗██║  ██║╚██████╔╝███████║
//  ╚═════╝ ╚═╝     ╚═╝╚═╝     ╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚══════╝
//  ╔════════════════════════════════════════╦════════════╦══════════════════════════════════════════════════════════════════════════════════════════╦══════════════════════════════════════════════════════════════════════════════════════════════════════════════════╗
//  ║ Flag Name                              ║ Value      ║ Description                                                                              ║ Notes                                                                                                            ║
//  ╠════════════════════════════════════════╬════════════╬══════════════════════════════════════════════════════════════════════════════════════════╬══════════════════════════════════════════════════════════════════════════════════════════════════════════════════╣
//  ║ Disallow health (DM)                   ║ 1          ║ Prevents health from spawning on the map.                                                ║                                                                                                                  ║
//  ║ Disallow powerups (DM)                 ║ 2          ║ Prevents powerups from spawning on the map.                                              ║ This dmflag is non functional as per https://forum.zdoom.org/viewtopic.php?f=7&t=14285                           ║
//  ║ Weapons stay (DM)                      ║ 4          ║ Weapons remain after being picked up by a player.                                        ║                                                                                                                  ║
//  ║ Falling damage (ZDoom)                 ║ 8          ║ Enables the falling damage used from ZDoom.                                              ║                                                                                                                  ║
//  ║ Falling damage (Hexen)                 ║ 16         ║ Enables the stronger but less aggressive falling damage used from Hexen.                 ║                                                                                                                  ║
//  ║ Falling damage (Strife)                ║ 8 + 16     ║ Combining both values for ZDoom and Hexen enables the falling damage used from Strife.   ║ The minimum amount of damage you take from falling in Strife is 52. Ouch!                                        ║
//  ║                                        ║ 32         ║ (unused)                                                                                 ║                                                                                                                  ║
//  ║ Stay on the same map (DM)              ║ 64         ║ Stay on the same map when someone exits.                                                 ║                                                                                                                  ║
//  ║ Spawn farthest (DM)                    ║ 128        ║ Spawn players as far as possible from other players.                                     ║                                                                                                                  ║
//  ║ Force respawn (DM)                     ║ 256        ║ Forces the players that were killed to respawn.                                          ║ Requires alwaysapplydmflags to be true to have an effect outside of deathmatch mode.                             ║
//  ║ Disallow armor (DM)                    ║ 512        ║ Prevents armor from spawning on the map.                                                 ║                                                                                                                  ║
//  ║ Disallow exit (DM)                     ║ 1024       ║ Kill anyone that tries to exit from the map.                                             ║                                                                                                                  ║
//  ║ Infinite ammo                          ║ 2048       ║ Players have infinite ammo.                                                              ║                                                                                                                  ║
//  ║ No monsters                            ║ 4096       ║ Monsters do not spawn on the map.                                                        ║                                                                                                                  ║
//  ║ Monsters respawn                       ║ 8192       ║ Monsters will respawn sometime after their death.                                        ║                                                                                                                  ║
//  ║ Items respawn                          ║ 16384      ║ Items respawn after being picked up by a player. However mega powerups will not respawn. ║ Dooms RadSuit and Heretics Wings of Wrath will always respawn in survival regardless of this CVars value.        ║
//  ║ Fast monsters                          ║ 32768      ║ Monsters are more faster and more aggressive                                             ║ Both they and projectiles use their FastSpeed property instead of their speed.                                   ║
//  ║ Disallow jump                          ║ 65536      ║ Prevents players from jumping.                                                           ║                                                                                                                  ║
//  ║ Allow jumping                          ║ 131072     ║ Allows the players to jump regardless of the MAPINFO NoJumping argument.                 ║                                                                                                                  ║
//  ║ Disallow freelook                      ║ 262144     ║ Prevents the players from being able to freelook.                                        ║                                                                                                                  ║
//  ║ Mega powerups respawn                  ║ 524288     ║ Allows mega powerups (i.e: invisibility invulnerability) to respawn.                     ║ Requires sv_itemrespawn to be true.                                                                              ║
//  ║ Disallow FOV                           ║ 1048576    ║ Disallows the clients to use a different Field of View value. [Default: 90]              ║                                                                                                                  ║
//  ║ Dont spawn multiplayer weapons (Coop)  ║ 2097152    ║ Prevents multiplayer only weapons from spawning.                                         ║                                                                                                                  ║
//  ║ Disallow crouch                        ║ 4194304    ║ Disallow players ability to crouch.                                                      ║                                                                                                                  ║
//  ║ Allow crouch                           ║ 8388608    ║ Allow players to crouch regardless of the NoCrouch flag on the MAPINFO lump.             ║                                                                                                                  ║
//  ║ Lose inventory (Coop)                  ║ 16777216   ║ Players lose all of their inventory when killed.                                         ║                                                                                                                  ║
//  ║ Lose keys (Coop)                       ║ 33554432   ║ Players will lose all of their keys when killed.                                         ║                                                                                                                  ║
//  ║ Lose weapons (Coop)                    ║ 67108864   ║ Players will lose all of their weapons when killed.                                      ║                                                                                                                  ║
//  ║ Lose armor (Coop)                      ║ 134217728  ║ Players will lose all of their armor when killed.                                        ║                                                                                                                  ║
//  ║ Lose powerups (Coop)                   ║ 268435456  ║ Players will lose all of their powerups when killed.                                     ║                                                                                                                  ║
//  ║ Lose ammo (Coop)                       ║ 536870912  ║ Players will lose all their ammo when killed.                                            ║                                                                                                                  ║
//  ║ Lose half ammo                         ║ 1073741824 ║ Players lose half of their ammo when killed.                                             ║                                                                                                                  ║
//  ╚════════════════════════════════════════╩════════════╩══════════════════════════════════════════════════════════════════════════════════════════╩══════════════════════════════════════════════════════════════════════════════════════════════════════════════════╝
//
//  Each one of these values you choose must be added together.
//  Example: Disallow health (DM) 1 + Disallow powerups (DM) 2 = dmflags 3
//dmflags 0


//  ██████╗ ███╗   ███╗███████╗██╗      █████╗  ██████╗ ███████╗██████╗
//  ██╔══██╗████╗ ████║██╔════╝██║     ██╔══██╗██╔════╝ ██╔════╝╚════██╗
//  ██║  ██║██╔████╔██║█████╗  ██║     ███████║██║  ███╗███████╗ █████╔╝
//  ██║  ██║██║╚██╔╝██║██╔══╝  ██║     ██╔══██║██║   ██║╚════██║██╔═══╝
//  ██████╔╝██║ ╚═╝ ██║██║     ███████╗██║  ██║╚██████╔╝███████║███████╗
//  ╚═════╝ ╚═╝     ╚═╝╚═╝     ╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚══════╝╚══════╝
//  ╔═══════════════════════════════════════╦══════════╦═══════════════════════════════════════════════════════════════════╦═════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════╗
//  ║ Flag Name                             ║ Value    ║ Description                                                       ║ Notes                                                                                                                                                                       ║
//  ╠═══════════════════════════════════════╬══════════╬═══════════════════════════════════════════════════════════════════╬═════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════╣
//  ║                                       ║ 1        ║ (unused)                                                          ║                                                                                                                                                                             ║
//  ║ Drop weapons                          ║ 2        ║ Players drop their current weapon when killed or fragged.         ║                                                                                                                                                                             ║
//  ║ Dont spawn runes                      ║ 4        ║ Prevents runes from spawning on the map.                          ║                                                                                                                                                                             ║
//  ║ Instant flag return (ST/CTF)          ║ 8        ║ Flags are instantly returned when the carriers are fragged.       ║                                                                                                                                                                             ║
//  ║ No team switching (ST/CTF)            ║ 16       ║ Players cannot change teams after already being on a team.        ║                                                                                                                                                                             ║
//  ║ Server picks teams (ST/CTF)           ║ 32       ║ Players are placed in teams automatically by the server.          ║                                                                                                                                                                             ║
//  ║ Double ammo                           ║ 64       ║ Double amount of ammo that items give you like skill 0 and 4 do.  ║                                                                                                                                                                             ║
//  ║ Degeneration                          ║ 128      ║ Players slowly lose health when above 100%                        ║  like in Quake.                                                                                                                                                             ║
//  ║ Allow BFG freeaiming                  ║ 256      ║ Allows the BFG to be fired vertically.                            ║                                                                                                                                                                             ║
//  ║ Barrels respawn                       ║ 512      ║ Barrels respawn after being blown up                              ║ Only works in non-deathmatch game modes if "alwaysapplydmflags" is true!                                                                                                    ║
//  ║ No respawn protection (In Deathmatch) ║ 1024     ║ Players do not have temporary invulnerability when respawning.    ║                                                                                                                                                                             ║
//  ║ Start with shotgun (In Cooperative)   ║ 2048     ║ Players will have a shotgun when they spawn.                      ║                                                                                                                                                                             ║
//  ║ Spawn where died (In Cooperative)     ║ 4096     ║ Players respawn at the same location they were killed at.         ║                                                                                                                                                                             ║
//  ║ Keep frags                            ║ 8192     ║ The clients frags are never reset when advancing to the next map. ║                                                                                                                                                                             ║
//  ║ No respawning                         ║ 16384    ║ Players can not respawn once killed or fragged.                   ║                                                                                                                                                                             ║
//  ║ Lose frag when fragged                ║ 32768    ║ When fragged                                                      ║  the player will lose a frag point.                                                                                                                                         ║
//  ║ Infinite inventory                    ║ 65536    ║ When true                                                         ║  using an inventory item will not expend it.                                                                                                                                ║
//  ║ Kill all monsters (In Cooperative)    ║ 131072   ║ All monsters must be killed before advancing into the next map.   ║                                                                                                                                                                             ║
//  ║ Disallow automap                      ║ 262144   ║ Disallow players to utilize the Automap.                          ║                                                                                                                                                                             ║
//  ║ Disallow allies on automap            ║ 524288   ║ Disallow players to see allies on the Automap.                    ║                                                                                                                                                                             ║
//  ║ Disallow spying                       ║ 1048576  ║ Disallow players from spying other players.                       ║                                                                                                                                                                             ║
//  ║ Chasecam                              ║ 2097152  ║ Allow the players to utilize the chasecam feature.                ║                                                                                                                                                                             ║
//  ║ Disallow suicide                      ║ 4194304  ║ Disallow the players to use the kill CCMD.                        ║                                                                                                                                                                             ║
//  ║ Disallow autoaim                      ║ 8388608  ║ Disallow the clients ability to use Autoaim.                      ║                                                                                                                                                                             ║
//  ║ Check ammo for weapon switch          ║ 16777216 ║ Weapon mush have ammo to be switched to.                          ║                                                                                                                                                                             ║
//  ║ Killing Romero kills all his spawns   ║ 33554432 ║                                                                   ║ This option makes it so the death of the BossBrain kills all monsters created by the BossEye before ending the level allowing a 100% kill tally on the intermission screen. ║
//  ║ Count monsters in end level sectors   ║ 67108864 ║                                                                   ║ This option makes monsters placed in sectors with the dDamage_End type (as used in Doom E1M8) not count towards the total.                                                  ║
//  ╚═══════════════════════════════════════╩══════════╩═══════════════════════════════════════════════════════════════════╩═════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════╝
//
//  Each one of these values you choose must be added together.
//  Example: Drop weapons 2 + Dont spawn runes 4 = dmflags2 6
//dmflags2 0


//  ███████╗ █████╗ ██████╗ ███╗   ███╗███████╗██╗      █████╗  ██████╗ ███████╗
//  ╚══███╔╝██╔══██╗██╔══██╗████╗ ████║██╔════╝██║     ██╔══██╗██╔════╝ ██╔════╝
//    ███╔╝ ███████║██║  ██║██╔████╔██║█████╗  ██║     ███████║██║  ███╗███████╗
//   ███╔╝  ██╔══██║██║  ██║██║╚██╔╝██║██╔══╝  ██║     ██╔══██║██║   ██║╚════██║
//  ███████╗██║  ██║██████╔╝██║ ╚═╝ ██║██║     ███████╗██║  ██║╚██████╔╝███████║
//  ╚══════╝╚═╝  ╚═╝╚═════╝ ╚═╝     ╚═╝╚═╝     ╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚══════╝
//  ╔═════════════════════════════════════════╦══════════╦══════════════════════════════════════════════════════════════════════════════════════════════════╦═══════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════╗
//  ║ Flag Name                               ║ Value    ║ Description                                                                                      ║ Notes                                                                                                                                     ║
//  ╠═════════════════════════════════════════╬══════════╬══════════════════════════════════════════════════════════════════════════════════════════════════╬═══════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════╣
//  ║ Never identify players                  ║ 1        ║ Clients can never identify other players when pointing at them.                                  ║                                                                                                                                           ║
//  ║ Enforce LMS spectator settings          ║ 2        ║ lms_spectatorchat will be respected in all game modes.                                           ║                                                                                                                                           ║
//  ║ Dont draw Coop Info                     ║ 4        ║ Disallows clients to utilize the Coop Info CVar regardless if enabled from the clients CVar.     ║                                                                                                                                           ║
//  ║ Disable unlagged                        ║ 8        ║ Disables unlagged support for all clients. (default false)                                       ║                                                                                                                                           ║
//  ║ Disable player collisions               ║ 16       ║ Allows players to pass through each other.                                                       ║ Great for small or cramped maps on Multiplayer.                                                                                           ║
//  ║ No medals                               ║ 32       ║ The medals feature will be disabled and will not be displayed nor upkept within the game.        ║                                                                                                                                           ║
//  ║ Share keys                              ║ 64       ║ For Cooperative and Survival game modes                                                          ║                                                                                                                                           ║
//  ║ Keep teams                              ║ 128      ║ Prevent players from changing teams on map change.                                               ║                                                                                                                                           ║
//  ║ Force Video defaults                    ║ 256      ║ If this is enabled some default rendering options are enforced.                                  ║ Clients render as if; gl_texture == 1; gl_lightmode == 3; gl_light_ambient == 20.0; gl_fogmode == 1; gl_lights_size == 1; r_3dfloors == 1 ║
//  ║ No rocket jumping                       ║ 512      ║ Disallow players from rocket jumping.                                                            ║                                                                                                                                           ║
//  ║ Award damage instead of kills           ║ 1024     ║ Players will be awarded points from the damage that they do on monsters                          ║                                                                                                                                           ║
//  ║ Force alpha                             ║ 2048     ║ Clients are enforced to display alpha i.e. render as if r_drawtrans was enabled.                 ║                                                                                                                                           ║
//  ║ Only spawn single player actors in coop ║ 4096     ║ Map actors are spawned as if the game was single player.                                         ║                                                                                                                                           ║
//  ║ Emulate vanilla blood brightness.       ║ 8192     ║ Forces blood brightness to max when damaged.                                                     ║                                                                                                                                           ║
//  ║ Unblock players on same team            ║ 16384    ║ Allows players of the same team to pass through each other only.                                 ║                                                                                                                                           ║
//  ║ Dont allow dropping.                    ║ 32768    ║ Prevents players from dropping items.                                                            ║                                                                                                                                           ║
//  ║ No map reset                            ║ 65536    ║ In a Survival game the map is not reset if all players die.                                      ║                                                                                                                                           ║
//  ║ Dead players keep inventory             ║ 131072   ║ In a Survival game when a player loses all of their lives                                        ║  they keep their inventory.                                                                                                               ║
//  ║ No unlagged BFG tracers                 ║ 262144   ║ Prevents use of backwards reconciliation for the hitscan tracers fired from the BFG9000.         ║                                                                                                                                           ║
//  ║ No manually closing doors               ║ 524288   ║ Stops doors from being manually closed.                                                          ║ Prevents players from intentionally (or unintentionally) griefing by closing doors that other players (or the same player) have opened.   ║
//  ║ Force software pitch limits             ║ 1048576  ║ Force client software renderers in all circumstances.                                            ║                                                                                                                                           ║
//  ║ Shoot through allies                    ║ 2097152  ║ Players attacks whether hitscans or projectiles to pass through teammates and friendly monsters  ║ This is ignored by actors who have FORCEALLYCOLLISION enabled.                                                                            ║
//  ║ Dont push allies                        ║ 4194304  ║ Prevents a players attacks and barrel explosions from thrusting teammates and friendly monsters  ║ This is ignored by actors who have FORCEALLYCOLLISION enabled.                                                                            ║
//  ║ Dont keep join queue                    ║ 8388608  ║ The join queue will be cleared between levels.                                                   ║ (development version 3.2-alpha and above only)                                                                                            ║
//  ║ Dont hide stats                         ║ 16777216 ║ Allows players to see the health and armour of other players in competitive game modes.          ║ (development version 3.2-alpha and above only)                                                                                            ║
//  ║ Dont override player colors             ║ 33554432 ║ Prevents players from overriding player colors via the cl_overrideplayercolors CVar.             ║ (development version 3.2-alpha and above only)                                                                                            ║
//  ╚═════════════════════════════════════════╩══════════╩══════════════════════════════════════════════════════════════════════════════════════════════════╩═══════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════════╝
//
//  Each one of these values you choose must be added together.
//  Example: Never identify players 1 + Enforce LMS spectator settings 2 = zadmflags 3
//zadmflags 0


//   ██████╗ ██████╗ ███╗   ███╗██████╗  █████╗ ████████╗███████╗██╗      █████╗  ██████╗ ███████╗
//  ██╔════╝██╔═══██╗████╗ ████║██╔══██╗██╔══██╗╚══██╔══╝██╔════╝██║     ██╔══██╗██╔════╝ ██╔════╝
//  ██║     ██║   ██║██╔████╔██║██████╔╝███████║   ██║   █████╗  ██║     ███████║██║  ███╗███████╗
//  ██║     ██║   ██║██║╚██╔╝██║██╔═══╝ ██╔══██║   ██║   ██╔══╝  ██║     ██╔══██║██║   ██║╚════██║
//  ╚██████╗╚██████╔╝██║ ╚═╝ ██║██║     ██║  ██║   ██║   ██║     ███████╗██║  ██║╚██████╔╝███████║
//   ╚═════╝ ╚═════╝ ╚═╝     ╚═╝╚═╝     ╚═╝  ╚═╝   ╚═╝   ╚═╝     ╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚══════╝
//  ╔═════════════════════════════════════════╦═════════════╦═════════════════════════════════════════════════════════════════════════════════════════════════════════════╗
//  ║ Flag Name                               ║ Value       ║ Description                                                                                                 ║
//  ╠═════════════════════════════════════════╬═════════════╬═════════════════════════════════════════════════════════════════════════════════════════════════════════════╣
//  ║ Find shortest textures like Doom        ║ 1           ║ AASHITTY in Doom II or AASTINKY in Doom was created to fill in the place of texture index 0 normally        ║
//  ║                                         ║             ║ treated by the Doom engine as no texture at all. When this is enabled the "raise platform by lower          ║
//  ║                                         ║             ║ texture" line special and MAP07 floor raise considers AASHITTY or AASTINKY as a valid texture and uses its  ║
//  ║                                         ║             ║ height when raising a platform. If disabled these textures arent considered valid and are ignored.          ║
//  ║ Use buggier stair building              ║ 2           ║ Calculate heights of stairs when stair building from the top step instead of the bottom step.               ║
//  ║ Limit pain elementals to 20 lost souls  ║ 4           ║ Prevents pain elementals from spawning lost souls if there are 20 or more on the map.                       ║
//  ║ Dont let others hear pickups            ║ 8           ║ This prevents players from hearing other players picking up items weapons or powerups in netgames.          ║
//  ║ Actors are infinitely tall              ║ 16          ║ This causes all objects to occupy an infinite vertical space from the ceiling to the floor which prevents   ║
//  ║                                         ║             ║ monsters or the player from being able to pass over or under other solid objects regardless of whether      ║
//  ║                                         ║             ║ they are touching each other on the Z plane or not.                                                         ║
//  ║                                         ║             ║ WARNING: Enabling this will break ZDoom-style thing bridges and objects that rely on height sensitivity.    ║
//  ║ Allow silent BFG trick                  ║ 32          ║ Forces all actors to play all sounds only on one channel cutting off any previous sounds the actor has      ║
//  ║                                         ║             ║ made. Only enable this if you cant live without the silent BFG trick as it will cripple the sound system    ║
//  ║                                         ║             ║ and prevent actors from playing any more than one sound at a time.                                          ║
//  ║ Enable wallrunning                      ║ 64          ║ This uses a buggier method of collision detection with walls that allows a player to run double average     ║
//  ║                                         ║             ║ speed when pressing against a vertically-aligned wall.                                                      ║
//  ║ Spawn item drops on the floor           ║ 128         ║ Items dropped by monsters appear on the floor below the center of the monster instead of being tossed from  ║
//  ║                                         ║             ║ the monsters corpse. May cause items to get stuck in walls or appear at the bottom of pits.                 ║
//  ║ All special lines can block use lines   ║ 256         ║ Any lines with line specials prevent the player from triggering a usable line behind it regardless of       ║
//  ║                                         ║             ║ whether the frontmost line can be used itself or not.                                                       ║
//  ║ Disable Boom door light effect          ║ 512         ║ Dont do the BOOM local door light effect                                                                    ║
//  ║ Ravens scrollers use original speed     ║ 1024        ║ Ravens scrollers use their original carrying speed                                                          ║
//  ║ Use sector based sound target code      ║ 2048        ║ Use sector based sound target code.                                                                         ║
//  ║ Limit deh.MaxHealth to health bonus     ║ 4096        ║ Players can not exceed over the 200% health as you can with just the normal MaxHealth bonuses.              ║
//  ║ Trace ign. lines w. s. sec on b. sides  ║ 8192        ║ Trace ignores lines with the same sector on both sides                                                      ║
//  ║ No monster dropoff move                 ║ 16384       ║ Monsters cannot move when hanging over a dropoff                                                            ║
//  ║ Scrolling sectors are additve           ║ 32768       ║ Scrolling sectors are additive like in Boom                                                                 ║
//  ║ Monsters see semi-invisible players     ║ 65536       ║ Monsters will be able to see the player even if the player has a partial invisibility sphere.               ║
//  ║ Silent instant floors                   ║ 131072      ║ Instantly moving floors are not silent                                                                      ║
//  ║ Sector sounds                           ║ 262144      ║ Sector sounds use original method for sound origin.                                                         ║
//  ║ Doom missile clip                       ║ 524288      ║ Use original Doom heights for clipping against projectiles                                                  ║
//  ║ Monster drop off                        ║ 1048576     ║ Monsters cant be pushed over dropoffs                                                                       ║
//  ║ Allow any bossdeath for level special   ║ 2097152     ║ If enabled any actor type which calls A_BossDeath triggers the levels special even if they are not          ║
//  ║                                         ║             ║ supposed to. This emulates a pre-Doom v1.9 behavior which is exploited by Doomsday of UAC.                  ║
//  ║ No Minotaur floor flames in water       ║ 4194304     ║ If enabled maulotaurs are unable to create their floor fire attack if their feet are clipped by water       ║
//  ║                                         ║             ║ sludge lava or other terrain effect. Note that the flames can still travel across water; this was on the    ║
//  ║                                         ║             ║ part of Raven Softwares developers as it was a bug found in the original clipping code and not an attempt   ║
//  ║                                         ║             ║ at realism as some may have believed.                                                                       ║
//  ║ Original A_Mushroom speed in DEH mods   ║ 8388608     ║ If enabled when the A_Mushroom codepointer is called from a state that was modified by a DeHackEd lump it   ║
//  ║                                         ║             ║ uses the original MBF behavior of the codepointer. This option does not affect states defined in DECORATE.  ║
//  ║ Monster movement is affected by effects ║ 16777216    ║ If enabled monsters are affected by sector friction wind and pusher/puller effects as they are in MBF.      ║
//  ║                                         ║             ║ By default monsters are not subjected to friction and only affected by wind and pushers/pullers if they     ║
//  ║                                         ║             ║ Have the WINDTHRUST flag.                                                                                   ║
//  ║ Crushed monsters can be resurrected     ║ 33554432    ║ If enabled corpses under a vertical door or crusher are changed into gibs rather than replaced by a   be    ║
//  ║                                         ║             ║ different actor if they do not have a custom Crush state. This allows an arch-vile or similar monster to    ║
//  ║                                         ║             ║ resurrect them. By default actors without a custom Crush state are removed entirely and can therefore not   ║
//  ║                                         ║             ║ raised from the dead.                                                                                       ║
//  ║ Friendly monsters arent blocked         ║ 67108864    ║ If enabled friendly monsters are like in MBF not affected by lines with the "block monsters" flag  with     ║
//  ║                                         ║             ║ allowing them to follow the player all around a map. This option does not however block them at lines       ║
//  ║                                         ║             ║ the "block player" flag.                                                                                    ║
//  ║ Invert sprite sorting                   ║ 134217728   ║ If enabled the original Doom sorting order for overlapping sprites is used.                                 ║
//  ║ Use Doom code for hitscan checks        ║ 268435456   ║ If enabled the original Doom code for hitscan attacks is used. This reintroduces two bugs which makes       ║
//  ║                                         ║             ║ hitscan attacks less likely to hit. The first is that it is a monsters cross-section rather than its        ║
//  ║                                         ║             ║ bounding box that is used to check for impact; this makes attacks with a limited range (especially melee    ║
//  ║                                         ║             ║ attacks) unlikely to hit very wide monsters. The second is the blockmap bug: if an actor crosses block      ║
//  ║                                         ║             ║ boundaries and its center is in a different block than the one in which the impact happens then there is    ║
//  ║                                         ║             ║ no collision at all letting attacks pass through it harmlessly.                                             ║
//  ║ Find neighboring light like Doom        ║ 536870912   ║ If enabled when a light level changes to the highest light level found in neighboring sectors the search    ║
//  ║                                         ║             ║ is made only for the first tagged sector like in Doom.                                                      ║
//  ║ Draw polyobjects like Hexen             ║ 1073741824  ║ Uses the old flawed polyobject system for maps that relied on its glitches.                                 ║
//  ║ Ignore Y offsets on masked midtextures  ║ -2147483648 ║ This option emulates a vanilla renderer glitch by ignoring the Y locations of patches drawn on two-sided    ║
//  ║                                         ║             ║ midtextures and instead always drawing them at the top of the texture.                                      ║
//  ╚═════════════════════════════════════════╩═════════════╩═════════════════════════════════════════════════════════════════════════════════════════════════════════════╝
//
//  Each one of these values you choose must be added together.
//  Example: Find shortest textures like Doom 1 + Use buggier stair building 2 = compatflags 3
//compatflags 0


//   ██████╗ ██████╗ ███╗   ███╗██████╗  █████╗ ████████╗███████╗██╗      █████╗  ██████╗ ███████╗██████╗
//  ██╔════╝██╔═══██╗████╗ ████║██╔══██╗██╔══██╗╚══██╔══╝██╔════╝██║     ██╔══██╗██╔════╝ ██╔════╝╚════██╗
//  ██║     ██║   ██║██╔████╔██║██████╔╝███████║   ██║   █████╗  ██║     ███████║██║  ███╗███████╗ █████╔╝
//  ██║     ██║   ██║██║╚██╔╝██║██╔═══╝ ██╔══██║   ██║   ██╔══╝  ██║     ██╔══██║██║   ██║╚════██║██╔═══╝
//  ╚██████╗╚██████╔╝██║ ╚═╝ ██║██║     ██║  ██║   ██║   ██║     ███████╗██║  ██║╚██████╔╝███████║███████╗
//   ╚═════╝ ╚═════╝ ╚═╝     ╚═╝╚═╝     ╚═╝  ╚═╝   ╚═╝   ╚═╝     ╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚══════╝╚══════╝
//  ╔══════════════════════════════════╦═══════╦═════════════════════════════════════════════════════════════════════════════════════════════════════════════╗
//  ║ Flag Name                        ║ Value ║ Description                                                                                                 ║
//  ╠══════════════════════════════════╬═══════╬═════════════════════════════════════════════════════════════════════════════════════════════════════════════╣
//  ║ Cannot travel straight NSEW      ║ 1     ║ This option emulates the error in the original engines sine table by offsetting player angle when spawning  ║
//  ║                                  ║       ║ or teleporting by one fineangle (approximatively 0.044°) preventing the player from facing directly in a    ║
//  ║                                  ║       ║ cardinal direction.                                                                                         ║
//  ║ Use Dooms floor motion behavior  ║ 2     ║ This option undoes a Boom fix to floor movement logic. If this option is on a floor may rise through the    ║
//  ║                                  ║       ║ ceiling or a ceiling may lower through a floor.                                                             ║
//  ║ Non-blocking lines can be pushed ║ 64    ║ For maps that expect non-blocking push lines to activate when you are standing on them and run into a       ║
//  ║                                  ║       ║ completely different line. (for example Thing Thrust Z ladders)                                             ║
//  ╚══════════════════════════════════╩═══════╩═════════════════════════════════════════════════════════════════════════════════════════════════════════════╝
//
//  Each one of these values you choose must be added together.
//  Example: Cannot travel straight NSEW 1 + Use Dooms floor motion behavior 2 = compatflags2 3
//compatflags2 0


//  ███████╗ █████╗  ██████╗ ██████╗ ███╗   ███╗██████╗  █████╗ ████████╗███████╗██╗      █████╗  ██████╗ ███████╗
//  ╚══███╔╝██╔══██╗██╔════╝██╔═══██╗████╗ ████║██╔══██╗██╔══██╗╚══██╔══╝██╔════╝██║     ██╔══██╗██╔════╝ ██╔════╝
//    ███╔╝ ███████║██║     ██║   ██║██╔████╔██║██████╔╝███████║   ██║   █████╗  ██║     ███████║██║  ███╗███████╗
//   ███╔╝  ██╔══██║██║     ██║   ██║██║╚██╔╝██║██╔═══╝ ██╔══██║   ██║   ██╔══╝  ██║     ██╔══██║██║   ██║╚════██║
//  ███████╗██║  ██║╚██████╗╚██████╔╝██║ ╚═╝ ██║██║     ██║  ██║   ██║   ██║     ███████╗██║  ██║╚██████╔╝███████║
//  ╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚═════╝ ╚═╝     ╚═╝╚═╝     ╚═╝  ╚═╝   ╚═╝   ╚═╝     ╚══════╝╚═╝  ╚═╝ ╚═════╝ ╚══════╝
//  ╔═══════════════════════════════════════════╦══════════╦═════════════════════════════════════════════════════════════════════════════════════════════════════════════╗
//  ║ Flag Name                                 ║ Value    ║ Description                                                                                                 ║
//  ╠═══════════════════════════════════════════╬══════════╬═════════════════════════════════════════════════════════════════════════════════════════════════════════════╣
//  ║ Client side scripts (NET)                 ║ 1        ║ Uses Skulltags old behavior when (NET) ACS Scripts are used. This is disabled by default for advantages     ║
//  ║                                           ║          ║ compatibility among other ZDoom wads. If the WAD file is designed for Skulltag and uses NET script          ║
//  ║                                           ║          ║ then you would enable this feature.                                                                         ║
//  ║ Clients send full button info             ║ 2        ║ This needs to be enabled to make the ACS function work on server side scripts with buttons other than       ║
//  ║                                           ║          ║ BT_ATTACK;BT_USE;BT_JUMP;BT_CROUCH;BT_TURN180;BT_ALTATTACK;BT_RELOAD;BT_ZOOM                                ║
//  ║                                           ║          ║ Because it increases net traffic it should only be activated if needed.                                     ║
//  ║ No land                                   ║ 4        ║ If this is enabled players are not allowed to use the land CCMD.                                            ║
//  ║ Old random generator                      ║ 8        ║ If this is enabled the original Doom random table is used to generate random integers in [0255] which       ║
//  ║                                           ║          ║ should make for instance the SSG cause a little more damage.                                                ║
//  ║ NOGRAVITY spheres                         ║ 16       ║ This compatflag gives the specified spheres the NOGRAVITY flag but only when they are spawned by the map.   ║
//  ║                                           ║          ║ Invulnerability Sphere;Mega Sphere;Soul Sphere;Blur Sphere                                                  ║
//  ║ Dont stop player scripts on disconnect    ║ 32       ║ The ACS scripts with a player as activator are not terminated when this player disconnects.                 ║
//  ║ Old explosion thrust                      ║ 64       ║ Enables the original (greater) horizontal explosion thrust.                                                 ║
//  ║ Old bridge drops                          ║ 128      ║ If this is enabled non-SOLID things (like flags) fall through invisible bridges.                            ║
//  ║ Old jump physics                          ║ 256      ║ Enables the old ZDoom 1.23b33 jump physics.                                                                 ║
//  ║ No weapon switch cancellation             ║ 512      ║ This flag disallows the ability to switch weapons while in the middle of. Once the selected weapon starts   ║
//  ║                                           ║          ║ its raising sequence it cannot be cancelled.                                                                ║
//  ║ Auto-aiming has vertical holes            ║ 1024     ║ Zandronum uses more tracers in order to fill in the vertical gaps of the autoaim this reverts it back to    ║
//  ║                                           ║          ║ vanilla Dooms three-tracer behavior.                                                                        ║
//  ║ West-facing spawns are silent             ║ 2048     ║ When set to true players who spawn facing west are silent as in vanilla Doom.                               ║
//  ║ Use old Skulltag jumping behavior         ║ 4096     ║ Restore Skulltag jumping behavior. This reverts the jumping change from ZDoom SVN revision 2970.            ║
//  ║ Reset Global ACS variables upon map reset ║ 8192     ║ When set to true any world or global-scope ACS variables/arrays will be reset upon resetting the map        ║
//  ║ No obituaries                             ║ 16384    ║ When set to true obituary messages will not be printed if a player dies.                                    ║
//  ║ Limited movement in the air               ║ 131072   ║ By default Zandronum gives players more maneuverability in the air than ZDoom. When this is true ZDoom’s    ║
//  ║                                           ║          ║ method is used. See Air Control for more precise details.                                                   ║
//  ║ Plasma bump bug                           ║ 262144   ║ Allows players to pick up items on the other side of solid walls by running into the wall at a specific     ║
//  ║                                           ║          ║ angle. This flag should only be used for old vanilla Doom maps that really need it; it can have serious     ║
//  ║                                           ║          ║ side effects on bridges and scrolling floors!                                                               ║
//  ║ Allow instant respawn                     ║ 524288   ║ Allows players to respawn instantly after being killed by holding down the "use" key when being hit.        ║
//  ║ Disable taunts                            ║ 1048576  ║ Prevents players from using the "taunt" command.                                                            ║
//  ║ Original sound curve                      ║ 2097152  ║ Enabling this uses the original Doom sound curve which causes sounds to fade away at a shorter distance.    ║
//  ║                                           ║          ║ When disabled the Hexen sound curve is used instead which allows players to hear sounds louder farther away ║
//  ║ Use old intermission screens/music        ║ 4194304  ║ Use doom2.exes original intermission screens/music.                                                         ║
//  ║ Disable stealth monsters                  ║ 8388608  ║ Disable stealth monsters since doom2.exe didnt have them.                                                   ║
//  ║ Old radius damage                         ║ 16777216 ║ The original Doom radius damage code is used i.e. explosions have infinite vertical range.                  ║
//  ║ Disable crosshair                         ║ 33554432 ║ Players will not be able to use crosshair.                                                                  ║
//  ║ Old weapon switch                         ║ 67108864 ║ Players will be forced to switch weapons every time they pick up a new weapon.                              ║
//  ╚═══════════════════════════════════════════╩══════════╩═════════════════════════════════════════════════════════════════════════════════════════════════════════════╝
//
//  Each one of these values you choose must be added together.
//  Example: Cannot travel straight NSEW 1 + Use Dooms floor motion behavior 2 = zacompatflags 3
//zacompatflags 0
```
