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

####For normal users
1. Subscribe to the library on the workshop.
2. Load gamesense

###For developers
Complete the two steps above, then require the lua like the example below:
```lua
--"note: this is a horrible example, as it would constantly log"
--"anti-aim is enabled in console if aa is enabled."
--"for proper implementation use your own callbacks, preferably"
--"through ui.set_callback"
local ref = require 'gamesense/ref_lib'

local function onPaint()
    if ui.get(ref.antiaim.enabled) == true then
        console.log("anti-aim is enabled")
    end 
end

client.set_event_callback("paint", onPaint)
```
####Categories go as following:
* Ragebot
* Antiaim
* Visuals
* Misc

####Can't find something?
If you can't find a menu item you're looking for, it's probably because:
* I put it in a different category than what it is in the menu/renamed it. (You can look on the forums and find it in the source) - I renamed Anti-aim correction to resolver.
* You're looking for a menu item I did not include (Legitbot, Playerlist, Configs, Lua, and Skinchanger tabs are not referenced.)
* You didn't spell the reference item correctly: I replaced all spaces in menu items with an underscore.


<!-- CONTRIBUTING -->
## Contributing
To contribute, please message me via the methods below. I will respond and add what you want me to, if it's deemed reasonable.
<!-- CONTACT -->
## Contact

You can dm me [on gamesense.pub](https://gamesense.pub/forums/profile.php?id=8103) - or via discord (desc#1548)

Project Link: [https://github.com/descisgay/ref_lib](https://github.com/descisgay/ref_lib)
