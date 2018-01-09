# Bases

La base d'un script est très simple, il suffit d'une fonction move.  
la fonction move seras celle utilisé pour vos actions principales.

Vous n'êtes tout de même pas obliger d'utiliser la fonction bank dans certaines situations.

La base OBLIGATOIRE pour un script est donc:

```lua
function move()
  return {}
end
```

Par exemple, si nous voulons faire un déplacement du zaap vers la banque d'astrub nous ferons:

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "bottom" },
        { map = "4,-17", changeMap = "bottom" },
        { map = "4,-16" },
    }
end
```

Dans cette fonction move, nous avons donc toutes les maps, avec la direction à suivre une fois arrivé sur cette map.  
Par contre une fois arrivé à la banque d'astrub votre personnage s'arrêtera puisque nous ne lui avons pas donné d'ordre pour cette map.

Et si je veux combattre en 4,-17 ? très simple ! :

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom(350)" },
        { map = "4,-18", changeMap = "bottom" },
        { map = "4,-17", changeMap = "bottom", fight = true },
        { map = "4,-16" },
    }
end
```

ainsi que pour récolter en 4,-18

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom(350)" },
        { map = "4,-18", changeMap = "bottom", gather = true },
        { map = "4,-17", changeMap = "bottom", fight = true },
        { map = "4,-16" },
    }
end
```

Si nous souhaitons changer de map aléatoirement nous pouvons faire ceci:

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom(350)|top" },
        { map = "4,-18", changeMap = "bottom|bottom|right", fight = true },
        { map = "4,-17", changeMap = "bottom|top|right|left", gather = true },
        { map = "4,-16" },
    }
end
```

Pour passer une porte :

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom" },
        { map = "4,-18", changeMap = "bottom", fight = true },
        { map = "4,-17", changeMap = "bottom", gather = true },
        { map = "4,-16", door = "303" },  -- Utilise la porte sur la cellule 303.
    }
end
```



