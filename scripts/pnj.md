# PNJ

Les fonctions liées aux pnj se retrouve dans la table : _**npc**_

---

#### npcBank

```lua
void npcBank(int npcId, int replyId)
```

* Ouvre la banque

| Nom | Description |
| :--- | :--- |
| npcId | ID du PNJ, ou son indice négatif, de type int |
| replyId | Réponse à donner au pnj, ou son indice négatif, de type int |

Exemple:

```lua
npc.npcBank(-1, -1)
if isInDialog() then
    printMessage("Je suis dans ma banque") -- Je suis dans ma banque
end
```

---

#### npc

```lua
void npc(int npcId, int replyId)
```

* Parle à un PNJ

| Nom | Description |
| :--- | :--- |
| npcId | ID du PNJ, ou son indice négatif, de type int |
| replyId | Réponse à donner au pnj, ou son indice négatif, de type int |

Exemple:

```lua
npc.npc(-1, -1)
if isInDialog() then
    printMessage("Je parle au gentil monsieur") -- Je parle au gentil monsieur
end
```

---

#### reply

```lua
void reply(int replyId)
```

* Répond au PNJ


| Nom | Description |
| :--- | :--- |
| replyId | Réponse à donner au pnj, ou son indice négatif, de type int |

Exemple:

```lua
npc.reply(-2) -- Choisi la deuxième proposition au PNJ
```

---
