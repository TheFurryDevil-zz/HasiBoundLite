This is a little DLL for Starbound that, when loaded, will add a new global table called **star** to every Lua context. In that table, in a subtable called **player** are a few functions. (All of them take a string as argument and work in singleplayer, multiplayer and with any mod setup)

**64 bit Starbound only**

#

**star.player.setName(name)**

Will simply set your characters name to *name* (Not your nickname in chat, but the name above your character). When you disconnect with a different name it will save that new name to the .player file of the character. If you don't want that you can call the function with the original name in a tech **uninit()** for example. Could be used to animate your name...

#

**star.player.addChatMessage(msg)**

Will set your characters chatbubble text to *msg*.
Could be used to talk without sending it to the chat...

#

**star.player.setSpecies(species)**

Will set your characters species, also persistent. A bit useless because as of now I didn't add functions to change the hair type and other stuff you can select in the char creation.

#

**star.player.setBodyDirectives(directives)**

**star.player.setEmoteDirectives(directives)**

**star.player.setHairDirectives(directives)**

These change the directives found in the .player file. Could be used to animate your hair or character in general...

## How to install

Simply inject the DLL into Starbound, before joining a server (or join again), and the functions should be available
