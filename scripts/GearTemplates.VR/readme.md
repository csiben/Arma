# Arma 3 Arsenal Gear Templates

**Author:** 	Rafael09ED

**Version:**	1.1

Allows the creation of template soldiers who have their loadout applied to all other units of the same type.

### Installation:

1. Copy the folder "f" to the mission directory
2. Merge the description.ext and initPlayerLocal.sqf files to the mission directory
3. Create a game logic module with the following text in the init:
`sqf
	{   _x disableAI "ANIM";  } forEach synchronizedObjects this;  
	0 = [this] execVM "f\assignGear\f_setLoadoutRoleModel.sqf";
`

4. Sync the game logic to each unit you want to use as a template loadout
5. Set the loadout of each unit synced using the arsenal

Units of the same type as the template units will be created with the same loadout as the templates

### Change Log:

#### 1.1
- Vehicle Cargo Support
- F3 Gear Script Replacement Interface
    
#### 1.0 
- Initial Release
