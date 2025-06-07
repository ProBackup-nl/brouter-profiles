# Touristic profile for velomobiles
## Contributed by Jockel Hofmann, based on "Rennrad - wenig Verkehr"
  - vermeidet viel stärker Höhenmeter, 
  - wählt bergauf kleinere, bergab größere Straßen
  - bergab, Abbiegen teuer
  - folgt auch durchgehenden, asphaltierten Radrouten @ https://www.velomobilforum.de/forum/index.php?threads/brouter-ein-konfigurierbarer-offline-streckenrouter-web-android.38274/post-1544915
## Referenzrouten DE:
 - https://bikerouter.de/#map=12/50.0011/8.0592/standard,Smoothness&lonlats=7.850075,50.009051;8.278885,50.007517&profile=vm-forum-velomobil-touristisch
 - https://bikerouter.de/#map=11/50.0541/8.5419/standard,Smoothness&lonlats=8.773527,50.107535;8.31459,49.997151&profile=vm-forum-velomobil-touristisch
## Enhancements by C. Jacobs (for NL):
 - higher turning cost, except for `roundabout`|`bridge`|`tunnel`|`primary`|`secondary`|`tertiary`
 - no penaly for `concrete` surface
 - penalties for velomobile annoyances like: stop signs, `give_way`, `traffic calming`, `barrier`s, elevator, short oneway cyclepaths on bridges, ...
 - honour direction of `give_way`, stop and traffic signs
 - lower penalty for `give_way` on cycle paths
 - extra (driver safety) penalty for short `sett`|`cobblestone` ways, ...
 - penalty for flat primary|secondary roads where `maxspeed`=80 and `use_sidepath`
 - `primary` at 50 km/h given cost equal to `secondary`
 - lower flatspeedpenalty for 30/40/50 km/h, higher for 90/100 km/h
 - higher cost for `cobblestone`|`sett` surfaces
 - default cost for `unknown` `smoothness` and a lower differentiated cost for `excellent`|`very_good`|`good`
 - penalty for bad ways `class:bicycle=-2` ; and near impassable `class:bicycle=-3`
 - extra penalty for `uncontrolled` `crossing`s on cycleways (don't like crossings on cycleways, especially in parallel to 30/40/50/60 km/h main roads, often bad sight)
## Route not good?
 1. check Tab (press keyboard `T` key to open), route data (press `shift`+`T` to cycle through the tabs)
 2. check [osm.org](https://www.openstreetmap.org/) that ways and nodes are marked correct
    often:
    - `give_way`, stop signs, `traffic_calming`, `surface`, `smoothness` are not tagged
    - after an edit, wait a night (up to 12 hours) for bikerouter.de to update osm tags, and recalculate ( `r` key, twice)
 4. file an issue at github, include 2 bikerouter links:
    1. to only the route part that you don't like, and
    2. a link with extra route point added so the route follows your intended route for the part of link #1
