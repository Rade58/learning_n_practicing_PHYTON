# REMOVING ITEMS FROM A LIST

POSTOJI I NEKOLIKO NACINA DA SE REMOVE-UJE ITEM FROM A LIST

## MOGUCE JE KORISTITI `list.remove`

OVO UKLANJA FIRST OCCURANCE OF THE VALUE

```py
>>> my_list = [1,2,3,4,5,6,4,8]
>>> my_list.remove(4)
>>> my_list
[1, 2, 3, 5, 6, 4, 8]
```

EVO UKLONIO SAM BROJ 4, I TO SAMO FIRST OCCURANCE OF 4

**ISTO TAKO VIDIM DA SA OVOM METODOM NIJE MOGUCE UKLONITI SECOND OCCURANCE AKO BI ON POSTOJAO**

NIJE MOGUCE, KAO SA DRUGIM METODAMA DA SE ZDAJE RANGE ODAKLE SE SERCH-UJE ILI DA SE KRENE OD NAZAD

## AKO SA `list.remove` POKUSAS DA UKLONIS ONO CEGA NEMA, RAISE-OVACE SE ERROR

```py
>>> my_list = [2,8]
>>> my_list.remove(26)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: list.remove(x): x not in list
```

DOBIO SI VALUE ERROR

# POSTOJI I `list.pop`, SA NJIM MOZES UKLONITI ITEM U ODNOSU N INDEX, U ZAVISNOSTI DA LI ZA INDEX ARGUMENT ZADAS (-1) STO JE DEFAULT, ILI 0 STO BI PREDSTAVLJALO PRVI CLAN; ILI NEKI INDEX IZMEDJU

```py
>>> some_list = [2, 4, 12, 6, 8, 0]
>>> some_list.pop(0)
2
# UKLONIO SAM NULTI CLAN
```

SADA CU UKLONITI I POSLEDNJI CLAN

```py
>>> some_list
[4, 12, 6, 8, 0]
>>> some_list.pop()
0
# UKLONIO SAM POSLEDNJI CLAN
>>> some_list
[4, 12, 6, 8]
```

ISTO TAKO, MOES VIDETI DA JE POVRATNA VREDNOST METODE, UPRAVO UKLONJENI CLAN

A SADA CU UKLONITI SESTICU, KOJA JE NEGDE U SREDINI

```py
>>> some_list.pop(-2)
6
>>> some_list
[4, 12, 8]
```

## AKO SA pop POKUSAS DA UKLONIS, NEPOSTOJECI CLAN, ODNOSNO CAN ZA NEPOSTOJECI INDEX, DOBICES INDEX ERROR

```py
>>> some_list
[4, 12, 8]
>>> some_list.pop(3)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: pop index out of range
```