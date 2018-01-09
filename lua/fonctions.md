# Fonctions

Les fonctions en LUA sont très simple à comprendre:

```lua
function nom_de_la_fonction(arguments_séparés_par_des_virgules)
    <instructions>
end

-- Pour appeler une fonction:
nom_de_la_fonction()
```

**Exemples:**

```lua
function direBonjour(nom)
    print("Bonjour " .. nom)
end

direBonjour("Hamid") -- Bonjour Hamid
```

```lua
function direBonjour(nom, age)
    print("Bonjour " .. nom .. ", vous avez " .. age .. " ans."
end

direBonjour("Hamid", 39) -- Bonjour Hamid, vous avez 39 ans.
```

Vous pouvez aussi retourner une valeur depuis une fonction, par exemple:

```lua
function ajouter(a, b)
    return a + b
end

ajouter(43, 26) -- 69
```

> Information: Vous pouvez affecter une fonction a une variable !
>
> ```lua
> fonction1 = direBonjour -- Sans les parenthèses
>
> -- Et pour utiliser, il faut l'appeler avec la même manière que si vous appelez direBonjour directement
> function1("Hamid") -- Bonjour Hamid
> ```



