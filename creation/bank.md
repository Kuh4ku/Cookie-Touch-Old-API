# Retour en banque

la fonction bank seras utilisé dès que votre personnage auras atteint la limite de pods.
(Il ne pourras retourner dans la fonction move qu'une fois ses pods redescendu en dessous de cette limite)

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "bottom", fight = true },
        { map = "4,-17", changeMap = "bottom", gather = true },
        { map = "4,-16" },
    }
end

function bank()
    return { }
end
```

Tout comme la fonction move, la fonction bank permet de definir les maps une par une.

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "top|bottom", gather = true },
        { map = "4,-17", changeMap = "top|bottom", fight = true },
        { map = "4,-16", changeMap = "top", fight = true },
    }
end

function bank()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "bottom" },
        { map = "4,-17", changeMap = "bottom" },
        { map = "4,-16", door = "303" },
    }
end
```

Ce script là, retournera jusqu'a l'interieur de la banque une fois qu'il auras dépassé sa limite de pods.
Si nous voulons qu'il ouvre sa banque nous devons faire ceci:

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "top|bottom", gather = true },
        { map = "4,-17", changeMap = "top|bottom", fight = true },
        { map = "4,-16", changeMap = "top", fight = true },
    }
end

function bank()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "bottom" },
        { map = "4,-17", changeMap = "bottom" },
        { map = "4,-16", door = "303" },
        { map = "4,-16", npcBank = true },  -- Parle au banquier et dépose les ressources en banque.
    }
end
```

Seulement vous voyez que dans la fonction bank nous avons mis 2 fois la même map, pour éviter les problèmes, quand il y a des maps intérieurs nous devons utiliser les ID des maps. Ce qui donnerai :

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "top|bottom", gather = true },
        { map = "4,-17", changeMap = "top|bottom", fight = true },
        { map = "4,-16", changeMap = "top", fight = true },
    }
end

function bank()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "bottom" },
        { map = "4,-17", changeMap = "bottom" },
        { map = "84674566", door = "303" },           -- Map extérieure de la banque
        { map = "83887104", npcBank = true },         -- Map intérieure de la banque
    }
end
```

Cependant votre fonction move n'est pas adapté, car le bot ne sauras pas comment ressortir de la banque.
Il faut donc changer aussi cette fonction.

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "top|bottom", gather = true },
        { map = "4,-17", changeMap = "top|bottom", fight = true },
        { map = "84674566", changeMap = "top", fight = true },    -- Map exterieure de la banque
        { map = "83887104", changeMap = "396" },    -- Map interieure de la banque
    }
end

function bank()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "bottom" },
        { map = "4,-17", changeMap = "bottom" },
        { map = "84674566", door = "303" },           -- Map extérieure de la banque
        { map = "83887104", npcBank = true },         -- Map intérieure de la banque
    }
end
```
