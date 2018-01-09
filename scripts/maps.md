# Map

Vous pouvez utiliser les fonctions map sans aucuns préfix.

---

#### saveZaap

```lua
void saveZaap()
```

* Enregistre le zaap de la map actuelle comme point de sauvegarde. C'est-à-dire que pour chaque utilisation de potion de rappel ou chaque combat perdu (à condition de pas être transformé en fantôme) vous retourneriez à ce zaap.

Exemple:

```lua
saveZaap()
```

---

#### useZaap

```lua
void useZaap(int destinationMapId)
```

* Utilise de le zaap de la map actuelle pour aller sur le zaap de la map qui a pour id : destinationMapId

Exemple:

```lua
useZaap(76761289372) -- Vous prenez le zaap pour aller au zaap d'astrub
```

---

#### useZaapi

```lua
void useZaapi(int destinationMapId)
```

* Utilise de le zaapi de la map actuelle pour aller sur le zaapi de la map qui a pour id : destinationMapId

Exemple:

```lua
useZaapi(767612893)
```

---

#### useLockedHouse

```lua
void useLockedHouse(int cellId, string code)
```

* Entre dans la maison où la porte se situe sur la cellule "cellId" avec pour code "code"

Exemple:

```lua
useLockedHouse(345, "123456") -- Entre dans la maison avec la porte en cellule 345 qui a pour code 123456
```

---

#### useLockedStorage

```lua
void useLockedStorage(int cellId, string code)
```

* Ouvre le coffre en cellule "cellId" qui a pour code "code"

Exemple:

```lua
 useLockedStorage(220, "654321") -- Ouvre coffre en cellule 345 qui a pour code 654321
```

---

#### moveToCell

```lua
void moveToCell(int cellId)
```

* Déplace votre personnage de cellule

| Nom | Description |
| :--- | :--- |
| cellId | ID de la cellule d'arrivée. Entre 1 et 550,  de type int |

Exemple:

```lua
moveToCell(300) -- Déplace mon personnage sur la cellule 300
```

---

#### useById

```lua
void useById(int elementId, int skillInstanceUid = -1)
```

* Utilise un élément sur la map selon son ID

| Nom | Description |
| :--- | :--- |
| elementId | ID de l'élement à utiliser, de type int |
| skillInstanceUid | [Facultatif] UID du skill, par défaut: -1, de type int |

Exemple:

```lua
useById(10)
```

---

#### use

```lua
void use(int elementCellId, int skillInstanceUid = -1)
```

* Utilise un élément sur la map selon sa cellule

| Nom | Description |
| :--- | :--- |
| elementCellId | ID de la cellule où l'élement à utiliser est positionné, de type int |
| skillInstanceUid | [Facultatif] UID du skill, par défaut: -1, de type int |

Exemple:

```lua
use(200) -- Utilise l'élément sur la cellule 200
```

---

#### onCell

```lua
bool onCell(int cellId)
```

* Indique si votre personnage est sur une cellule

| Nom | Description |
| :--- | :--- |
| cellId | ID de la cellule, entre 1 et 550, de type int |

Exemple:

```lua
if onCell(200) then
    printMessage("Je suis sur la cellule 200") -- Je suis sur la cellule 200
else
    printMessage("Je ne suis pas sur la cellule 200") -- Je ne suis pas sur la cellule 200
end
```

---

#### joinFriend

```lua
void joinFriend(string name)
```

* Rejoins votre amis, à condition que vous soyez tous les deux sur Incarnam.

Exemple:

```lua
joinFriend("MonCopain")
```

---

#### changeMap

```lua
void changeMap(string direction)
```

* Change de map vers la direction "direction"

Exemples:

```lua
changeMap("bottom") -- Change de map vers le bas
```

---

#### waitMapChange

```lua
void waitMapChange(int delay = 5000)
```

* Attend le changement de map avec un délai

| Nom | Description |
| :--- | :--- |
| delay | [Facultatif] Nombre de millisecondes à attendre, par défaut: 5000, de type int |

Exemples:

