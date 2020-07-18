This is a little DLL for Starbound that, when loaded, will add new functions to every Lua context. 
(All of them work in singleplayer, multiplayer and with any mod setup)

**64 bit Starbound only**

#

### New in 1.1.0:

**unsafe(string key)**

If you specify "unsafe_key" as a string in your starbound.config, it is not an empty string, and you pass the same value as argument, it will return a table with unsafe functions. Just print the table to see it's structure. This will allow you to keep "safeScripts" enabled without sacrificing it's functions.

**star.chat.focused()**

Returns whether the chat input field has focus.

**star.chat.text()**

Returns the text in the chat input field.

**star.player.aimPosition()**

Returns your aimPosition just like **tech.aimPosition()**, except in any script. Mostly for convenience.

**star.player.setFacialHair(string group, string type, string directives)**

**star.player.setFacialMask(string group, string type, string directives)**

**star.player.setHairType(string group, string type)**

Starbound uses these like **"/humanoid/\<species>/\<group>/\<type>:\<frame>\<directives>"**

**star.player.setGender(number gender)**

0 for male, 1 for female

**star.player.setPersonality(table personality)**

All values must be specified. Example: **{idle = "idle.1", armIdle = "idle.1", armOffset = {0, 0}, headOffset = {0, 0}}**

#

**star.player.setName(string name)**

Will simply set your characters name to *name* (Not your nickname in chat, but the name above your character). When you disconnect with a different name it will save that new name to the .player file of the character. If you don't want that you can call the function with the name that should be saved in a tech **uninit()**, for example.

**star.player.addChatMessage(string msg)**

Will set your characters chatbubble text to *msg*.

**star.player.setSpecies(string species)**

Will set your characters species, also persistent.

**star.player.setBodyDirectives(string directives)**

**star.player.setEmoteDirectives(string directives)**

**star.player.setHairDirectives(string directives)**

These change the directives also found in the .player file.

## How to install

Simply inject the DLL into Starbound, before joining a server (or join again), and the functions should be available
