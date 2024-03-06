# Funktionsweise:
Dieses System Funktioniert indem der die UUID's, die Version und der Ordnername das Subpacks übereinstimmen.

Das Geheimnis liegt in der world_resource_packs.json Datei im Welt Ordner:

	[
		{
			"pack_id" : "11111111-1111-1111-1111-111111111111",
			"subpack" : "0.0.0.0_Server",
			"version" : [ 1, 0, 0 ]
		}
	]
Das sind sie Werte auf die Minecraft Achtet. Wenn der User schon ein Pack hat was diese Vorraussetzungen erfüllt, würd Minecraft diese Laden, statt dieses Res-Pack Herrunterladen zu wollen.

 Anmerkungen:
* Ich habe mich für diese UUID Werte endschieden weil sie einfacher zu Merken sind als eine zufällig generierte UUID.
# Tutorial für Server: (und Relams)

	{
		"format_version": 2,
		"header": {
			"description": "Hier kann eine Beschreibung hin",
			"name": "Hier kann ein Name hin",
			"uuid": "11111111-1111-1111-1111-111111111111",
			"version": [ 1,0,0 ],
			"min_engine_version": [ 1,20,0 ]
		},
		"modules": [
			{
				"description": "Hier kann eine Beschreibung hin",
				"type": "resources",
				"uuid": "22222222-2222-2222-2222-222222222222",
				"version": [ 1,0,0 ]
			}
		],
		"subpacks": [
			{
				"folder_name": "0.0.0.0_Server",
				"name": "Server Subpack",
				"memory_tier": 1
			}
		]
	}


# Tutorial für User:

	{
		"format_version": 2,
  	"header": {
    	"description": "Hier kann eine Beschreibung hin",
    	"name": "Hier kann ein Name hin",
    	"uuid": "11111111-1111-1111-1111-111111111111",
			"version": [ 1,0,0 ],
			"min_engine_version": [ 1,20,0 ]
		},
	 	"modules": [
			{
	 			"description": "Hier kann eine Beschreibung hin",
				"type": "resources",
				"uuid": "22222222-2222-2222-2222-222222222222",
				"version": [ 1,0,0 ]
		 	}
		],
	 	"subpacks": [
			{
				"folder_name": "0.0.0.0_Server",
				"name": "Server Rescurcen-Pack",
				"memory_tier": 0
	 		},
	 		{
	 			"folder_name": "Default",
				"name": "Standart Rescurcen-Pack",
	 			"memory_tier": 1
			}
		]
	}
 
# Persönliche Gedanke
Dieses Tutorial endstand aus einer Idee die ich persönlich verdammt cool Finde.
Ich hoffe das sich diese Etabliert und für einen Großraum an Anwendung findet.

Ich wollte eigendlich 0.0.0.0:Server verweden, aber das Dateisystem Akzeptiert ':' nicht im Namen.

Hoffe es hat euch gefallen.
