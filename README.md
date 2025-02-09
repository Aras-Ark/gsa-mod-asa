# GameServerApp.com Integration mod for ARK:Survival Ascended

Create a customized version of the GSA Integration mod for your community.

> [!IMPORTANT]
> While you can use the source code to create your own mod, it is not allowed to advertise your mod as being the official GameServerApp mod (or similar). It is OK to mention that your mod works with GameServerApp API.

## Features

- [In-game shop](https://docs.gameserverapp.com/dashboard/integration_mod#in-game-shop)
- [Token gems](https://docs.gameserverapp.com/dashboard/integration_mod#token-gems)
- [Report issue / player form](https://docs.gameserverapp.com/dashboard/integration_mod#report-form)
- [Cluster chat](https://docs.gameserverapp.com/dashboard/integration_mod#cluster-chat)
- [Shortlink / URL / Vote buttons screen](https://docs.gameserverapp.com/dashboard/integration_mod#vote-screen)
- [Review / Rate community](https://docs.gameserverapp.com/dashboard/integration_mod#review)
- [Dino paint brush](https://docs.gameserverapp.com/dashboard/integration_mod#dino-paint-brush)
- [Mute players](https://docs.gameserverapp.com/dashboard/admin_tools/general#ban-kick--mute)
- [Enhanced notifications](https://docs.gameserverapp.com/dashboard/integration_mod#enhanced-notifications)
- [Twitch sub & RP access control](https://docs.gameserverapp.com/dashboard/admin_tools/general#whitelist)
- Radial menu - _for console support_

## Rcon commands
```
scriptcommand gsakill {steamid}  //can kill other players, at some occassions
scriptcommand gsakillnew {playerid}  //fixes bug from gsakill
scriptcommand gsateleport {steamid} {x y z}
scriptcommand gsainfo {steamid}
scriptcommand gsadinocoloring {amount} {steamid}
scriptcommand gsanotify {warning/danger/success} {duration} {steamid/global} {message}
scriptcommand gsamute {steamid} {true/false} {message}
scriptcommand gsachat {steamid/global} {name%^message}
scriptcommand gsadebug {true/false}
scriptcommand gsareport {steamid}
scriptcommand gsareview {steamid}
scriptcommand gsawatermark {middle|left} {true|false}
scriptcommand gsaxp {steamid} {amount}
```

## Test the mod
If you're curious and want to give the mod a try, there are currently 2 versions listed on the CurseForge website:
- [GameServerApp.com Integration (PC-only)](https://legacy.curseforge.com/ark-survival-ascended/mods/gameserverapp-integration)
- [GameServerApp.com integration (Console)](https://legacy.curseforge.com/ark-survival-ascended/mods/gsa-integration-no-shop)

# Development

### Why is the mod open source now?
Our main focus is working on the GameServerApp dashboard, and besides having to fix the mod due to breaking devkit updates, folks also asked for new features on the mod.<br>
We had to make a decision, since time is not unlimited. Instead of abandoning the mod, we went with open sourcing the mod.

### How about mod development?
GSA will no longer be actively involved in the development of the mod, and asked a mod developer to help us manage the open source repo.<br>
We will monitor changes, since it still bears the GSA name, but are not planning to take an active role.

We do plan to continue working on the Community API, which the mod relies on, and work with mod developers that want to add new features to the mod.

Currently active developer(s):
- [ropie](https://github.com/ropie)

### How to contribute / report issues
You can post new ideas for the mod in the [suggestions section](https://github.com/gameserverapp/gsa-mod-asa/discussions/categories/suggestions).<br>
Report bugs and/or issues in the [issues section](https://github.com/gameserverapp/gsa-mod-asa/issues).

# How to set up
The mod requires an active connection with the GSA Community API, in order to retrieve data from your dashboard.<br>
The API is used to retrieve what keybindings you have [configured on the dashboard](https://docs.gameserverapp.com/dashboard/integration_mod) or what [Shop packs](https://docs.gameserverapp.com/dashboard/monetization/shop_packs) are for sale, for example.

<br>

> [!WARNING]
> DO NOT share the API keys with anyone, treat them like passwords.<br>
> GSA Staff will __never__ ask for your API keys or password. 

<br>

### DediConnect
DediConnect users can paste the code below in their `GameUserSettings.ini`. GSA automatically replaces with the right values:
```
[gameserverapp]
ID={container.name}
ClientID={api.community.client_id}
ClientSecret={api.community.client_secret}
```


### RconConnect
When using a self-hosted or rented game server, you can get the required mod configurations from the [RconConnect Integrate page](https://docs.gameserverapp.com/getting_started/rconconnect/integrate).

![image](https://github.com/user-attachments/assets/f23458e6-97b2-4e54-b33e-d864ef0ae8a1)


# Developers
If you want to know more about the GSA API's and how to interact with them, check out the [GSA Community API docs](https://docs.gameserverapp.com/developers/community-api/shop-get-index).<br>
You can also reach out on [Discord](https://gameserverapp.com/join-discord).

### Getting started with the ARK Devkit
See the [ARK Devkit documentation website](https://devkit.studiowildcard.com/home) for more information about the devkit itself, or check out the [ARK modding community website](https://arkmodding.net/).

# Security
If you found a security issues please contact support@gameserverapp.com.<br>
Do not contact this email address for help with the mod. For help with the mod, join our [Discord](https://gameserverapp.com/join-discord).

## License
The GameServerApp.com Integration mod is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
