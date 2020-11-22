# Worlds

*You need "Manage Server" or "Administrator" permissions to use these commands.*

### World configuration types

There are 2 types of world configration in TWiz:

1. Channel World
2. Global/default World

Most commands will first check if the channel world is set and if its not, then the global world, and their returned information is based on the world found first.

For both type of worlds, you need to use the shorthand name for the world, eg. en110

You can usually find this shorthand name from the domain name in the world, eg. https://**en110**.tribalwars.net or your regions equivalent.

### Setting global world

Global world is used for every Discord channel, that doesn't have a channel world set.

> !set_world \<world_name>

Example:

> !set_world en110

### Setting channel world

> !set_channel_world \<world_name>

Example:

> !set_channel_world en110


*Remember, if you changed your prefix, you need to use the new one you set!*