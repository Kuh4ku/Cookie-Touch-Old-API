# Echanges

Les fonctions liées aux échanges se retrouve dans la table : _**exchange**_

---

#### weightP

```lua
int weightP()
```

* Indique votre pourcentage de pods durant l'échange

Exemple:

```lua
printMessage("J'ai " .. exchange.weightP() .. "% de pods.") -- J'ai 20% de pods.
```

---

#### targetWeightP

```lua
int targetWeightP()
```

* Indique le pourcentage de pods durant l'échange de votre correspondant

Exemple:

```lua
printMessage("Il a " .. exchange.targetWeightP() .. "% de pods.") -- Il a 36% de pods.
```

---

#### startExchange

```lua
void startExchange(int playerId)
```

* Lance un échange avec le joueur de votre choix

| Nom | Description |
| :--- | :--- |
| playerId | ID du joueur à qui vous voulez lancer l'échange, de type int |

Exemple:

```lua
exchange.startExchange(82736423)
```

---

#### sendReady

```lua
void sendReady()
```

* Accepte l'échange

Exemple:

```lua
exchange.sendReady()
```

---

#### putItem

```lua
void putItem(int gid, int quantity)
```

* Met un item dans l'échange

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |
| quantity | Quantité de l'item à mettre dans l'échange, de type int |

Exemple:

```lua
exchange.putItem(548, 10) -- Met 10 potions de rappel dans l'échange
```

---

#### putAllItems

```lua
void putAllItems()
```

* Met tous les objets échangeables disponibles dans l'échange.

Exemple:

```lua
exchange.putAllItems()
```

---

#### removeItem

```lua
void removeItem(int gid, int quantity)
```

* Enlève un item de l'échange

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |
| quantity | Quantité de l'item à enlever de l'échange, de type int |

Exemple:

```lua
exchange.removeItem(548, 10) -- Enlève les 10 potions de rappel de l'échange
```

---

#### putKamas

```lua
void putKamas(int quantity)
```

* Rajoute des kamas dans l'échange

| Nom | Description |
| :--- | :--- |
| quantity | Quantité de kamas à mettre dans l'échange, de type int |

Exemple:

```lua
exchange.putKamas(10000) -- Met 10000 kamas dans l'échange
```

---

#### removeKamas

```lua
void removeKamas(int quantity)
```

* Enlève des kamas dans l'échange

| Nom | Description |
| :--- | :--- |
| quantity | Quantité de kamas à retirer de l'échange, de type int |

Exemple:

```lua
exchange.removeKamas(2000) -- Enlève 2000 kamas de l'échange
```

---
