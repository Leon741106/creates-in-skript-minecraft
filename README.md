# creates-in-skript-minecraft
Ein erweiterbares Minecraft Crates-Skript. Spieler sammeln Keys, um Crates zu öffnen und Belohnungen wie Diamond-Rüstung, Werkzeuge oder Items zu erhalten. Aktuell ist nur die Classic Crate implementiert, weitere Crates lassen sich leicht hinzufügen.


#commands //giveclassickey [<player>] [<number>]

Gibt dem Spieler eine bestimmte Anzahl Classic Keys.

Berechtigung: admin.givekey

Standardwerte: Spieler = ausführenender Spieler, Anzahl = 1

/mykeys

Zeigt dem Spieler, wie viele Classic Keys er hat.

/givecrateshulker [<player>]

Gibt dem Spieler eine Classic Crate Shulker Box.

Berechtigung: admin.givecrateshulker

Standardwert: Spieler = ausführenender Spieler

/keys

Zeigt die Anzahl der Classic Keys des Spielers an (ähnlich wie /mykeys).

/deleteclassiccrates

Löscht alle Classic Crate Shulker Boxes im Chunk des Spielers.

Berechtigung: admin.deletecrates

/keyallclassic [<number>]

Gibt allen Spielern eine bestimmte Anzahl Classic Keys.

Berechtigung: admin.keyall

Standardwert: Anzahl = 1


Globale Variablen

{create_classic}

Typ: Inventar

Beschreibung: Das Inventar der Classic Crate, das Items enthält, die Spieler beim Öffnen erhalten.

Erweiterung: Neue Crates können durch eigene Inventare wie {create_legendary} hinzugefügt werden.

{keys::%player%::classic}

Typ: Zahl

Beschreibung: Speichert die Anzahl der Classic Keys für jeden Spieler.

Erweiterung: Neue Key-Typen können ähnlich gespeichert werden, z. B. {keys::%player%::legendary}.

{endcrystal}, {obsidian}, {respawnanch}, {glowstone}

Typ: ItemStack

Beschreibung: Temporäre Variablen für stapelbare Items, die in der Crate platziert werden.

Erweiterung: Weitere Items können hinzugefügt werden, z. B. {_netherite} für Netherite Items.

Temporäre Variablen für Items

{_sword}

Typ: ItemStack

Beschreibung: Diamond Sword mit Sharpness 1 und Unbreaking 2 für die Classic Crate.

{_pickaxe}

Typ: ItemStack

Beschreibung: Diamond Pickaxe mit Efficiency 1 und Unbreaking 2 für die Classic Crate.

{_helmet}, {_chestplate}, {_leggings}, {_boots}

Typ: ItemStack

Beschreibung: Diamond-Rüstung mit Protection 1 und Unbreaking 2 für die Classic Crate.

{_shulker}

Typ: ItemStack

Beschreibung: Temporäre Variable für die Shulker Box, die als Classic Crate verteilt wird.

Temporäre Variablen für Befehle

{_target}

Typ: Spieler

Beschreibung: Spieler, der einen Befehl ausführt oder ein Item erhält.

{_amount}

Typ: Zahl

Beschreibung: Menge an Keys oder Items, die durch einen Befehl verteilt werden.

{_count}

Typ: Zahl

Beschreibung: Zählt die Anzahl der entfernten Classic Crates bei /deleteclassiccrates.
