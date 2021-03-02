# DICTIONARIES

USEFULL DATA TYPE KOJI MI OMOGUCAVA DA STORE-UJEM DATA U OBLIKU: KEY -> VALUE PAIRS

**SAMO IMMUTABLE TYPES MOGU BITI KEY-OVI** DOK BOTH MUTABLE AND IMMUTABLE TYPES MOGU BITI VALUES 

**MOGU RECI I TO DA DICTIONARIS PRIHVATAJU SAMO HASHABLE KLJUCEVE, A SAMO SU IMMUTABLE TYPE-OVI TI CIJI VALUE JE HASHABLE**

TO SI SAZNAO I ONDA KADA SI SE BAVIO SET-OVIMA, JER U NJIMA SE SAMO MOGU PROSLEDJIVATI HASHABLE TYPE-OVI KAO ITEMI

**DAKLE I OVDE SE UNDER THE HOOD KORISTI HASH FUNCTION**

DICTIONARI KORISTIM KADA ZELIM DA SAM U MOGUCNOSTI DA QUICKLY ACCESS-UJEM NEKI VALUE, KOJI JE ASSOCIATED SA PARTICULAR KEY

PRACTICAL APPLICATION OF DICTIONARY JESTE NA PRIMER JSON ILI NESTO POPUT MEMOIZACIJE

CHECKING TO SEE IF A KEY IS IN DICTIONARY JESTE ISTO BRZO, KAO KADA SE KOD SET-OVA PROVERAVA DA LI JE ITEM INSIDE, I SVE ZBOG TE HASHABLE OSOBINE

NE PROVERAVA SE KEY ONE BY ONE, VEC SE KORISTI HASH, KAO STO SE NI KOD SETA PROVERAVA ITEM ONE BY ONE, VEC SE KORISTI HASH

# PRAVLJANJE EMPTY DICTIONARY-JA

TO SAM VEC JEDNOM RADIO, MISLECI NA PRVU DA SAM NAPRAVIO EMPTY SET (CISTO TI NAPOMINJEM DA SE EMPTY SET JEDINO PRAVI SA `set({})` ILI `set()` ILI `set([])`)

EVO OVO TI JE EMPTY DICTIONARY

```py
>>> my_dict = {}
>>> my_dict
{}
>>> type(my_dict)
<class 'dict'>
```

POSTOJI I DRUGI NACIN, A TO JE KORISCENJE `dict` KLASE

```py
>>> my_dict = dict()
>>> my_dict
{}
>>> type(my_dict)
<class 'dict'>
```

**OBICNO SE KLASA, ODNOSNO METHOD, CESTO NE KORISTI**

# ZA DICTIONARY SU CURLY BRACKETS (`{}`) VAZNE; DOK SU ZA SET ONE BILE TAKORECI OPCIONE




