# Pingprovements

A mod that improves pings in Risk of Rain 2 in several different ways.

All credits for the original mod goes to [pixeldesu](https://github.com/pixeldesu/Cloudburst).

Credits for the original compatibility with the Survivors of the Void DLC goes to [radiden](https://github.com/radiden/pingprovements).

## Features

- Allows multiple pings by the same player
- Colors pings by the tier of the target
- Configurable lifetimes for all ping types
- Configurable colors for all ping types
- Show labels for ping targets (instead of just chat messages)
- Show the distance to pings
- Show a notification on item pings containing the item description (like pickup notifications) if the item has already been discovered
- Hide offscreen ping labels

## Installation

Simply copy `Pingprovements.dll` to your BepInEx plugin folder.

## Configuration

After the game has been started with the mod installed once, you will have a config file available with following options:

- `Durations`
    - `DefaultPingLifetime`: Lifetime of the default walk ping in seconds (Default: `6`)
    - `EnemyPingLifetime`: Lifetime of the enemy ping in seconds (Default: `8`)
    - `InteractablePingLifetime`: Lifetime of the interactable ping in seconds (Default: `30`)
- `Colors`
    - `DefaultPingColor`: Color of the default ping text (Default: `0.525,0.961,0.486,1.000`)
    - `EnemyPingColor`: Color of the enemy ping text (Default: `0.820,0.122,0.122,1.000`)
    - `InteractablePingColor`: Color of the interactable ping text (Default: `0.886,0.871,0.173,1.000`)
    - `TieredInteractablePingColor`: Color pings in their target tier color (Default: `true`)
- `SpriteColors`
    - `DefaultPingSpriteColor`: Color of the default ping sprite (Default: `0.527,0.962,0.486,1.000`)
    - `EnemyPingSpriteColor`: Color of the enemy ping sprite (Default: `0.821,0.120,0.120,1.000`)
    - `InteractablePingSpriteColor`: Color of the interactable ping sprite (Default: `0.887,0.870,0.172,1.000`)
- `ShowPingText`
    - `Chests`: Shows item names and cost on chest pings (Default: `true`)
    - `ShopTerminals`: Shows item names and cost on shop terminal pings (Default: `true`)
    - `Drones`: Shows drone type on broken drone pings (Default: `true`)
    - `Shrines`: Shows shrine type on shrine pings (Default: `true`)
    - `Pickups`: Shows item names on pickup pings (Default: `true`)
    - `Enemies`: Show names on enemy pings (Default: `true`)
    - `Distance`: Show the distance to made pings (Default: `true`)
    - `HideOffscreenPingText`: Hides the ping label if the ping goes offscreen (Default: `true`)
- `Notifications`
    - `ShowItemNotification`: Show pickup-style notification with description on ping of an already discovered item (Default: `true`)

This mod overrides the internal `fixedTimer` for pings after it has been built, so no special conditions like teleporter or shrine pings will change the time for `InteractablePingLifetime`.