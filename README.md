# elunamod-wispofrain
This is a mod for Eluna for Azerothcore/TrinityCore.

### Description:
- When a user kills a creature, they have CHANCE_TO_SPAWN_WISP / MAX_CHANCE chance to spawn a wisp, provided they have the RISK_OF_RAIN spell.
- WISP_ENTRY will autocast from SPELL_ARRAY until killed or WISP_DURATION seconds have passed.
- If the killer or any party members have RISK_OF_RAIN_MOD_HARDMODE, then SHIELD_SPELL is on WISP_ENTRY until interrupted or stunned.
- If WISP_ENTRY is killed, then killer and party members will receive a random ID from BUFF_ARRAY / DEBUFF_ARRAY.
- As the buff is distributed, if RISK_OF_RAIN_MOD_NODEBUFFS is held by the unit, then that unit will only receive buffs.

All of the above values can be changed in the LUA file itself.

- Select your `world` database
- Import the code at the beginning of `RiskOfRain.lua`, specifically from where it says "SQL STARTS" to "SQL ENDS"
- If you have a `spell_dbc_12340` table from `WDBX Editor` or `Stoneharry's Spell Editor`, import the SPELL.DBC SQL from where it specifies start to end.
- - If using AzerothCore, you can instead edit these queries to insert into `spell_dbc` rather than the above table. You will NOT need to recreate the DBCs for the server or the client.
- If you do not have a `spell_dbc_12340` table, you will need to edit the contents of your `spell.dbc` to match these SQL values. Good luck! (It will be much easier to do the above)
- Recreate `spell.dbc` and import it to your sever and client.

# notice of future updates
This repo will receive limited updates, as each spell in the future will be manually scripted to have additional bells and whistles. The folder structure of this repo may change to include those additional spells.
