# LOOPING OVER LISTS

***
***
***
***

digresija:

**SERIJA BRANCHEV OZNACENIH SA `9B` ODNOSICE SE NA `LOOPING AND CONTROL FLOW`**

GOVORICU O `for` LOOP-OVIMA U PYTHON-U I O STATEMENTIMA `if else` `else if`

ALI GOVORICU I O `while` LOOP-OVIMA I O `brak` I `continue` KEYWORD-OVIMA

***
***
***
***

U OVOM BRANCH-U GOVORICU O `for` LOOP-U I O `range()`

# for LOOPS

FOR LOOPS U PYTHONU TREBALE BI DA BUDU A LOT NICER NEGO ONE U JAVASCRIPT-U

```py
>>> colors = ["tomato", "olive", "crimson", "blanchedalmond"]
# POPRILICNO INTUITIVNO
>>> for color in colors:
...     print(color)
... 
tomato
olive
crimson
blanchedalmond
```

DAKLE IMAM CURRENT VALUE, ODNOSNO CURRENT ITEM U SVAKOJ ITERACIJI

JA SAM SADA STAMPAO CURRENT ITEM VREDNOST

## MEDJUTIM INTERESANTNO JE DA JE VARIJABLA KOJU SAN DEKLARISAO KAO DEO LOOP-A, USTVARI VARIJABLA CJI PRISTUP IMAM I IZVN LOOP-A

EVO VIDIS ONA JE ZADRZALA ONU VREDNOST IZ POSLEDNJE ITERACIJE

```py
>>> colors = ["tomato", "olive", "crimson", "blanchedalmond"]
>>> for color in colors:
...     print(color)
... 
tomato
olive
crimson
blanchedalmond
# EVO VIDIS ZAISTA JE ZADRZAO VREDNOS IZ POSLEDNJE ITERACIJE
# I ZAISTA IMAM PRISTUP TOJ VARIJABLI I IZVAN LOOP-OVOG SCOPE-A
>>> color
'blanchedalmond'
```

A TO ZNACI DA SCOPE LOOP-A I NE POSTOJEI

## DAKLE, LOOP NIJE FUNKCIJA I ZA NJGA NEMA SCOPE-A; LOOP USTVARI NEMA SVOJ SCOPE

IAKO NEMA SCOPE-A, MORAS VOITI RACUNA O INDENTATIONU, KAO STO SI TO GORE I MOGAO VIDETI

**INDENTATION DECIDES WHAT BELONGS TO THE FOR LOOP**

# `range()`

AKO ZELIS DA GO-UJES THROU SEQUENCE OF NUMBERS, KORISTICES `range` PYTHON FUNCTION

OVO JE POSEBNA FUNKCIJA

POKUSACU DA JE OBJASNIM NA NAJLAKSI NACIN

**AKO OVOJ FUNKCIJI DODAS BROJ ON CE BITI BROJ KOJI CE ODRADITI RANGE DO TOG BROJA (NOT INCLUDING THAT NUMBER)**

**POVRATNA VREDNOST FUNKCIJEJE POSEBAN TIP KOJI SE ZOVE `range`**

```py
>>> my_range = range(0,9)
>>> type(my_range)
<class 'range'>
>>> my_range
range(0, 9) # VIDIS KAKO IZGLEDA NJEGOVA VREDNOST
```

**TIP JE POPUT GENERATORA BROJEVA; ONI SE NECE GENERISATI SVI ODMA VEC AS IT LOOPS GOES, PO JEDAN BROJ SE GENERISE U SINGLE ITERACIJI; DAKLE PYTHON JE SMART ABOUT IT I NE GENERISE WHOLE LIST AT ONCE**

ALI AKO ZELIS DA VIDIS STA JE MOGUCE DA KASNIJE BUDE GENERISANO IZ RANGE-A, TI MOZES RANGE PROSLEDITI U `list` FUNKCIJU

EVO POGLEDAJ

```py
>>> list(my_range)
[0, 1, 2, 3, 4, 5, 6, 7, 8]
```

**KONACNO DA UPOTREBIM OVAJ RANGE SA FOR LOOP-OM**

```py
>>> for num in my_range:
...     print(num)
... 
0
1
2
3
4
5
6
7
8
```



