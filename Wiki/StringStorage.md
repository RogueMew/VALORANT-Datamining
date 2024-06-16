Here's a revised version:

---

Strings are typically organized within files referred to as String Tables, often named either `StringTable` or `Strings`.

If you're in search of additional string files, you might want to explore the string tracker, which monitors the [`Game.locres`](../String%20Tracker/README.md) files along with other smaller ones.

To illustrate the structure of a string, let's delve into how character strings are stored, focusing on Omen.

```json
{
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
```

For Omen, the essential information is stored under the `KeysToMetaData` key under `StringTable`. This section contains all the strings pertinent to his abilities and descriptions.

For instance, if we're interested in Omen's first ability, we'd locate the entry labeled "Ability1". Additionally, you may notice remnants of Omen's development, like a grenade ability that was eventually replaced with his teleport, but the key names remain unchanged.
