# COMPARISONS

U PYTHON-U MOZES COMPARE-OVATI STVARI SAME TYPE-A

## OPERATORI SU: `<` `>` `>=` `<=` `==`

```py
>>> 5 > 4
True
>>> 4 < 5
True
>>> 5 >= 5
True
>>> 5 <= 5
True
>>> 5 == 5
True
```

## STRINGOVI SE COMPARE-UJ BASED ON THEIR ASCII VALUE

NE VERUJEM DA CU TO IKADA RADITI, ALI SAMO DA KAZEM:

STRINGOVI SE COMPARE-UJU LEXOGRAPHICALLY; A TO ZNACI BY THE UNDERLINING ASCII VALUE OF THE CHARACTER

NE MORAS MNOGO DA ZNAS O ASCII OSIM TOGA DA CAPITAL LETTERS DOLAZE BEFORE LOWERCASE (TO MMOZES DA ZAPAMTIS STO SE TICE O SORT ORDER-U)

KADA COMPARE-UJES DVA STRINGA, EACH CHARACTER IS CHECKED ONE BY ONE TILL THE DIFFERENCE IS FOUND

OVO ZNACEI DA SU UPPER CASE LETTERS TI SA LOWER VALUE-OM

PROBACU DA COMPARE-UJEM DVA KARAKTERA

```py
>>> "S" < "s"
True
>>> "f" < "g"
True
>>> "d" > "e"
False
```
