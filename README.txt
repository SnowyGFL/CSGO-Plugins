# CSGO-Plugins
My Plugins:
*AntiStackDamage - CS:GO Fix Fix trigger_hurt that has Parent

*AutoRestart - Automatically restarts the server at a specific time. Hud + Chat + Console Announce every minute(last minute - every second). AutoRetry clients when restarting the server
  -CVARS:
    #sm_autorestart <0/1> - Enable/Disable Auto Restart
    #sm_autorestart_time <0000-2359> - Time to restart server at
    #sm_autorestart_wait <0-30> - Wait to restart server at in Minutes
  -Admin Command:
    #sm_forcerestart [<time in minutes>] - Force Restart Server After <time>

*Auto_Retry - Remembers which maps the player played(SQLite DB). if the player plays for the first time on the map, then he automatically reconnects
  -Client Command:
    #sm_retryclear - Сleans the DB of maps played by the client

*EntWatch_DZ - Reworked EntWatch 3 for CS:GO

*EntWatch Old - Entwatch 3 for CS:GO with Hud + HudPos + HudColor + Glow + Transfer of discarded items(Give) + Menus + Block Pick up items with E+Change HUD Channel

*Hide_Teammates - Hides Teammates on the entire map or distance
  -Client Command:
    #sm_hide [<-1-CVAR_MAX_Distance>] (-1 - Disable, 0 - Enable on the entire map, 1-CVAR_MAX_Distance - Enable ont the Distance)
    #sm_hide - show menu
    #sm_hideall - toggle hide teammates on the entire map
  -CVARS:
    #sm_hide_enabled <0/1> - Enable/Disable plugin
    #sm_hide_maximum <1000-8000> - The maximum distance a player can choose

*Map Music Dhook SoundLib2 - Disable Map Music with Volume Control + Menus

*block_use_pickup_weapon - Ignore PickUp Weapons with press E

*buttonwatcher - Buttons Watcher with Bans and Menus. Watching func_button, momentary_rot_button, func_rot_button. Reacts: Use and Damage
  -CVARS:
    #sm_buttons_view <0/1> - Enable/Disable Global the display Buttons
    #sm_buttons_timer <0.0/10.0> - Timer before showing the pressed button again
  -Admin Command:
    #sm_bban <target> [<time in minutes>] - Buttons Ban on time. (-1 temporarily, 0 permanently, 1-... - ban on time)
    #sm_unbban <target> - Buttons UnBan
    #sm_bbanlist - Currently BBanned Statistic
  -Client Command:
    #sm_bstatus - Show status client's Buttons Ban
    #sm_buttons - Enable/Disable showing the client the button clicks

*helpmenu_multilang - Custom Multilang HelpMenu for new Clients. Show rules/Server Info/Clients Commands. Allows you to set your own text without Recompile plugin
  -Client Command:
    #sm_helpmenu - Show Helpmenu
    #F4 - Show Commands Menu(FakeClientCommand)
  -Admin Command:
    #sm_helpmenu_reload - Reload Config
*topdefenders_perk - TopDefenders+TopInfectors+Perk+built-in Downloadlist+Show Damage(current damage+Kills+total damage)+Show infect(Nickname victim+total infected)+Store Integration(Variably). Perk - Trail/Sprite/Model, Add Speed, Reduced Gravity, immunity to first infection and more
  -CVARS:
    #sm_topdefenders_enable <0/1> - Enable/Disable plugin
    #sm_topdefenders_topcount <3/15> - Number of people to top(Zombie Damage)
    #sm_topdefenders_perk <0/1> - Gives perk for the top(Zombie Damage)
    #sm_topdefenders_cashdiv <0/50> - Money for damage - Damage divider(Cash=Cash+Damage/Divider) 0 - Disable
    #sm_topdefenders_infectors_enable <0/1> - Enable Top Infector Addon
    #sm_topdefenders_infectors_topcount <3/15> - Number of people to top Infector
    #sm_topdefenders_infectors_perk <0/1> - Gives Infector perk for the top Infector
    #sm_topdefenders_immunity_chance <0/100> - Сhance of immunity from infection if prescribed in the configuration file
    #sm_topdefenders_immunity_minplayers <10/64> - Minimum players for immunity
    #sm_topdefenders_showdamage - Enable/Disable Show Hint Damage Addon
  -Admin Command:
    #sm_topdefenders_config_test1 - Test Config Top Defenders
    #sm_topdefenders_config_test2 - Test Config Top Infectors
    #sm_topdefenders_refresh - Refresh Config without show
  -Client Command:
    #sm_pr - Remove Perk from yourself
  -Configure perk/HUD position/Hud colors in addons\sourcemod\configs\topdefenders.cfg
  -Built-in Downloadlist in addons\sourcemod\configs\topdefenders_downloadlist.ini
  -You can configure a few perks per place(only one of the type), see ConfigFile
  -In order to integrate the shop you must uncomment #define SHOP and configure function names SHOP_SET_CREDITS_FUNC(Shop_SetClientCredits) and SHOP_GET_CREDITS_FUNC(Shop_GetClientCredits)
