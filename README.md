# jim-mining

## FiveM MultiFramework Custom mining script by me from scratch

- Highly customisable via `locations.lua`
  - Locations are easily changeable/removable

- Features several ways to get materials
  - Gold Panning - Search specified streams for gold and silver, or trash
  - Mining - Mine to get stones that can be wash or cracked for materials
  - Stone Washing - Wash stone to find rare gems or gold
  - Stone Cracking - Crack open stones to find ores for crafting materials

- Customisable points for mining, stone cracking and gold panning
  - Add a Location for an ore to the config and it will use this location for both qb-target and a prop
  - Can place them anywhere, doesn't have to be just one mining location
  - I opted for a drilling animation as opposed to the pickaxe swinging
  - Nicely animated for better immersion

- NPC's spawn on the blip locations
  - These locations can also give third eye and select ones have context menus for selling points

- NPC's and ore's Spawn at Mineshaft + Quarry so your players can go to either

- Features simplistic built in crafting that uses recipes in the config.lua

- Features Jewel Cutting bench as an attempt to add more than just gold bars and such to sell
  - You can use your gold bars and jewels to craft other items to sell to a Jewellery Buyer

---

# Installation and more:
## [JixelPatterns GitBook Documentation](https://jixelpatterns.gitbook.io/docs)

### If you need support I have a discord server available, it helps me keep track of issues and give better support.
## [JixelPatterns Discord](https://discord.gg/9pCDHmjYwd)

### If you think I did a good job here, consider donating as it keeps by lights on and my cat round:
## [JixelPatterns Kofi](https://ko-fi.com/jixelpatterns)

