# Funktionsweise:
Dieses System funktioniert, indem die UUIDs, die Version und der Ordnername des Subpacks übereinstimmen. Das Herzstück liegt in der world_resource_packs.json Datei im Welt-Ordner.

	[
		{
			"pack_id" : "11111111-1111-1111-1111-111111111111",
			"subpack" : "0.0.0.0_Server",
			"version" : [ 1, 0, 0 ]
		}
	]
Dies sind die Werte, auf die Minecraft achtet. Wenn der Benutzer bereits ein Pack hat, das diese Anforderungen erfüllt, lädt Minecraft dieses, anstatt dieses Ressourcen-Pack herunterladen zu wollen.

 Anmerkungen:
* Die Wahl der UUID-Werte basiert auf ihrer leichteren Merkfähigkeit im Vergleich zu zufällig generierten UUIDs.
* Der Subpack-Name setzt sich aus einer Kombination von IP und Servername zusammen, um Doppelungen im System zu vermeiden.
* Die IP kann durch "realm" ersetzt werden, wenn es sich um ein Realm handelt.
# Tutorial für Server und Realms:

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

Hier gibt es nicht viel zu sagen. Der folder_name muss individuell gestaltet werden, ansonsten gelten die Minecraft Ressourcenpack-Regeln.
# Tutorial für Benutzer:

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

Beachte, dass dein Standard-Subpack ganz unten steht. Dies hat sich für mich als angenehm erwiesen, könnte jedoch je nach Situation variieren. Der folder_name sollte auf den Server-folder_name angepasst werden.
# Persönliche Gedanken:
Dieses Tutorial entstand aus einer Idee, die ich persönlich für sehr cool halte. Ich hoffe, dass sich dieses System etabliert und für eine Vielzahl von Anwendungen nützlich wird. Ursprünglich wollte ich "0.0.0.0:Server" verwenden, jedoch akzeptiert das Dateisystem ":" nicht im Namen.

Feedback, Vorschläge und Verbesserungen sind immer willkommen. Dies ist mein erstes Tutorial und ich bin dankbar für jegliche Unterstützung.
