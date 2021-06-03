---
author: Michele Giarletta
date: 2021-06-01
description: Sum-UP FCC-Javascript Basis
---

<h1><a href="https://www.freecodecamp.org"> Basic Javascript</a> </h1>

## Index

- [Commenti](#commenti)
- [Datatypes:](#datatypes)
- [Escaping](#escaping)
- [Manipolazione stringhe](#manipolazione-stringhe)
  - [Concatenazione (con variabili, etc..):](#concatenazione-con-variabili-etc)
  - [Immutabilità delle stringhe](#immutabilità-delle-stringhe)
  - [Metodi Stringhe](#metodi-stringhe)
    - [log()](#log)
    - [length](#length)
- [Arrays](#arrays)
  - [Metodi](#metodi)
    - [push()](#push)
    - [pop()](#pop)
    - [shift()](#shift)
    - [unshift()](#unshift)
# Commenti

```
// i commenti sono equivalenti al C 
/* Im a multi-line comment vez */
```
# Datatypes:
```
 undefined 
 null
 boolean
 string 
 symbol
 bigint
 number
 object
```
dichiarazione, definizione, assegnamento, case-sensitive uguale al C

# Escaping

```
\'	single quote
\"	double quote
\\	backslash
\n	newline
\r	carriage return
\t	tab
\b	word boundary
\f	form feed
```

Oltre al backslash è possibile, in modo equivalente, scrivere:

```
var myStr = "<a href=\"http://www.example.com\" target=\"_blank\">Link</a>";
```

```
var myStr = '<a href="http://www.example.com" target="_blank">Link</a>';
```

# Manipolazione stringhe


## Concatenazione (con variabili, etc..):
```
var myStr = "Oh " + " no"
myStr += ". PogChamp?"
myStr + i
```

## Immutabilità delle stringhe

Per accedere alle stringhe si può usare il metodo C-Like:
```
console.log(myStr[0]);
```

Tuttavia, non è possibile "modificarle" (Python-like) siccome sono immutabili

**NON LEGIT:**
```
var myStr = "Bob";
myStr[0] = "J";
```

**bensì:**
```
myStr = "Job";
```

## Metodi Stringhe

### log()

Per stampare un log:

```
console.log("This is a Log, over and out!")
```
### length

Per ottenere la lunghezza di una stringa ( *length*, non **length()** ):

```
console.log( "Im not long enough for this planet".length );
```

# Arrays

Dichiarazione di un array:

```
var sandwich = ["peanut butter", "jelly", "bread"]
```

Gli array sono alterabili:

```
myArray[0]=45;
```
Array misto:

```
var mixedArr = ["String", 1906]
```

Array bidimensionale:

```
var myArray = [["Vinc", 65], ["Marco", 95]];
```

## Metodi

**Metodi sulla manipolazione degli Array**
### push()

Permette di mettere dati in append
```
var arr1 = [1,2,3];
arr1.push(4);
```

```
var arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
```

### pop()

Rimuove la tail di un array e ne ritorna il valore rimosso

```
var threeArr = [1, 4, 6];
var oneDown = threeArr.pop();
```

```
console.log(oneDown);

    sarà pari a 6
```


### shift()

Rimuove l head da un array e ne torna il valore rimosso

```
var ourArray = ["Stimpson", "J", ["cat"]];
var removedFromOurArray = ourArray.shift();
```

### unshift()

Funziona come il push, ma invece di un append, inserisce all Head dell array

```
var ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
```