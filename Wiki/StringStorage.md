Strings are stored in files usually called String Tables. The files are stored usually named `StringTable` or `Strings`

If you are looking for more string files you could also check the string tracker which tracks the [`Game.locres`](../String%20Tracker/README.md) files and some other small ones.

To show the format of a string we will be looking at how character strings are stored. Specifically Omen.

```json
[
  {
    "Type": "StringTable",
    "Name": "Wraith_Strings",
    "Class": "UScriptClass'StringTable'",
    "StringTable": {
      "TableNamespace": "Wraith_Strings",
      "KeysToMetaData": {
        "DisplayName": "Omen",
        "Prototype_DisplayName": "WraithPrototype",
        "Prototype_DisplayName_Teleport": "WraithTeleport",
        "Description": "A phantom of a memory, Omen hunts in the shadows. He renders enemies blind, teleports across the field, then lets paranoia take hold as his foe scrambles to uncover where he might strike next.",
        "Ability1_DisplayName": "Paranoia",
        "Ability1_Description": "EQUIP a blinding orb. FIRE to throw it forward, briefly Nearsighting and Deafening all players it touches. This projectile can pass straight through walls.",
        "Ability2_Description": "EQUIP a shadow orb, entering a phased world to place and target the orbs. PRESS the ability key to throw the shadow orb to the marked location, creating a long-lasting shadow sphere that blocks vision. HOLD FIRE while targeting to move the marker further away. HOLD ALT FIRE while targeting to move the marker closer. PRESS RELOAD to toggle normal targeting view.",
        "GrenadeAbility_DisplayName": "Shrouded Step",
        "GrenadeAbility_Description": "EQUIP a shrouded step ability and see its range indicator. FIRE to begin a brief channel, then teleport to the marked location.",
        "Ultimate_DisplayName": "From the Shadows",
        "Ultimate_Description": "EQUIP a tactical map. FIRE to begin teleporting to the selected location. While teleporting, Omen will appear as a Shade that can be destroyed by an enemy to cancel his teleport, or PRESS EQUIP for Omen to cancel his teleport.",
        "Prototype_Description_Teleport": "An enigmatic shadow, Wraith covers the battlefield and darkness and can teleport to unexpected locations. When Wraith's waround, it's never certain if you're ever truly safe.",
        "Buddy_DisplayName": "Omen Buddy",
        "GrenadeAbility_Description_Rank": "Rank 1: +1 Charge\r\nRank 2: +1 Charge\r\nRank 3: Cooldown (20)",
        "Ability2_Description_Rank": "Rank 1: +1 Charge\r\nRank 2: Cooldown (60)\r\nRank 3: Cooldown (20)",
        "Ability2_Teleporting": "TELEPORTING",
        "Ability1_Description_Rank": "Rank 1: +1 Charge\r\nRank 2: Kill Reset (2)",
        "Ultimate_TeleportStart": "GATHERING SHADOW",
        "Ultimate_TeleportOutro": "REFORMING",
        "Ultimate_TeleportWarning": "Omen Teleporting!",
        "Ability1_Tooltip": "Rank 1: Free Charge per Round\r\nRank 2: ",
        "Ultimate_DisplayNameCaps": "FROM THE SHADOWS",
        "Ability2_DisplayName": "Dark Cover",
        "DisplayName_AllCaps": "OMEN",
        "Prototype_DisplayName_AllCaps": "WRAITHPROTOTYPE"
      }
    },
    "StringTableId": 0
  }
]
```

For
Omen we can see we need to be looking for the json key `StringTable`. This holds all the strings we need for anything to be worth it.

```json
"StringTable": {
      "TableNamespace": "Wraith_Strings",
      "KeysToMetaData": {
        "DisplayName": "Omen",
        "Prototype_DisplayName": "WraithPrototype",
        "Prototype_DisplayName_Teleport": "WraithTeleport",
        "Description": "A phantom of a memory, Omen hunts in the shadows. He renders enemies blind, teleports across the field, then lets paranoia take hold as his foe scrambles to uncover where he might strike next.",
        "Ability1_DisplayName": "Paranoia",
        "Ability1_Description": "EQUIP a blinding orb.  FIRE to throw it forward, briefly Nearsighting and Deafening all players it touches. This projectile can pass straight through walls.",
        "Ability2_Description": "EQUIP a shadow orb, entering a phased world to place and target the orbs. PRESS the ability key to throw the shadow orb to the marked location, creating a long-lasting shadow sphere that blocks vision. HOLD FIRE while targeting to move the marker further away. HOLD ALT FIRE while targeting to move the marker closer. PRESS RELOAD to toggle normal targeting view.",
        "GrenadeAbility_DisplayName": "Shrouded Step",
        "GrenadeAbility_Description": "EQUIP a shrouded step ability and see its range indicator. FIRE to begin a brief channel, then teleport to the marked location.",
        "Ultimate_DisplayName": "From the Shadows",
        "Ultimate_Description": "EQUIP a tactical map. FIRE to begin teleporting to the selected location. While teleporting, Omen will appear as a Shade that can be destroyed by an enemy to cancel his teleport, or PRESS EQUIP for Omen to cancel his teleport.",
        "Prototype_Description_Teleport": "An enigmatic shadow, Wraith covers the battlefield and darkness and can teleport to unexpected locations. When Wraith's waround, it's never certain if you're ever truly safe.",
        "Buddy_DisplayName": "Omen Buddy",
        "GrenadeAbility_Description_Rank": "Rank 1: +1 Charge\r\nRank 2: +1 Charge\r\nRank 3: Cooldown (20)",
        "Ability2_Description_Rank": "Rank 1: +1 Charge\r\nRank 2: Cooldown (60)\r\nRank 3: Cooldown (20)",
        "Ability2_Teleporting": "TELEPORTING",
        "Ability1_Description_Rank": "Rank 1: +1 Charge\r\nRank 2: Kill Reset (2)",
        "Ultimate_TeleportStart": "GATHERING SHADOW",
        "Ultimate_TeleportOutro": "REFORMING",
        "Ultimate_TeleportWarning": "Omen Teleporting!",
        "Ability1_Tooltip": "Rank 1: Free Charge per Round\r\nRank 2: ",
        "Ultimate_DisplayNameCaps": "FROM THE SHADOWS",
        "Ability2_DisplayName": "Dark Cover",
        "DisplayName_AllCaps": "OMEN",
        "Prototype_DisplayName_AllCaps": "WRAITHPROTOTYPE"
      }
    }
```

String table holds all the strings you will need to disect to find anything useful such as ability names and descriptions.

Lets say for the 1st ability Omen has, I would look for something called ability 1. We can also see things that were part of Omens development but were changed out for something else without changing the Key name, this being a gernade he wouldve had which turned into his teleport.