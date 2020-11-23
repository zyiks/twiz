# Live Conquers

*You need "Manage Server" or "Administrator" permissions to use these commands.*

This command allows to set channels as monitor channels, where the bot will post desired bot conquers with a delay of around one minute. 

### Adding monitors

You need to add a monitor for each tribe seperately. For "monitor groups" it is recommended to make seperate channels.

>!addmonitor \<tribe tag> \<gain> \<loss> \<barbarian> \<self conquer> \<internal>

The first parameter is the **tribe tag**. This should be set to the tribe you want conquer information about. 

If the tribe tag contains spaces, surround it with quotation marks.

The following parameters have to be answered with a **yes** or **no**. All the parameters have to be answered in order for the tribe to be monitored:

- gain *i.e. Show conquers, where the village is taken by the tribe*
- loss *i.e. Show conquers, where the village gets taken from tribe*
- barbarian *i.e. Show conquers, where the village taken was a barbarian village*
- self conquer *i.e. Show conquers, where the original village owner was the same as the taker*
- internal - *i.e. Show conquers, where the original village owner belongs to the same tribe as the taker*

**NB! When adding the monitor, it is important to remember the world preference order: 1) Channel 2) Global**

Example:

>!addmonitor Cicada no yes no no yes

## Listing monitors

The following command displays all the active monitors in the channel.

>!listmonitor

## Removing monitors

The following command removes all the monitors about the given tribe tag from the current channel.

>!clearmonitor \<tribe tag>

Example:

>!clearmonitor Cicada