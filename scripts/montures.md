# Montures

Les fonctions liées aux montures se retrouve dans la table : _**mount**_

---

#### hasMount

```lua
bool hasMount()
```

* Indique si vous avez une monture

Exemple:

```lua
if mount.hasMount() then
    printMessage("J'ai une jolie monture") -- J'ai une jolie monture
end
```

---

#### isRiding

```lua
bool isRiding()
```

* Indique si vous êtes sur votre monture

Exemple:

```lua
if mount.isRiding() then
    printMessage("Je suis en train de chevaucher ma monture :p") -- Je suis en train de chevaucher ma monture :p
end
```

---

#### currentRatio

```lua
int currentRatio()
```

* Indique le pourcentage actuel d'expérience donnée à votre monture

Exemple:

```lua
printMessage("Je donne " .. mount.currentRatio() .. "% d'xp à ma monture") -- Je donne 10% d'xp à ma monture
```

---

#### toggleRiding

```lua
void toggleRiding()
```

* Si vous êtes sur votre monture, vous descendez, sinon vous montez dessus.

Exemple:

```lua
mount.toggleRiding()
```

---

#### setRatio

```lua
void setRatio(int ratio)
```

* Défini le pourcentage d'expérience que vous attribuez à votre monture

| Nom | Description |
| :--- | :--- |
| ratio | Pourcentage d'expérience à donner à votre monture, de type int |

Exemple:

```lua
mount.setRatio(20) -- Vous allez désormais donner 20% d'xp à votre monture.
```

---
