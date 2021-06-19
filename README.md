<h3 align="center">Menu referencing library for Gamesense.pub</h3>

  <p align="center">
    A library dedicated to removing unnecessary lines full of "ui.reference"
    <br />
    <a href="https://github.com/descisgay/ref_lib"><strong>Documentation »</strong></a>
    <br />
    <br />
    <a href="https://github.com/descisgay/ref_lib/issues">Report Bug</a>
    ·
    <a href="https://github.com/descisgay/ref_lib/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">How to use</a></li>
      </ul>
    </li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
I started to work on this "library" because after browsing the forums for a while, and looking at leaked/posted luas, I noticed that alot of the first few lines were dedicated to just, well, referencing menu items. This kinda looked ugly to me, so I decided I was going to make a library for it. All I've done is just include every important menu item into it's own category.

### Built With
* [Lua](https://lua.org)
* [Gamesense](https://gamesense.pub/forums/lua.php)



<!-- GETTING STARTED -->
## Getting Started
### Prerequisites
You must have a gamesense.pub account and an active subscription to use the library.

### Installation

For normal users
1. Subscribe to the library on the workshop.
2. Load gamesense

For developers<br>

Complete the two steps above, then require the lua like the example below:
```lua
--"note: this is a horrible example, as it would constantly log"
--"anti-aim is enabled in console if aa is enabled."
--"for proper implementation use your own callbacks, preferably"
--"through ui.set_callback"
local ref = require"ref_lib"

local function onPaint()
    if ui.get(ref.antiaim.enabled) then
        client.log("anti-aim is enabled")
    end 
end

client.set_event_callback("paint", onPaint)
```

<!-- DOCUMENTATION -->
## Documentation

Categories go as following:
* Ragebot
* Antiaim
* Fake lag
* Visuals
* Chams
* Misc

### Calls:
- ref.ragebot:
	- enabled - returns a table as following: [boolean, hotkey mode]
	- target_selection - returns a string
	- target_hitbox - returns a string(s)
	- multipoint - returns a table as following: [hitboxes, hotkey mode, scale dropdown]
	- multipoint_scale - returns an integer
	- prefer_safepoint - returns a boolean
	- force_safepoint - returns a hotkey state/mode
	- avoid_unsafe_hitboxes - returns a string(s)
	- automatic_fire - returns a boolean
	- automatic_penetration - returns a boolean
	- silent_aim - returns a boolean
	- hitchance - returns an integer
	- minimum_damage - returns an integer
	- automatic_scope - returns a boolean
	- reduce_aim_step - returns a boolean
	- maximum_fov - returns an integer
	- low_fps_mitigations - returns a string(s)
	- remove_recoil - returns a boolean
	- accuracy_boost - returns a string
	- delay_shot - returns a boolean
	- quick_stop - returns a table as following: [boolean, hotkey mode]
	- quick_stop_options - returns a string(s)
	- quick_peek_assist - returns a table as following: [boolean, hotkey mode]
	- quick_peek_assist_mode - returns a table as following: [string(s), color table]
	- resolver - returns a boolean
	- resolver_override - returns a hotkey state/mode
	- prefer_body_aim - returns a boolean
	- prefer_body_aim_disablers - returns a string(s)
	- force_body_aim - returns a hotkey state/mode
	- force_body_aim_on_peek - returns a boolean
	- duck_peek_assist - returns a hotkey state/mode
	- double_tap - returns a table as following: [boolean, hotkey mode]
	- double_tap_mode - returns a string
	- double_tap_hitchance - returns an integer
	- double_tap_fake_lag_limit - returns an integer
	- double_tap_quick_stop - returns a string(s)

- ref.antiaim:
	- enabled - returns a boolean
	- pitch - returns a string
	- yaw_base - returns a string
	- yaw - returns a table as following: [string, integer]
	- yaw_jitter - returns a table as following: [string, integer]
	- body_yaw - returns a table as following: [string, integer (only will return integer if not on opposite mode)]
	- freestanding_body_yaw - returns a boolean
	- fake_yaw_limit - returns an integer
	- edge_yaw - returns a boolean
	- freestanding - returns a table as following: [string, hotkey mode, string (should always be set to "Default" or freestanding will not work.)]
	- slow_motion - returns a table as following: [boolean, hotkey mode]
	- slow_motion_type - returns a string
	- leg_movement - returns a string
	- hide_shots - returns a table as following: [boolean, hotkey mode]
	- fake_peek - returns a table as following: [boolean, hotkey mode]

- ref.fakelag:
	- enabled - returns a table as following: [boolean, hotkey mode]
	- amount - returns a string
	- variance - returns an integer
	- limit - returns an integer

- ref.visuals:
	- activation_type - returns a hotkey state/mode
	- teammates - returns a boolean
	- dormant - returns a boolean
	- box - returns a table as following: [boolean, color table]
	- health - returns a boolean
	- name - returns a boolean
	- flags - returns a boolean
	- weapon_text - returns a boolean
	- weapon_icon - returns a table as following: [boolean, color table]
	- ammo - returns a table as following: [boolean, color table]
	- distance - returns a boolean
	- glow - returns a table as following: [boolean, color table]
	- hit_marker - returns a boolean
	- hit_marker_sound - returns a boolean
	- visualize_aimbot - returns a table as following: [boolean, color table]
	- visualize_aimbot_sp - returns a table as following: [boolean, color table]
	- visualize_sounds - returns a table as following: [boolean, color table]
	- line_of_sight - returns a table as following: [boolean, color table]
	- money - returns a boolean
	- skeleton - returns a table as following: [boolean, color table]
	- out_of_fov_arrow - returns a table as following: [boolean, color table, size, distance from crosshair]
	- radar - returns a boolean
	- dropped_weapons - returns a table as following: [string(s), color table]
	- grenades - returns a table as following: [boolean, color table]
	- innacuracy_overlay - returns a table as following: [boolean, color table]
	- recoil_overlay - returns a boolean
	- crosshair - returns a boolean
	- bomb - returns a table as following: [boolean, color table]
	- grenade_trajectory - returns a table as following: [boolean, color table]
	- grenade_trajectory_hit - returns a color table
	- grenade_proximity_warning - returns a boolean
	- spectators - returns a boolean
	- penetration_reticle - returns a boolean
	- hostages - returns a table as following: [boolean, color table]
	- shared_esp - returns a table as following: [boolean, hotkey mode]
	- shared_esp_with_other_team - returns a boolean
	- restrict_shared_esp_updates - returns a boolean
	- upgrade_tablet - returns a boolean
	- danger_zone_items - returns a boolean
	- remove_flashbang_effects - returns a boolean
	- remove_smoke_grenades - returns a boolean
	- remove_fog - returns a boolean
	- remove_skybox - returns a boolean
	- visual_recoil_adjustment - returns a string
	- transparent_walls - returns an integer
	- transparent_props - returns an integer
	- brightness_adjustment - returns a table as follows: [string, color table (only if set to night mode will color table exist.)]
	- remove_scope_overlay - returns a boolean
	- instant_scope - returns a boolean
	- disable_post_processing - returns a boolean
	- force_third_person_alive - returns a table as following: [boolean, hotkey mode]
	- force_third_person_dead - returns a boolean
	- disable_rendering_of_teammates - returns a boolean
	- bullet_tracers - returns a table as following: [boolean, color table]
	- bullet_impacts - returns a table as following: [boolean, integer]

- ref.chams:
	- player - returns a table as following: [boolean, color table]
	- player_behind_wall - returns a table as following: [boolean, color table, cham mode, accent color)] - will only have accent color if cham mode supports it
	
	- teammate - returns a table as following: [boolean, color table]
	- teammate_behind_wall - returns a table as following: [boolean, color table, cham mode, accent color)] - will only have accent color if cham mode supports it
	
	- local_player - returns a table as following: [boolean, color table, cham mode, accent color)] - will only have accent color if cham mode supports it
	
	- local_player_fake - returns a table as following: [boolean, color table, cham mode, accent color)] - will only have accent color if cham mode supports it
	- ragdolls - returns a boolean
	
	- hands - returns a table as following: [boolean, color table, cham mode, accent color)] - will only have accent color if cham mode supports it
	
	- weapon_viewmodel - returns a table as following: [boolean, color table, cham mode, accent color)] - will only have accent color if cham mode supports it
	
	- disable_model_occlusion - returns a boolean
	
	- shadow - returns a table as following: [boolean, color table]
	
	- props - returns a table as following: [boolean, color table]

