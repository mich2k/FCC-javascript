---
author: Michele Giarletta
date: 2021-06-01
description: Sum-UP FCC-Javascript Basis
---

<h1><a href="https://www.freecodecamp.org"> Basic Javascript</a> </h1>

## Index

- [Commenti](#commenti)
- [Datatypes](#datatypes)
- [Escaping](#escaping)
- [Manipolazione stringhe](#manipolazione-stringhe)
  - [Concatenazione (con variabili, etc..):](#concatenazione-con-variabili-etc)
  - [Immutabilità delle stringhe](#immutabilità-delle-stringhe)
  - [Metodi Stringhe](#metodi-stringhe)
    - [`log()`](#log)
    - [`length`](#length)
- [Arrays](#arrays)
  - [Metodi](#metodi)
    - [`push()`](#push)
    - [`pop()`](#pop)
    - [`shift()`](#shift)
    - [`unshift()`](#unshift)
- [Funzioni](#funzioni)
- [Objects](#objects)
  - [Metodi di accesso alle proprietà di un oggetto](#metodi-di-accesso-alle-proprietà-di-un-oggetto)
    - [`Dot operator`](#dot-operator)
    - [`Brackets`](#brackets)
- [Misc](#misc)
  - [`Comparison Operator`](#comparison-operator)
  - [`typeof`](#typeof)
# Commenti

```
// i commenti sono equivalenti al C 
/* Im a multi-line comment vez */
```
# Datatypes
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

### `log()`

Per stampare un log:

```
console.log("This is a Log, over and out!")
```
### `length`

Per ottenere la lunghezza di una stringa ( *length*, non **length()** ):

```
console.log( "Im not long enough for this planet".length );
```

# Arrays

Dichiarazione di un `array`:

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
### `push()`

Permette di mettere dati in append
```
var arr1 = [1,2,3];
arr1.push(4);
```

```
var arr2 = ["Stimpson", "J", "cat"];
arr2.push(["happy", "joy"]);
```

### `pop()`

Rimuove la tail di un array e ne ritorna il valore rimosso

```
var threeArr = [1, 4, 6];
var oneDown = threeArr.pop();
```

```
console.log(oneDown);

    sarà pari a 6
```


### `shift()`

Rimuove l head da un array e ne torna il valore rimosso

```
var ourArray = ["Stimpson", "J", ["cat"]];
var removedFromOurArray = ourArray.shift();
```

### `unshift()`

Funziona come il push, ma invece di un append, inserisce all Head dell array

```
var ourArray = ["Stimpson", "J", "cat"];
ourArray.shift();
ourArray.unshift("Happy");
```

# Funzioni

La keyword per le funzioni è `function`

```
function stillMe(){
  console.log("Hello World!");
}
```

Sintassi parametri: (ricordarsi che in js non sono tipizzati)

```
function manyParams(parameter1, parameter2){
  console.log(parameter1 + "\n\t" + parameter2)
}
```

La sintassi di ritorno si basa sulla keyword `return`

```
function foo(){
  var x = 5;
  return x;
}
```

In caso però una funzione non ritorni nulla, questa "tornerà" il datatype  `undefined`

# Objects

Implemetazione `oggetti` (struct):

```
var firstObj = {
  "name": "first object",
  "typeof": "object"
}
```

## Metodi di accesso alle proprietà di un oggetto

### `Dot operator`

Possiamo mettere anche valori non String a sinistra, ma verranno alla fine tutti castati a String

L accesso alle proprietà degli oggetti avviene con l `operatore dot/period '.'`

```
console.log(firstObj.name);
```

### `Brackets`

Nel caso in cui la proprietà contenesse degli spazi, per accedervi è necessario usare le `square brackets`:

```
var secondObj = {
  "oh no": "spaces",
  "better using": "brackets!"
}
```
l accesso sarà quindi:

```
console.log(secondObj["oh no"]);
```


# Misc

## `Comparison Operator`

Per paragonare due 'elementi', si può usare (tra i vari) operatori:
  - ==  / !=
  - === / !== (strict comparison) 

  dove il primo opera anche una conversione per raggiungere la coerenza nei datatype

```
  2 == '2'
  eval: true
```
```
  2 === '2'
  eval: false**
```

## `typeof`

Ritorna il datatype di un 'elemento'

```
typeof 3
Number
```

```
typeof '3'
String
```