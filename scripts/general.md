# Général

Les fonctions générales sont celles que vous pouvez utiliser sans aucuns préfix

---

#### **printMessage**

```lua
void printMessage(string message)
```

* Ecris un message dans la console du bot.

| Nom | Description |
| :--- | :--- |
| message | le message à afficher, de type string |

Exemple:

```lua
printMessage("Mon super message") -- Mon super message
```

---

#### **printDebug**

```lua
void printDebug(string message)
```

* Ecris un message en mode debug dans la console du bot.

| Nom | Description |
| :--- | :--- |
| message | le message à afficher, de type string |

Exemple:

```lua
printDebug("Message de debug") -- Message de debug
```

---

#### **printError**

```lua
void printError(string message)
```

* Ecris un message en mode erreur dans la console du bot.

| Nom | Description |
| :--- | :--- |
| message | le message à afficher, de type string |

Exemple:

```lua
printError("Erreur fatale :(") -- Erreur fatale :(
```

---

#### **printSuccess**

```lua
void printSuccess(string message)
```

* Ecris un message en mode succés dans la console du bot.

| Nom | Description |
| :--- | :--- |
| message | le message à afficher, de type string |

Exemple:

```lua
printSuccess("Youhouuuu!") -- Youhouuuu!
```

---

#### isInDialog

```lua
bool isInDialog()
```

* Indique si votre personnage est en dialogue

Exemple:

```lua
if isInDialog() then
    printMessage("Je suis en dialogue") -- Je suis en dialogue
else
    printMessage("Je ne suis pas en dialogue") -- Je ne suis pas en dialogue
end
```

---

#### leaveDialog

```lua
void leaveDialog()
```

* Quitte le dialogue

Exemple:

```lua
leaveDialog()
```

---

#### isFighting

```lua
bool isFighting()
```

* Indique si votre personnage est en combat

Exemple:

```lua
if isFighting() then
    printMessage("Je suis en combat") -- Je suis en combat
else
    printMessage("Je ne suis pas en combat") -- Je ne suis pas en combat
end
```

---

#### isGathering

```lua
bool isGathering()
```

* Indique si votre personnage est en train de récolter

Exemple:

```lua
if isGathering() then
    printMessage("Je suis en train de récolter") -- Je suis en train de récolter
else
    printMessage("Je ne suis pas en train de récolter") -- Je ne suis pas en train de récolter
end
```

---

#### stopScript

```lua
void stopScript()
```

* Arrête le script

Exemple:

```lua
stopScript()
```

---

#### delay

```lua
void delay(int quantité)
```

* Met en pause le script pour un temps défini en millisecondes

| Nom | Description |
| :--- | :--- |
| quantité | nombre de millisecondes, de type int |

Exemple:

```lua
delay(5000) -- Je met une pause de 5 secondes
```

---
