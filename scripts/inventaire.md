# Inventaire

Les fonctions liées à l'inventaire se retrouve dans la table : _**inventory**_

---

#### pods

```lua
int pods()
```

* Indique votre nombre de pods

Exemple:

```lua
printMessage("J'ai " .. inventory.pods() .. " pods.") -- J'ai 800 pods
```

---

#### podsMax

```lua
int podsMax()
```

* Indique votre nombre de pods maximum

Exemple:

```lua
printMessage("J'ai " .. inventory.podsMax() .. " pods maximum") -- J'ai 1000 pods maximum
```

---

#### podsP

```lua
int podsP()
```

* Indique votre pourcentage de pods

Exemple:

```lua
printMessage("J'ai " .. inventory.podsP() .. "% pods.") -- J'ai 55% de pods.
```

---

#### itemCount

```lua
int itemCount(int gid)
```

* Indique la quantité présente dans votre inventaire de l'objet spécifié

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |

Exemple:

```lua
printMessage("J'ai " .. inventory.itemCount(548) .. " potions de rappel.") -- J'ai 10 potions de rappel.
```

---

#### itemWeight

```lua
int itemWeight(int gid)
```

* Indique le nombre de pods de l'item spécifié

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |

Exemple:

```lua
printMessage(inventory.itemWeight(548) .. " pods.") -- 2 pods.
```

---

#### useItem

```lua
void useItem(int gid, int quantity = 1)
```

* Utilise l'item spécifié. Si vous n'indiquez pas de quantité, le bot utilisera un seul objet.

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |
| quantity | [Facultatif] Quantité à utiliser, par défaut: 1, de type int |

Exemples:

```lua
inventory.useItem(548) -- Utilise une potion de rappel
```

```lua
inventory.useItem(548, 3) -- Utilise 3 potions de rappel (Oui aucun intérêt xD)
```

---

#### equipItem

```lua
void equipItem(int gid)
```

* Equipe l'item indiqué sur votre personnage

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |

Exemple:

```lua
inventory.equipItem(10)
```

---

#### unEquipItem

```lua
void unEquipItem(int gid)
```

* Déséquipe l'item indiqué de votre personnage

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |

Exemple:

```lua
inventory.unEquipItem(10)
```

---

#### dropItem

```lua
void dropItem(int gid, int quantity = 1)
```

* Jette un, ou plusieurs, item\(s\) au sol.

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |
| quantity | [Facultatif] Quantité à jeter, par défaut: 1, de type int |

Exemples:

```lua
inventory.dropItem(548) -- Jette une potion de rappel au sol
```

```lua
inventory.dropItem(548, 2) -- Jette 2 potions de rappel au sol
```

---

#### deleteItem

```lua
void deleteItem(int gid, int quantity = 1)
```

* Supprime un, ou plusieurs, item\(s\)

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |
| quantity | [Facultatif] Quantité à supprimer, par défaut: 1, de type int |

Exemples:

```lua
inventory.deleteItem(548) -- Supprime une potion de rappel
```

```lua
inventory.deleteItem(548, 2) -- Supprime 2 potions de rappel
```

---
