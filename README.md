# Experimental mss32 for Disciples 2 [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Features:

Available functions.

Functions are divided into scenario (scenarion) functions that work on the global map, and battle functions that work only in combat. Do not use scenario functions in combat and vice versa. Use getScenario() and _batInfo_getBattle() to get the scenario and battle respectively.

---

### Scenario functions:
```
AddUnitXP(IdView unitId, int value)
Adds experience to the selected unit. Experience cannot increase the level and will hit a ceiling, as in the training camp.
Arguments:
IdView unitId - unit ID (unit.id).
int value - amount of experience.
Returns:
int - amount of experience received by the unit.
```
```
SetHeal(IdView unitId, int value)
Heals the unit. A negative value will deal damage. The unit may die.
Arguments:
IdView unitId - unit ID (unit.id).
int value - healing amount. Can take a negative value.
Returns:
bool - true if successful.
```
```
HasUnitModifier(string or IdView unitId, string modId)
Checks if a unit has a modifier.
Arguments:
string or IdView unitId - unit ID (unit.id) or its ID as a string.
string modId - modifier ID.
Returns:
bool - true if the modifier exists, false if it doesn't.
```
```
AddUnitModifier(IdView unitId, string modId)
Adds a modifier to the unit.
Arguments:
IdView unitId - unit ID (unit.id).
string modId - modifier ID.
Returns:
bool - true if successful.
```
```
RemoveUnitModifier(IdView unitId, string modId)
Removes a modifier from the unit.
Arguments:
IdView unitId - unit ID (unit.id).
string modId - modifier ID.
Returns:
bool - true if successful.
```
### Battle functions:
Functions that apply status effects ignore resistance and immunity.
```
GetUnitAttackCount(IdView unitId)
Gets the number of available attacks for the unit in the current round.
Arguments:
IdView unitId - unit ID (unit.id).
Returns:
int - number of attacks. 0 if the unit is not in the current round list.
```
```
GetUnitTurn()
Gets the unit that is currently acting.
Arguments:
none
Returns:
IdView - unit information.
```
```
SetUnitAttackCount(IdView unitId, int value)
Sets the number of possible attacks for the unit.
Arguments:
IdView unitId - unit ID (unit.id).
int value - number of attacks. 0 - the unit will attack indefinitely.
Returns:
bool - true if successful.
```
```
AddUnitModifier(IdView unitId, IdView unitId2, string id)
Gives a unit a modifier. This modifier follows the rules of modifiers applied in combat and will be automatically removed when unitId2's turn begins (usually the one who applied the modifier).
Arguments:
IdView unitId - unit ID (unit.id) that will receive the modifier.
IdView unitId2 - unit ID whose turn will remove the modifier.
string id - modifier ID.
Returns:
bool - true if successful.
```
```
SetHeal(IdView unitId, int value)
Heals the unit. A negative value will deal damage. The unit CANNOT die (technical limitation).
Arguments:
IdView unitId - unit ID (unit.id).
int value - amount of healing received.
Returns:
bool - true if successful.
```
```
SetShatteredArmor(IdView unitId, int value)
Sets the amount of shattered armor. If the value is negative, the unit will increase its armor.
Arguments:
IdView unitId - unit ID (unit.id).
int value - amount of shattered armor. A negative value reduces the effect and increases armor if the value is negative.
Returns:
bool - true if successful.
```
```
SetPoison(IdView unitId, int value, bool isLong)
SetFrostbite(IdView unitId, int value, bool isLong)
SetBlister(IdView unitId, int value, bool isLong)
Applies DOT damage with poison/frost/burn to the unit, respectively.
Arguments:
IdView unitId - unit ID (unit.id).
int value - amount of damage. Damage cannot be below 0 and above 300.
bool isLong - long-lasting effect
Returns:
bool - true if successful.
```
### License
[Detours](https://github.com/microsoft/Detours), [GSL](https://github.com/microsoft/GSL), [fmt](https://github.com/fmtlib/fmt) and [sol2](https://github.com/ThePhD/sol2) submodules as well as [![Lua](https://www.andreas-rozek.de/Lua/Lua-Logo_64x64.png)](http://www.lua.org/license.html) are using their own licenses.


This modification is not made or supported by Strategy First.<br />
Disciples 2 is a trademark of Strategy First Inc.

