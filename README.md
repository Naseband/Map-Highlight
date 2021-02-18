# Map Highlighting Include

  With this include you can highlight areas on the ingame map.
  4 GangZones will quickly expand from the specified location, creating a ping effect.
  This ping effect can be customized, you can change the speed, distance, width, color, direction and delay.
  Since GangZones cannot actually be moved, the script repeatedly creates and destroys them to create a similar effect.
  In the current version only global GangZones are supported.

# Functions

  CreateMapHighlight(Float:x, Float:y, color, Float:distance, Float:width, interval, direction, max_steps, pause_time, playerid)

  x, y: 		the 2D position of the center
  color: 		RGBA color
  distance:		distance in m which the ping will travel
  width: 		the width of the zones in m
  interval: 	interval in ms in which the zones will be updated
  direction: 	positive values will move the zones away from the center, negative values will move them towards the center
  max_steps:	the total number of steps the zones will take (they travel 1 step per interval)
  pause_time: 	delay in ms for which the animation will pause after completing one iteration, 0 for none
  playerid: 	the PlayerID for which the zones will show, -1 for all players
  returns: 		ID of the MapHighlight, -1 if no free slot was found

  DestroyMapHighlight(mhlid)

  mhlid: 		the ID of the MapHighlight to destroy
  returns: 		1 if it was valid, 0 if not

  IsValidMapHighlight(mhlid)

  mhlid: 		the ID of the MapHighlight
  returns: 		1 if it is valid, 0 if not

  SetMapHighlightPlayerID(mhlid, playerid)

  mhlid:		the ID to set the PlayerID of
  playerid:		the PlayerID to show the zones to, -1 for all players
