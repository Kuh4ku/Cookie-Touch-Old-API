# Personnage

Les fonctions liées au personnage se retrouve dans la table : _**character**_

---

#### isAlive

```lua
bool isAlive()
```

* Indique si votre personnage est en vie

Exemple:

```lua
if character.isAlive() then
    printMessage("Ouf je suis vivant :)") -- Ouf je suis vivant :)
end
```

---

#### isTombstone

```lua
bool isTombstone()
```

* Indique si votre personnage est une tombe

Exemple:

```lua
if character.isTombstone() then
    printMessage("Ahhhhh je suis une tombe :'(") -- Ahhhhh je suis une tombe :'(
end
```

---

#### isPhantom

```lua
bool isPhantom()
```

* Indique si votre personnage est un fantôme

Exemple:

```lua
if character.isPhantom() then
    printMessage("Bouuuuh je suis un fantôme!") -- Bouuuuh je suis un fantôme!
end
```

---

#### name

```lua
string name()
```

* Vous donne le nom de votre personnage

Exemple:

```lua
printMessage("Je m'appelle " .. character.name()) -- Je m'appelle Bledart
```

---

#### level

```lua
byte level()
```

* Vous donne le niveau de votre personnage

Exemple:

```lua
printMessage("Je suis niveau " .. character.level()) -- Je suis niveau 180
```

---

#### sex

```lua
bool sex()
```

* Vous donne le sexe de votre personnage

Exemple:

```lua
if character.sex() then
    printMessage("Je suis une fille") -- Je suis une fille
else
    printMessage("Je suis un garçon") -- Je suis un garçon
end
```

---

#### lifePoints

```lua
int lifePoints()
```

* Vous donne vos points de vie

Exemple:

```lua
printMessage("J'ai " .. character.lifePoints() .. " PDV") -- J'ai 3455 PDV
```

---

#### maxLifePoints

```lua
int maxLifePoints()
```

* Vous donne vos points de vie maximum

Exemple:

```lua
printMessage("J'ai " .. character.maxLifePoints() .. " PDV Maximum") -- J'ai 4800 PDV Maximum
```

---

#### lifePointsP

```lua
int lifePointsP()
```

* Vous donne le pourcentage de vos points de vie

Exemple:

```lua
printMessage("J'ai " .. character.lifePointsP() .. "% PDV") -- J'ai 65% PDV
```

---

#### experience

```lua
int experience()
```

* Vous donne vos points d'experience

Exemple:

```lua
printMessage("J'ai " .. character.experience() .. " XP") -- J'ai 7126 XP
```

---

#### energyPoints

```lua
int energyPoints()
```

* Vous donne vos points d'energie

Exemple:

```lua
printMessage("J'ai " .. character.energyPoints() .. " points d'énergie") -- J'ai 7500 points d'énergie
```

---

#### maxEnergyPoints

```lua
int maxEnergyPoints()
```

* Vous donne vos points d'énergie maximum

Exemple:

```lua
printMessage("J'ai " .. character.maxEnergyPoints() .. " points d'énergie maximum") -- J'ai 10000 points d'énergie maximum
```

---

#### energyPointsP

```lua
int energyPointsP()
```

* Vous donne votre pourcentage d'énergie

Exemple:

```lua
printMessage("J'ai " .. character.energyPointsP() .. "% d'énergie") -- J'ai 80% d'énergie
```

---

#### kamas

```lua
int kamas()
```

* Vous donne votre nombre de kamas

Exemple:

```lua
printMessage("J'ai " .. character.kamas() .. " kamas") -- J'ai 10 kamas
```

---

#### sit

```lua
void sit()
```

* Fait assoir votre personnage pour regagner vos points de vie plus rapidement

Exemple:

```lua
character.sit()
```

---

#### freeSoul

```lua
void freeSoul()
```

* Libère votre personnage s'il est en tombe

Exemple:

```lua
character.freeSoul()
```

---
