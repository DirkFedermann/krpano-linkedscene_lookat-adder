# krpano-linkedscene_lookat-adder
In the krpano version 1.21.2 (build 2023-12-11) there is a bug, that with existing (older) vtours with hotspots that **DO NOT** have the `linkedscene_lookat` attribute the feature of adding a "Target Startup View" to existing hotspots is not working correctly.

It seems like krpano only wants to edit the value, but does not check if it is part of the hotspot and does not add it when it is not there.

This Adder adds a `linkedscene_lookat` to all hotspots.

## Example
From this:
```xml
<hotspot name="spot1" style="skin_hotspotstyle" ath="-177.049" atv="0.446" linkedscene="location002" />
```
to this:
```xml
<hotspot name="spot1" style="skin_hotspotstyle" ath="-177.049" atv="0.446" linkedscene="location002" linkedscene_lookat="0.0,0.0,120.0" />
```
