To use the power system, go to this file:
Youmu.txt

In @Initialize, you should see this:
	
	LoadPlayerShotData(GetCurrentScriptDirectory ~ "ShotData.txt");
	ObjPlayer_AddIntersectionCircleA1(playerObject, 0, 0, 2, 20);
	
	SetPlayerAutoItemCollectLine(140);
	SetPlayerSpeed(5, 2);
	
  >>>   powerEnabled = false;
	
	LoadSounds;
	
	DrawSprite;
	DrawHitbox;
	
	CreateShots;
	CreateOptions;

Change "powerEnabled = false" to "powerEnabled = true".
	
	LoadPlayerShotData(GetCurrentScriptDirectory ~ "ShotData.txt");
	ObjPlayer_AddIntersectionCircleA1(playerObject, 0, 0, 2, 20);
	
	SetPlayerAutoItemCollectLine(140);
	SetPlayerSpeed(5, 2);
	
  >>>  powerEnabled = true;
	
	LoadSounds;
	
	DrawSprite;
	DrawHitbox;
	
	CreateShots;
	CreateOptions;

The power system is now enabled on that shot type. You can also copy the entire file and change that in the copy,
so you can have both power enabled and disabled players on the selection screen in-game.

If you want to disable the power system, change "powerEnabled" back to false.