# LeaveMyBaseAlone Info
****Put the mod into your client to effect structures****
v1.1.1 Still some nullref errors but they dont effect the mod. Repair tool only effects other players structures if you're permitted. 
Ward sets hp over a radius. Removed HP automatically setting on Misc objects, but repair tool can still set hp on them if you wish.
HP is set upon placing an object, not globally anymore; Alternatively you can use the hammer on preexisting structures to modify the health as well.
There is now an option to enable/disable resources being consumed upon building a structure. As well as a option to turn on/off mod notification; In the config.
This mod is a fix to Griefing on public servers. 
It sets structure HP to a specified value from config. 
Saving the server will then persistantly save the structures hp's for anyone one else who joins, even on server stop/start.

# code

```cs
//get actual structure object from client and set health
 hview.GetZDO().Set("health", m_Structure.Value); 
//hardcode monsters targetting to remove player bases.
   m_monsterTargetRayMask = LayerMask.GetMask(new string[]
            {
             "Default",
             "static_solid",
             "Default_small",
            "vehicle"
            });
```