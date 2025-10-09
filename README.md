# Modding toolset for Disciples 2 [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

### Features:

### BattleMsgDataApi
battle:getUnitAttackCount( unit.id )
return: int Attack Count; 0 if unit not in the turn list.

battle:isUnitTurn( unit.id )
return: bool.

battle:setUnitAttackCount( unit.id, int value )
return: int Attack Count

battle:setHeal( unit.id, int value)

### Versions prior 0.4:
Installation and deinstallation process is the same, but with binkw32.dll.

### Building from sources:
Build Debug or Release Win32 target using Visual Studio solution located in mss32 folder. 

### License
[Detours](https://github.com/microsoft/Detours), [GSL](https://github.com/microsoft/GSL), [fmt](https://github.com/fmtlib/fmt) and [sol2](https://github.com/ThePhD/sol2) submodules as well as [![Lua](https://www.andreas-rozek.de/Lua/Lua-Logo_64x64.png)](http://www.lua.org/license.html) are using their own licenses.


This modification is not made or supported by Strategy First.<br />
Disciples 2 is a trademark of Strategy First Inc.