```lua
waitMapChange() -- Attend 5 secondes le changement de la map
```

```lua
waitMapChange(7000) -- Attend 7 secondes le changement de la map
```

---

#### area

```lua
string area()
```

* Donne votre zone actuelle

Exemple:

```lua
printMessage("Je suis dans la zone: " .. area()) -- Je suis dans la zone: Amakna
```

---

#### subArea

```lua
string subArea()
```

* Donne votre sous zone actuelle

Exemple:

```lua
printMessage("Je suis dans la sous zone: " .. subArea()) -- Je suis dans la sous zone: Amakna - Kanojedo
```

---

#### currentPos

```lua
string currentPos()
```

* Donne votre position actuelle

Exemple:

```lua
printMessage("Je suis en " .. currentPos()) -- Je suis en 4,-19
```

---

#### currentMapId

```lua
string currentMapId()
```

* Donne votre map actuelle

Exemple:

```lua
printMessage("Je suis sur la map " .. currentMapId()) -- Je suis sur la map 233223
```

---

#### onMap

```lua
bool onMap(string coords)
```

* Indique si votre personnage est sur une map

| Nom | Description |
| :--- | :--- |
| coords | Coordonnées de la map, peut etre l'id ou la position, de type string |

Exemples:

```lua
if onMap("200") then
    printMessage("Je suis sur la map 200") -- Je suis sur la map 200
else
    printMessage("Je ne suis pas sur la map 200") -- Je ne suis pas sur la map 200
```

```lua
if onMap("-4,18") then
    printMessage("Je suis en -4,18") -- Je suis en -4,18
else
    printMessage("Je ne suis pas en -4,18") -- Je ne suis pas en -4,18
end
```

---

#### canFight

```lua
bool canFight(int[] forbiddenMonsters = nil, int[] mandatoryMonsters = nil, int minMonsters = 1, int maxMonsters = 8, int minMonstersLevel = 1, int maxMonstersLevel = 1000)
```

* Dis si vous pouvez lancer un combat sur la map actuelle selon les conditions.

| Nom | Description |
| :--- | :--- |
| forbiddenMonsters | [Facultatif] ID des monstres interdits, par défaut: nil, de type int[] |
| mandatoryMonsters | [Facultatif] ID des monstres obligatoires, par défaut: nil, de type int[] |
| minMonsters | [Facultatif] Nombre minimum de monstres requis, par défaut: 1, de type int |
| maxMonsters | [Facultatif] Nombre maximum de monstres requis, par défaut: 8, de type int |
| minMonstersLevel | [Facultatif] Nombre minimum requis pour le level du groupe, par défaut: 1, de type int |
| maxMonstersLevel | [Facultatif] Nombre maximum requis pour le level du groupe, par défaut: 1000, de type int |

Exemples:

```lua
if canFight() then
    printMessage("Je peut combattre ici") -- Je peut combattre ici
else
    printMessage("Je ne peut pas combattre") -- Je ne p
end
```

---

#### fight

```lua
void fight(int[] forbiddenMonsters = nil, int[] mandatoryMonsters = nil, int minMonsters = 1, int maxMonsters = 8, int minMonstersLevel = 1, int maxMonstersLevel = 1000)
```

* Lance un combat sur la map actuelle selon les conditions.

| Nom | Description |
| :--- | :--- |
| forbiddenMonsters | [Facultatif] ID des monstres interdits, par défaut: nil, de type int[] |
| mandatoryMonsters | [Facultatif] ID des monstres obligatoires, par défaut: nil, de type int[] |
| minMonsters | [Facultatif] Nombre minimum de monstres requis, par défaut: 1, de type int |
| maxMonsters | [Facultatif] Nombre maximum de monstres requis, par défaut: 8, de type int |
| minMonstersLevel | [Facultatif] Nombre minimum requis pour le level du groupe, par défaut: 1, de type int |
| maxMonstersLevel | [Facultatif] Nombre maximum requis pour le level du groupe, par défaut: 1000, de type int |

Exemples:

```lua
fight() -- Lance un combat
```

---
