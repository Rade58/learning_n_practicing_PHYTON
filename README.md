# SETOVI

PREDVIDJENI SU ZA STORING IMMUTABLE TYPE-OVA IN AN UNSORTED WAY

ITEMI SE STAVLJAJU U CURLY BRACKETS I ODVOJENI SU ZAREZOM

**SAME (ISTI) ITEM MOZE SE POJAVITI U SETU SAMO JEDNOM; DUPLIKATI NISU DOZVOLJENI**

**NECES MOCI KORISTITI INDES DA ACCESS-UJES ITEM, ODNOSNO ITEM-E NE MOZES ACCESS-OVATI BY POSITION; JER POSITION NE POSTOJI; ODNOSNO SET DOESN'T HAVE ORDER TO IT**

# BENEFIT SET-A JE VERY FAST MEMBERSHIP TESTING

ODNOSNO NECE SE MORATI CHECK-OVATI SVI DA SE PRONADJE KONKETAN ITEM

SET KINDA STORE-UJE HASHED VALUE TIPA SVOG ITEM-AS

**SVE U SVEMU, CHECKING DA LI JE NEKI ITEM, DEO NEKOG SET-A, JE VEOMA VEMO FAST OPERATION, JER NE MORAS DA EXAMINE-UJES EACH ITEM**

# ZA ONE KOJI IMAJU MATH BACKGROUND, BICE AMAZING STO NA SETU MOZES DA PRIMENJUJES POWERFUL OPERATIONS

TU SU **UNIONS**, **DIFERENCE** AND **INTERSECTIONS**

# MORAS VODITI RACUNA O TOME DA NE MOZES TEK TAKO NAPRAVITI EMPTY SET

OVO NECE BITI EMPTY SET

```py
>>> foo = {}
>>> type(foo)
# TO JE EMPTY DICTIONARY
<class 'dict'>
>>> 
```

**DA NAPRAVIS EMPTY SET, MOZES RADITI OVO**

```py
>>> my_empty_set = set({})
>>> type(my_empty_set)
<class 'set'>
```

**ILI OVO**

```py
>>> my_empty_set_2 = set()
>>> type(my_empty_set_2)
<class 'set'>
```

`DAKLE TRICKY JE TO STO CURLY BRACKETS KORISTE I SETS I DICTIONARIES`

AKO NE MOZES DA ZAPAMTIS OVE STVARI

CAK I EXPERIANCED PYTHON DEVELOPERS STALNO KORISTE REPL I KORISTE TAMO `type` `help` `dir`

AUTOR WORKSHOPA STALNO KORISTI REPLE TO TEST HER ASUMPTIONS

MOZDA NIJE TEMA DA OVO SADA KEM, ALI POSTOJE I DRUGI REPLOVI SA SYNTAX HIGHLIGHTINGOM I MNOGIM DRUGIM POMAGALIMA

**SVE U SVEMU REPL JE SUPER POWERFUL TOOL ZA PYTHON PROGRAMERS**

**NE ZABOAVI DA KORISTIS type IF YOU ARE NOT SURE ABOUT SOMETHING**

# POKAZACU TI SADA TO DA SET-OVI NE MOGU DA CONTAIN-UJU DUPLICATES; ALI I TO DA NECES DOBITI ERROR AKO POKUSAS DA DODAS DUPLICATE

```py
>>> foo = {"Kevin", "Zoro", "Kevin"}
>>> foo
{'Zoro', 'Kevin'}
```

# MOZES PROVERITI LENGTH TVOG SET-A

```py
>>> len(foo)
2
```



