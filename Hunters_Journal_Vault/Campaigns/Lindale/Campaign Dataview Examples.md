# Campaign Dataview (Examples)

## NPCs by Faction
```dataview
TABLE role, file.link AS "NPC"
FROM "Campaigns/Blood on the Strand/Entities/NPCs"
WHERE faction
GROUP BY faction
SORT faction ASC
```

## Characters by Creed/Drive
```dataview
TABLE creed, drive, file.link AS "Character"
FROM "Campaigns/Blood on the Strand/Entities/Characters"
WHERE creed
SORT creed ASC
```

## Case Files (Open)
```dataview
TABLE status, priority, last_update, file.link
FROM "Campaigns/Blood on the Strand/Case Files"
WHERE status = "Open"
SORT priority DESC, last_update DESC
```
