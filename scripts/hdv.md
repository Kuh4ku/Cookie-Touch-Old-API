# HDV

Les fonctions liées à l'hdv se retrouve dans la table : _**bid**_

---

#### startBuying

```lua
void startBuying()
```

* Ouvre l'hotel des ventes en mode Achat.

Exemple:

```lua
bid.startBuying()
if isInDialog() then
    printMessage("HDV ouvert !")
end
```

---

#### getItemPrice

```lua
int getItemPrice(int gid, int lot)
```

* Donne le prix d'un item selon le lot choisit \(1, 10, 100\)

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |
| lot | lot de l'objet (1, 10, 100), de type int |

Exemple:

```lua
price = bid.getItemPrice(548, 10)
printMessage("OMG, ça coûte " .. price .. " kamas.") -- OMG, ça coûte 10 kamas.
```

---

#### buyItem

```lua
void buyItem(int gid, int lot)
```

* Achète un item dans l'hotel des ventes selon le lot choisit \(1, 10, 100\)

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |
| lot | lot de l'objet (1, 10, 100), de type int |

Exemple:

```lua
bid.buyItem(548, 10) -- Vous achetez donc ici 10 potions de rappel
```

---

#### itemsInSaleCount

```lua
int itemsInSaleCount()
```

* Donne le nombre de lots que vous avez en vente

Exemple:

```lua
printMessage("Vous avez " .. bid.itemsInSaleCount() .. " lots en vente.")
```

---

#### getItemsInSale

```lua
ObjectInSale[] getItemsInSale()
```

* Donne une liste des objets que vous avez en vente

Exemple:

```lua
for k,v in pairs(bid.getItemsInSale()) do
    printMessage("GID: " .. v.GID) -- GID: 548
    printMessage("UID: " .. v.UID) -- UID: 182617
    printMessage("Lot: " .. v.Lot) -- Lot: 10
    printMessage("Quantité: " .. v.Quantity) -- Quantité: 3
end
```

---

#### sellItem

```lua
void sellItem(int gid, int lot, int price)
```

* Met un item en vente selon le lot choisit \(1, 10, 100\) et le prix

| Nom | Description |
| :--- | :--- |
| gid | ID de l'item, de type int |
| lot | lot de l'objet (1, 10, 100), de type int |
| price | prix de l'objet à vendre, de type int |

Exemple:

```lua
bid.sellItem(548, 10, 8000) -- Vous vendez ici 10 potions de rappel au prix de 8000 kamas
```

---

#### removeItemInSale

```lua
void removeItemInSale(int uid)
```

* Retire un item de l'hotel des ventes.

| Nom | Description |
| :--- | :--- |
| uid | UID de l'item, de type int |

Exemple:

```lua
bid.removeItemInSale(182617) -- Vous retirez ici vos potions de rappel
```

---

#### editItemInSalePrice

```lua
void editItemInSalePrice(int uid, int newPrice)
```

* Modifie le prix d'un de vos objets présent dans l'hotel des ventes

| Nom | Description |
| :--- | :--- |
| uid | UID de l'item, de type int |
| newPrice | Nouveau prix de l'item, de type int |

Exemple:

```lua
bid.editItemInSalePrice(182617, 9000) -- Vous mettez a jour pour 9000 kamas.
```

---
