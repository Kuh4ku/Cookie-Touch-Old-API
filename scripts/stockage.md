# Stockage

Les fonctions liées aux coffres se retrouve dans la table : _**storage**_

Ces fonctions peuvent servir aussi bien que pour les coffres en tout genre que pour la banque.

---

#### itemCount

```lua
int itemCount(int gid)
```

* Donne la quantité de cet item présent dans le coffre

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |

Exemple:

```lua
printMessage("J'ai " .. storage.itemCount(548) .. " potions dans mon coffre") -- J'ai 10 potions dans mon coffre
```

---

#### kamas

```lua
int kamas()
```

* Donne la quantité de kamas présent dans le coffre

Exemple:

```lua
printMessage("J'ai " .. storage.kamas() .. " kamas dans le coffre") -- J'ai 100 kamas dans le coffre
```

---

#### putItem

```lua
void putItem(int gid, int quantity)
```

* Met un item dans le coffre

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |
| quantity | Quantité à mettre dans le coffre, de type int |

Exemple:

```lua
storage.putItem(548, 3) -- Met 3 potions de rappel dans votre coffre
```

---

#### getItem

```lua
void getItem(int gid, int quantity)
```

* Reprend un item du coffre

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |
| quantity | Quantité à reprendre du coffre, de type int |

Exemple:

```lua
storage.getItem(548, 3) -- Reprend 3 potions de rappel de votre coffre
```

---

#### putKamas

```lua
void putKamas(int quantity)
```

* Met des kamas dans le coffre

| Nom | Description |
| :--- | :--- |
| quantity | Quantité de kamas à mettre dans le coffre, de type int |

Exemple:

```lua
storage.putKamas(5000) -- Met 5000 kamas dans votre coffre
```

---

#### getKamas

```lua
void getKamas(int quantity)
```

* Reprend des kamas du coffre

| Nom | Description |
| :--- | :--- |
| quantity | Quantité de kamas à prendre dans le coffre, de type int |

Exemple:

```lua
storage.getKamas(1000) -- Reprend 1000 kamas dans le coffre
```

---

#### putAllItems

```lua
void putAllItems()
```

* Dépose tous vos objets dans le coffre

Exemple:

```lua
storage.putAllItems()
```

---

#### getAllItems

```lua
void getAllItems()
```

* Reprend tous vos objets du coffre

Exemple:

```lua
storage.getAllItems()
```

---

#### putExistingItems

```lua
void putExistingItems()
```

* Dépose dans le coffre les objets que vous avez dans votre inventaire et qui sont déjà présent dans le coffre

Exemple:

```lua
storage.putExistingItems()
```

---

#### getExistingItems

```lua
void getExistingItems()
```

* Reprend de votre coffre tous les objets que vous possédez déjà dans votre inventaire

Exemple:

```lua
storage.getExistingItems()
```

---
