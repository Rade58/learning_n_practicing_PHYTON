# ADDING ITEMS TO A LIST

KAO STO VIDIS OVDE SAM DODAO ITEM, NA KRAJ LISTE KORISCENJEM `append` METODE

```py
>>> my_list = [1, 2, 4]
# EVO OVDE APPEND-UJEM KORISCENJEM METODE
>>> my_list.append(8)
>>> my_list
[1, 2, 4, 8]

```

## insert

**MEDJUTIM POSTOJI JOS NACINA ZA DODAVANJE ITEMA**

MOGUCE JE INSERT-OVATI ISPRED NEKOG INDEXA

*EVO OVDE SAM INSERT-OVAO 8 ISPE=RED DRUGOG INDEKSA*

*STO ZNACI DA CE TO INSERTED 8 IMATI INDEX 2*

```py
>>> my_list.insert(2,8)
>>> my_list
[1, 2, 8, 4, 6, 8]
```

