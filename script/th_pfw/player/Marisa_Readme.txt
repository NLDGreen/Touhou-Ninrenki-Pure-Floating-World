To use the power system, go to the file for the shot you want to use it with.

The file is one of these:
Reimu_A.txt
Reimu_B.txt
Reimu_C.txt

In @Initialize, you should see this:
	
	LoadPlayerShotData(GetCurrentScriptDirectory ~ "ShotData.txt");
	ObjPlayer_AddIntersectionCircleA1(playerObject, 0, 0, 2, 20);
	
	SetPlayerAutoItemCollectLine(160);
	SetPlayerSpeed(4, 2);
	
>>> powerEnabled = false;
	shotType = 1;
	
	LoadSounds;
	
	DrawSprite;
	DrawHitbox;
	
	CreateShots;
	CreateOptions;

Change "powerEnabled = false" to "powerEnabled = true".
	
	LoadPlayerShotData(GetCurrentScriptDirectory ~ "ShotData.txt");
	ObjPlayer_AddIntersectionCircleA1(playerObject, 0, 0, 2, 20);
	
	SetPlayerAutoItemCollectLine(160);
	SetPlayerSpeed(4, 2);
	
>>> powerEnabled = true;
	shotType = 1;
	
	LoadSounds;
	
	DrawSprite;
	DrawHitbox;
	
	CreateShots;
	CreateOptions;

The power system is now enabled on that shot type. You can also copy the entire file and change that in the copy,
so you can have both power enabled and disabled players on the selection screen in-game.

If you want to disable the power system, change "powerEnabled" back to false.





Orrerries Sun

This spell replaces the player's options for 20 seconds. Options will return to normal if the player is killed.