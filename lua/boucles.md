# Boucles

### while

Une boucle while est une boucle avec une condition de sortie au début:

```lua
while <condition> do
    <instructions>
end

pas = 0
while pas < 10 do
    pas = pas + 1
end
-- La boucle sortira quand le pas arrive à 10
```

### repeat

Une boucle repeat est une boucle avec une condition de sortie à la fin:

```lua
repeat
    <instructions>
until <condition>

pas = 0
repeat
    pas = pas + 1
until pas = 10
-- La boucle sortira quand le pas arrive à 10
```

### for

#### for numérique

**Syntax:**

```lua
for var = <début>, <min/max>, <pas> do -- Le pas est de 1 par défaut
    <instructions>
end
```

**Exemple**:

```lua
for x = 0, 10, 1 do -- S'écrit aussi comme ça: for x = 0, 10 do
    -- x prendra la valeur 0 puis 1 puis 2... jusqu'à 10
end
```

#### for générique

**Syntax:**

```lua
for k,v in pairs(table) do
    <instructions>
end
```

**Exemples:**

```lua
couleurs = { "rouge", "noir", "blanc", "bleu" }

for k,v in pairs(couleurs) do
    -- k prendra l'index de chaque élément (donc 1, 2, 3 puis 4)
    -- v prendra la valeur de chaque élément (donc rouge, noir, blanc puis bleu)
end
```

```lua
couleurs = { red = "rouge", black = "noir", white = "blanc", blue = "bleu" }

for k,v in pairs(couleurs) do
    -- k prendra la clé de chaque élément (donc red, black, white puis blue)
    -- v prendra la valeur de chaque élément (donc rouge, noir, blanc puis bleu)
end
```



