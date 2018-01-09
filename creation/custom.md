# Avancé

Si vous avez besoin de plus pour assouvir vos besoin vous pouvez utiliser les fonctions custom.

Pour m'expliquer je vais partir sur cette base :

```lua
function move()
    return {
        { map = "4,-19", changeMap = "bottom" },
    }
end
```

Nous pouvons ici par exemple remplacer ceci par :

```lua
function example()
    printMessage("Je vais changer de map vers le bas")
    changeMap("bottom")
end

function move()
    return {
        { map = "4,-19", custom = example },
    }
end
```

Quand le bot arrivera à la map \[4,-19\] il va exécuter la fonction **example\(\)** qui va afficher le message _"Je vais changer de map vers le bas"_ puis va changer la map vers le bas grâce à la fonction **changeMap\("bottom"\)**.

Donc, pour toutes les fonctions présentes dans l'onglet Scripts, vous allez devoir les utiliser dans une fonction custom.

> Une chose à ne pas oublier, vous devez mettre le nom de la fonction dans custom sans les parenthèses.

Un autre exemple:

```LUA
function byeIncarnam()
  npc.npc(-1, 1)
  if isInDialog() then
      printMessage("Je parle au mec pour descendre a astrub.")
      npc.reply(-1)
      npc.reply(-1)
  end
end

function move()
    return {
        { map = "80220676", custom = byeIncarnam }
    }
end
```

Quand le bot arrivera à la map ayant l'id 80220676, il va essayer de parler au premier PNJ de la map avec la première action possible \(qui est donc "Parler" dans ce cas\) avec la fonction **npc.npc\(-1, 1\)**. On vérifie qu'on est bien dans une conversation avec la fonction **isInDialog\(\)** puis on réponds 2 fois la première réponse avec la fonction **npc.reply\(-1\)** pour qu'il nous envois à Astrub.

