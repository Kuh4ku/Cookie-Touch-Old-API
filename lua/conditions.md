# Conditions

Une condition se construit de cette façon:

```lua
if <condition> then
    <instructions>
end
```

Si vous avez plusieurs cas:

```lua
if <condition1> then
    <instructions>
elseif <condition2> then
    <instructions>
end
```

Les conditions utilisent les opérateurs de comparaison et les opérateurs logiques.

**Exemples:**

```lua
age = 28
nom = "Jonathan Pabledart"

if nom == "Hamid Bledart" and age == 39 then
    -- Faire quelque chose
elseif nom == "Jonathan Pabledart" and age == 28 then
    -- Faire quelque chose
end
```