# Steps for Qbox
- Add Inventory Items

    -- JIM-MINING
    stone = { label = "Stone", weight = 150, stack = true, close = false, description = "",
        client = { image = "stone.png", }
    },
    -- Ores
    ironore = { label = "Iron Ore", weight = 100, stack = true, close = false, description = "",
        client = { image = "ironore.png", }
    },
    leadore = { label = "Lead Ore", weight = 100, stack = true, close = false, description = "",
        client = { image = "leadore.png", }
    },
    copperore = { label = "Copper Ore", weight = 100, stack = true, close = false, description = "",
        client = { image = "copperore.png", }
    },
    sulfurore = { label = "Sulfur Ore", weight = 100, stack = true, close = false, description = "",
        client = { image = "sulfurore.png", }
    },
    silverore = { label = "Silver Ore", weight = 100, stack = true, close = false, description = "",
        client = { image = "silverore.png", }
    },
    goldore = { label = "Gold Ore", weight = 100, stack = true, close = false, description = "",
        client = { image = "goldore.png", }
    },
    uncut_sapphire = { label = "Uncut Emerald", weight = 100, stack = true, close = false, description = "",
        client = { image = "sapphireuncut.png", }
    },
    uncut_ruby = { label = "Uncut Ruby", weight = 100, stack = true, close = false, description = "",
        client = { image = "rubyuncut.png", }
    },
    uncut_emerald = { label = "Uncut Diamond", weight = 100, stack = true, close = false, description = "",
        client = { image = "emeralduncut.png", }
    },
    uncut_diamond = { label = "Uncut Sapphire", weight = 100, stack = true, close = false, description = "",
        client = { image = "diamonduncut.png", }
    },

    -- Nuggets
    ironnugget = { label = "Iron Nugget", weight = 75, stack = true, close = false, description = "",
        client = { image = "ironnugget.png", }
    },
    leadnugget = { label = "Lead Nugget", weight = 75, stack = true, close = false, description = "",
        client = { image = "leadnugget.png", }
    },
    coppernugget = { label = "Copper Nugget", weight = 75, stack = true, close = false, description = "",
        client = { image = "coppernugget.png", }
    },
    silvernugget = { label = "Silver Nugget", weight = 75, stack = true, close = false, description = "",
        client = { image = "silvernugget.png", }
    },
    goldnugget = { label = "Gold Nugget", weight = 75, stack = true, close = false, description = "",
        client = { image = "goldnugget.png", }
    },

    -- Extras
    sulfur = { label = "Sulfur", weight = 75, stack = true, close = false, description = "",
        client = { image = "sulfur.png", }
    },
    coal = { label = "Coal", weight = 75, stack = true, close = false, description = "",
        client = { image = "coal.png", }
    },
    charcoal = { label = "Charcoal", weight = 75, stack = true, close = false, description = "",
        client = { image = "charcoal.png", }
    },

    -- Raw Gems
    sapphire = { label = "Sapphire", weight = 50, stack = true, close = false, description = "",
        client = { image = "sapphire.png", }
    },
    ruby = { label = "Ruby", weight = 50, stack = true, close = false, description = "",
        client = { image = "ruby.png", }
    },
    emerald = { label = "Emerald", weight = 50, stack = true, close = false, description = "",
        client = { image = "emerald.png", }
    },
    diamond = { label = "Diamond", weight = 50, stack = true, close = false, description = "",
        client = { image = "diamond.png", }
    },

    -- Jewelry
    gold_diamond_ring = { label = "Diamond Gold Ring", weight = 275, stack = true, close = true, description = "",
        client = { image = "gold_diamond_ring.png", }
    },
    gold_emerald_ring = { label = "Emerald Gold Ring", weight = 275, stack = true, close = false, description = "",
        client = { image = "gold_emerald_ring.png", }
    },
    gold_ruby_ring = { label = "Ruby Gold Ring", weight = 275, stack = true, close = false, description = "",
        client = { image = "gold_ruby_ring.png", }
    },
    gold_sapphire_ring = { label = "Sapphire Gold Ring", weight = 275, stack = true, close = false, description = "",
        client = { image = "gold_sapphire_ring.png", }
    },

    silver_diamond_ring = { label = "Diamond Silver Ring", weight = 275, stack = true, close = false, description = "",
        client = { image = "silver_diamond_ring.png", }
    },
    silver_emerald_ring = { label = "Emerald Silver Ring", weight = 275, stack = true, close = false, description = "",
        client = { image = "silver_emerald_ring.png", }
    },
    silver_ruby_ring = { label = "Ruby Silver Ring", weight = 275, stack = true, close = false, description = "",
        client = { image = "silver_ruby_ring.png", }
    },
    silver_sapphire_ring = { label = "Sapphire Silver Ring", weight = 275, stack = true, close = false, description = "",
        client = { image = "silver_sapphire_ring.png", }
    },

    gold_diamond_necklace = { label = "Diamond Gold Necklace", weight = 600, stack = true, close = false, description = "",
        client = { image = "gold_diamond_necklace.png", }
    },
    gold_emerald_necklace = { label = "Emerald Gold Necklace", weight = 600, stack = true, close = false, description = "",
        client = { image = "gold_emerald_necklace.png", }
    },
    gold_ruby_necklace = { label = "Ruby Gold Necklace", weight = 600, stack = true, close = false, description = "",
        client = { image = "gold_ruby_necklace.png", }
    },
    gold_sapphire_necklace = { label = "Sapphire Gold Necklace", weight = 600, stack = true, close = false, description = "",
        client = { image = "gold_sapphire_necklace.png", }
    },

    silver_diamond_necklace = { label = "Diamond Silver Necklace", weight = 600, stack = true, close = false, description = "",
        client = { image = "silver_diamond_necklace.png", }
    },
    silver_emerald_necklace = { label = "Emerald Silver Necklace", weight = 600, stack = true, close = false, description = "",
        client = { image = "silver_emerald_necklace.png", }
    },
    silver_ruby_necklace = { label = "Ruby Silver Necklace", weight = 600, stack = true, close = false, description = "",
        client = { image = "silver_ruby_necklace.png", }
    },
    silver_sapphire_necklace = { label = "Sapphire Silver Necklace", weight = 600, stack = true, close = false, description = "",
        client = { image = "silver_sapphire_necklace.png", }
    },

    gold_diamond_earring = { label = "Diamond Gold Earrings", weight = 250, stack = true, close = false, description = "",
        client = { image = "gold_diamond_earring.png", }
    },
    gold_emerald_earring = { label = "Emerald Gold Earrings", weight = 250, stack = true, close = false, description = "",
        client = { image = "gold_emerald_earring.png", }
    },
    gold_ruby_earring = { label = "Ruby Gold Earrings", weight = 250, stack = true, close = false, description = "",
        client = { image = "gold_ruby_earring.png", }
    },
    gold_sapphire_earring = { label = "Sapphire Gold Earrings", weight = 250, stack = true, close = false, description = "",
        client = { image = "gold_sapphire_earring.png", }
    },

    silver_diamond_earring = { label = "Diamond Silver Earrings", weight = 250, stack = true, close = false, description = "",
        client = { image = "silver_diamond_earring.png", }
    },
    silver_emerald_earring = { label = "Emerald Silver Earrings", weight = 250, stack = true, close = false, description = "",
        client = { image = "silver_emerald_earring.png", }
    },
    silver_ruby_earring = { label = "Ruby Silver Earrings", weight = 250, stack = true, close = false, description = "",
        client = { image = "silver_ruby_earring.png", }
    },
    silver_sapphire_earring = { label = "Sapphire Silver Earrings", weight = 250, stack = true, close = false, description = "",
        client = { image = "silver_sapphire_earring.png", }
    },

    -- Ingots
    ironingot = { label = "Iron Ingot", weight = 750, stack = true, close = false, description = "",
        client = { image = "ironingot.png", }
    },
    leadingot = { label = "Lead Ingot", weight = 750, stack = true, close = false, description = "",
        client = { image = "leadingot.png", }
    },
    copperingot = { label = "Copper Ingot", weight = 750, stack = true, close = false, description = "",
        client = { image = "copperingot.png", }
    },
    goldingot = { label = "Gold Ingot", weight = 750, stack = true, close = false, description = "",
        client = { image = "goldingot.png", }
    },
    silveringot = { label = "Silver Ingot", weight = 750, stack = true, close = false, description = "",
        client = { image = "silveringot.png", }
    },

    -- Tools
    pickaxe = { label = "Pickaxe", weight = 1000, stack = false, close = false, description = "",
        client = { image = "pickaxe.png", }
    },
    miningdrill = { label = "Mining Drill", weight = 3000, stack = false, close = false, description = "",
        client = { image = "miningdrill.png", }
    },
    mininglaser = { label = "Mining Laser", weight = 2000, stack = false, close = false, description = "",
        client = { image = "mininglaser.png", }
    },
    drillbit = { label = "Drill Bit", weight = 50, stack = true, close = false, description = "",
        client = { image = "drillbit.png", }
    },
    goldpan = { label = "Gold Panning Tray", weight = 50, stack = true, close = false, description = "Don't worry you'll hit gold eventually!",
        client = { image = "goldpan.png", }
    },

## Rarity
