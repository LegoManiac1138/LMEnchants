# LMEnchants

---

## Contents
- [Features](#features)
- [Installation](#installation)
- [Configuration](#configuration)
- [Permissions](#permissions)
- [Dependencies](#dependencies)

---

<br>

## Information
<p>
LMEnchants is a plugin that adds custom enchantments to Minecraft, while also allowing customization of vanilla 
enchantments. While normally, custom enchantments aren't able to be rendered by the Client, Item lore formatting is done
for Vanilla and Custom Enchants.
</p>

---

<br>

## Features
- Formatting for both Vanilla and Custom Enchantments.
- Custom Enchantment table for adding enchantments to items.
- Customization of every enchantment's base cost, as well as the formula for all enchantments.
- Anvil interaction has been altered to reflect changes to Custom and Vanilla enchantments.
- Enchantment Crystals, which function like Enchanted Books, but for use in other plugins.
---

<br>

## Current Enchantments
<h3>_Mining_</h3>
- <span style="color:yellow">Haste</span>: Gives the player the "Haste" potion effect.
- <span style="color:yellow">Excavator</span>: Digs a cuboid area that scales with the enchantment level. (with Support for WorldGuard regions).
- <span style="color:yellow">Telekinesis</span>: Adds blocks broken to your inventory instead of dropping on the ground first.
- <span style="color:yellow">Smelting</span>: Like Silk Touch, but smelts raw ores into their ingot form. Fortune allies to such items.

<h3>_Boots_</h3>
- <span style="color:yellow">Speed</span>: Gives the player the "Speed" potion effect.

<br>

<h3>_More to come in the future..._</h3>
<h4>  Custom Enchantments will be registered using an Item's internal storage instead of hacked into the Enchantment class,
as Minecraft has removed the ability to register an enchantment 1.20.5+.</h4>

<br>

## Installation
1. Download the latest version
2. Place the .jar file into the /plugins directory inside the server folder
3. Restart the server.
4. Configure enchantment costs and display names inside /plugins/LMEnchants/enchant_settings.yml.
---

<br>

## Configuration

<h4>Level Formatting:</h4>
```yaml
# The enum that determines the formatting for Enchantment names. ROMAN_NUMERAL follows 
# default Minecraft behavior, whereas NUMERIC is Base 10 format.
format: ROMAN_NUMERAL
```

<h4>Enchantment Crystals:</h4>
```yaml
# This enables/disables the Enchantment Crystal functionality for Vanilla Crystals. This can
# allow a Server owner to only allow Custom Enchantments to be received this way. Crystals allow 
# the player to apply them without needing an anvil, and voids the XP cost.
vanilla_crystals: true 
```

<h4>Enchantment Formula:</h4>
```yaml
constant: 5.0  # This means that every level of an Enchantment is the base level times this number.
exponential: 1.2  # Every enchantment level will increase the XP cost exponentially by this number.
incremental: 3.0  # Every enchantment level will increase the XP cost incrementally by this number.
```

<h4>A sample configuration for the "Efficiency" Enchantment:<h4>
```yaml
enchants:
  efficiency:
    cost: 4     # The base XP level cost
    display_color: '&e'    # This will display the "Efficiency" name in Yellow
```
---

<br>

## Permissions

### Admin Permissions:
```
- lmenchants.admin: (Overarching permission for the plugin)
- lmenchants.commands: (Permission for all commands)
```
### Commands:
```
- lmenchants.commands.crystals: Command for Enchantment Crystals
- lmenchants.commands.enchants: Base Enchantment command
```

<br>

## Dependencies
- LuckPerms 