- ref.misc:
	- override_fov - returns an integer
	- override_zoom_fov - returns an integer
	- knifebot - returns a table as following: [boolean, string(s)]
	- zeusbot - returns a boolean
	- automatic_weapons - returns a table as following: [boolean, integer]
	- reveal_competitive_ranks - returns a boolean
	- reveal_overwatch_players - returns a boolean
	- auto_accept_matchmaking - returns a boolean
	- clantag_spammer - returns a boolean
	- log_weapon_purchases - returns a boolean
	- log_damage_dealt - returns a boolean
	- automatic_grenade_release - returns a table as following: [boolean, hotkey mode]
	- ping_spike - returns a table as following: [boolean, hotkey mode, integer]
	- free_look - returns a hotkey state/mode
	- persistent_kill_feed - returns a boolean
	- last_second_defuse - returns a hotkey state/mode
	- disable_sv_pure - returns a boolean
	- unlock_hidden_cvars - returns a boolean (should only be used if cs:go is in -insecure mode.)
	- stantalone_quick_stop - returns a boolean
	- infinite_duck - returns a boolean
	- easy_strafe - returns a boolean
	- bunny_hop - returns a boolean
	- air_strafe - returns a boolean
	- air_strafe_direction - returns a string
	- air_strafe_smoothing - returns an integer
	- avoid_collisions - returns a boolean
	- zhop - returns a table as following: [boolean, hotkey mode, integer, integer]
	- pre_speed - returns a table as following: [boolean, hotkey mode]
	- no_fall_damage - returns a table as following: [boolean, color table]
	- air_duck - returns a string
	- blockbot - returns a table as following: [boolean, hotkey mode]
	- jump_at_edge - returns a table as following: [boolean, hotkey mode]
	- fast_walk - returns a boolean
	- menu_key - returns a hotkey state/mode
	- menu_color - returns a color table
	- dpi_scale - returns a string
	- anti_untrusted - returns a boolean
	- hide_from_obs - returns a boolean
	- low_fps_warning - returns a boolean
	- lock_menu_layout - returns a boolean
	- sv_maxusrcmdprocessticks - returns an integer
	- sv_maxunlag - returns an integer

Can't find something?
If you can't find a menu item you're looking for, it's probably because:
* I put it in a different category than what it is in the menu/renamed it. (You can look on the forums and find it in the source) - I renamed Anti-aim correction to resolver.
* You're looking for a menu item I did not include (Legitbot, Playerlist, Configs, Lua, and Skinchanger tabs are not referenced.)
* You didn't spell the reference item correctly: I replaced all spaces in menu items with an underscore.

Getting an error that says you're using a table incorrectly?
* You need to put a table index at the end of your call to the library (ref.ragebot.enabled[1], etcetera)

<!-- CONTRIBUTING -->
## Contributing
To contribute, please message me via the methods below. I will respond and add what you want me to, if it's deemed reasonable.
<!-- CONTACT -->
## Contact

You can dm me [on gamesense.pub](https://gamesense.pub/forums/profile.php?id=8103) - or via discord (desc#1548)

Project Link: [https://github.com/descisgay/ref_lib](https://github.com/descisgay/ref_lib)
