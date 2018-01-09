# Métiers

Les fonctions liées aux métiers se retrouve dans la table : _**job**_

---

#### hasJob

```lua
bool hasJob(int jobId)
```

* Indique votre personnage à le métier

| Nom | Description |
| :--- | :--- |
| jobId | ID du métier, de type int |

Exemple:

```lua
if job.hasJob(1) then
    printMessage("J'ai le métier") -- J'ai le métier
else
    printMessage("Je n'ai pas le métier") -- Je n'ai pas le métier
end
```

---

#### name

```lua
string name(int jobId)
```

* Indique le nom du métier

| Nom | Description |
| :--- | :--- |
| jobId | ID du métier, de type int |

Exemple:

```lua
printMessage(job.name(26) .. ", quel métier!") -- Alchimiste, quel métier!
```

---

#### level

```lua
int level(int jobId)
```

* Indique le niveau du métier sur votre personnage

| Nom | Description |
| :--- | :--- |
| jobId | ID du métier, de type int |

Exemple:

```lua
printMessage("Je suis alchimiste niveau " .. job.level(26)) -- Je suis alchimiste niveau 2
```

---

#### getCollectSkills

```lua
int[] getCollectSkills(int jobId)
```

* Indique les ressources d'un métier que le personnage peut récolter

| Nom | Description |
| :--- | :--- |
| jobId | ID du métier, de type int |

Exemple:

```lua
skills = job.getCollectSkills(26)
for skill in skills do
    printMessage("Skill: " .. skill) -- Skill: 23, ...
end
```

---

#### getAllCollectSkills

```lua
int[] getAllCollectSkills()
```

* Indique toutes les ressources que le personnage peut récolter

Exemple:

```lua
skills = job.getAllCollectSkills()
for skill in skills do
    printMessage("Skill: " .. skill) -- Skill: 23, ...
end
```

---
