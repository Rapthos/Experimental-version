# Experimental mss32 for Disciples 2 [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Features:

### BattleMsgData
```
- Get current attack count
battle:getUnitAttackCount( unit.id )
return: int Attack Count; 0 if unit not in the turn list.

- 
battle:isUnitTurn( unit.id )
return: bool.

- Set attack count. If value = 0 - give infinite turn.
battle:setUnitAttackCount( unit.id, int value )
return: int Attack Count

- Heal unit. Can accept negative value
battle:setHeal( unit.id, int value)
```
### Scenario
```
-- Add unit XP. Unit can`t lvl up. Can accept negative value.
scen:addUnitXP(const std::string& id, int value)
return: xp gain. Return 0 if can't gain or unit doesn't exist.

- Heal unit. Can accept negative value
scen:setUnitHeal(const std::string& id, int value)
return true.

- Returns if unit has modifier. Can accept unitId or string.
scen:hasUnitModifier(const IdView &unitId, const std::string &id)
Return true if has.

- Add modifier to unit.
scen:addUnitModifier(const IdView& unitId, const std::string& id)
Return true.

- Remove modifier from unit.
scen:removeUnitModifier(const IdView& unitId, const std::string& id)
Return true.
```

### License
[Detours](https://github.com/microsoft/Detours), [GSL](https://github.com/microsoft/GSL), [fmt](https://github.com/fmtlib/fmt) and [sol2](https://github.com/ThePhD/sol2) submodules as well as [![Lua](https://www.andreas-rozek.de/Lua/Lua-Logo_64x64.png)](http://www.lua.org/license.html) are using their own licenses.


This modification is not made or supported by Strategy First.<br />
Disciples 2 is a trademark of Strategy First Inc.

