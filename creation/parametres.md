# Paramètres

Pour chacun de vos scripts, vous avez la possibilité de définir vos propres paramètres.
Nous allons découvrir les paramètres disponibles, ici, en détails.

---

#### DISPLAY_FIGHT_COUNT

* Permet d'afficher, oui ou non, le nombre de combats effectués dans la console.
* Défaut: false

Exemple:

```lua
DISPLAY_FIGHT_COUNT = true -- Ici le nombre de combats s'affichera.
```

---

#### DISPLAY_GATHER_COUNT

* Permet d'afficher, oui ou non, le nombre de récoltes effectués dans la console.
* Défaut: false

Exemple:

```lua
DISPLAY_GATHER_COUNT = false -- Ici le nombre de récoltes ne s'affichera pas.
```

---

#### MAX_PODS

* Défini la valeur maximum de pods, en pourcentage, avant l'auto delete et/ou le retour en banque.
* Défaut: 90

Exemple:

```lua
MAX_PODS = 80
```

---

#### AUTO_DELETE

* Ids des objets à supprimer une fois MAX_PODS atteint.
* Défaut: null

Exemple:

```lua
AUTO_DELETE = { 541, 38 } -- Supprimera toutes vos potions de rappels, et vos blés.
```

---

#### AUTO_REGEN

* Ids des objets à utiliser pour la régénération des points de vie.
* Défaut: null

Exemple:

```lua
AUTO_REGEN = { 468, 528 } -- Utilisera Pain d'Amakna & Pain au Blé Complet (DANS CET ORDRE)
```

---

#### OPEN_BAGS

* Permet d'ouvrir les sacs de récoltes automatiquement.
* Défaut: false

Exemple:

```lua
AUTO_REGEN = true -- Activera l'ouverture automatique des sacs
```

---

#### ELEMENTS_TO_GATHER

* Défini les éléments à récolter.
* Défaut: null

Exemple:

```lua
ELEMENTS_TO_GATHER = { 423, 425 } -- Récoltera du Lin et du Chanvre
```

---

#### MIN_MONSTERS

* Défini le minimum de monstres par combat
* Défaut: 1

Exemple:

```lua
MIN_MONSTERS = 2 -- Le bot lanceras des combats de 2 monstres minimum
```

---

#### MAX_MONSTERS

* Défini le maximum de monstres par combat
* Défaut: 8

Exemple:

```lua
MAX_MONSTERS = 4 -- Le bot lanceras des combats de 4 monstres maximum
```

---

#### MAX_FIGHTS_PER_MAP

* Défini le maximum de combat par map
* Défaut: -1 (On peut faire autant de combats qu'on souhaite)

Exemple:

```lua
MAX_FIGHTS_PER_MAP = 10 -- Le bot feras maximum 10 combats sur chaque map
```

---

#### MIN_MONSTERS_LEVEL

* Défini le level minimum du groupe de monstres par combat
* Défaut: 1

Exemple:

```lua
MIN_MONSTERS_LEVEL = 100 -- Le bot lanceras des combats contre des groupes de niveaux 100 minimum
```

---

#### MAX_MONSTERS_LEVEL

* Défini le level maximum du groupe de monstres par combat
* Défaut: 1000

Exemple:

```lua
MAX_MONSTERS_LEVEL = 300 -- Le bot lanceras des combats contre des groupes de niveaux 300 maximum
```

---

#### FORBIDDEN_MONSTERS

* Défini les monstres à éviter pour les combats.
* Défaut: null

Exemple:

```lua
FORBIDDEN_MONSTERS = { 61, 63 } -- Le bot ne lanceras pas des combats contre des groupes contenant des Moskito ou des Crabes
```

---

#### MANDATORY_MONSTERS

* Défini les monstres à avoir absolument pour les combats.
* Défaut: null

Exemple:

```lua
MANDATORY_MONSTERS = { 489, 490 } -- Le bot lanceras des combats seulement contre des groupes contenant des Piou Rouge ET des Piou Vert
```

---

#### BANK_PUT_ITEMS

* Défini les objects à mettre en banque ainsi que leurs quantités.
* Défaut: null

Exemple:

```lua
BANK_PUT_ITEMS = {
    { item = 541, quantity = 1 },
} -- Le bot poseras en banque une potion de rappel
```

---

#### BANK_GET_ITEMS

* Défini les objects à récupérer en banque ainsi que leurs quantités.
* Défaut: null

Exemple:

```lua
BANK_GET_ITEMS = {
    { item = 541, quantity = 1 },
} -- Le bot récuperera en banque une potion de rappel
```

---

#### BANK_PUT_KAMAS

* Défini le nombre de kamas à mettre en banque.
* Défaut: -1 (On ne met pas ses kamas en banque)

Exemples:

```lua
BANK_PUT_KAMAS = 2000 -- Ici on met 2000 kamas en banque.
```

```lua
BANK_PUT_KAMAS = 0 -- Ici on met tous ses kamas en banque (-1 étant pour ignorer le paramètre)
```
---

#### BANK_GET_KAMAS

* Défini le nombre de kamas à récupérer en banque.
* Défaut: -1 (On ne met récupère pas ses kamas en banque)

Exemples:

```lua
BANK_GET_KAMAS = 3000 -- Ici on récupère 3000 kamas en banque.
```

```lua
BANK_GET_KAMAS = 0 -- Ici on récupère tous ses kamas en banque (-1 étant pour ignorer le paramètre)
```
---
