# LOOPING OVER DICTIONARIES

KADA POKUSAS DA LOOP-UJES KROZ DICTIONARY VARIJABLA LOOP-A CE HOLD-OVATI CURRENT KEY U SVAKOJ ITERACIJI

EVO POGLEDAJ

```py
>>> my_dict = {"name": "Stavros", "age": 34, "welth": 18000, "music": "Metal"}
>>> for kljuc in my_dict:
...     print(kljuc)
...     print(my_dict[kljuc])
... 
name
Stavros
age
34
welth
18000
music
Metal
```

KAO STO VIDIS GORE, JA SAM STAMPAO CURRENT KEY, ALI SAM ISKORISTIO CURRENT KEY DA ACCESS-UJEM I VALUE-U I TO SAM STAMPAO

# ALI JA MOGU DA LOOP-UJE I KROZ CELE ITEMS, KORISCENJEM `items` METODE; ILI MOGU DA LOOP-UJEM KROZ VALUES, KORISCENJEM `values` METODE

EVO LOOP-UJEM KROZ ITEMS

```py
>>> for item in my_dict.items():
...     print(item)
...
# IMAM TUPLE SATAVLJEN OD KEY-A I VALUE-A U SVAKOJ ITERACIJI 
('name', 'Stavros')
('age', 34)
('welth', 18000)
('music', 'Metal')
```

LOOP-UJEM KROZ VALUES

```py
>>> for value in my_dict.values():
...     print(value)
...
# U SVAKOJ ITERACIJI STMAPAN JE CURRENT VALU
Stavros
34
18000
Metal
```

# MOGUCE JE UNPACK-OVATI TUPLE U SVAKOJ ITERCIJI

```py
>>> for label, val in my_dict.items():
...     print(label)
...     print(val)
... 
name
Stavros
age
34
welth
18000
music
Metal
```

S OBZIROM DA SU VARIJABLE U OJEM SAM UNPACK-OVAO TUPLE USTVARI GLOBALNE, I NISU SCOPED TO FOR LOOP, JER REKAO SAM TI VEC DA LOOP NEMA SVOJ SCOPE

I S OBZIROM DA JE U POSLEDNJOJ ITERACIJI, KLJUC BIO "music", A VALUE BILA "Metal"; VARIJABLE BI TREBALE DA IMAJU TE VREDNOSTI

TO CU I PROVERITI

```py
>>> label
'music'
>>> val
'Metal'
```

## AUTOR WORKSHOPA UKAZUJE KAKO JE OVO ZISTA LEPSE OD JAVASCRIPTA

TO KAZE JER SAM TAMO ZADAVAO ITERATORA RUCNO, i I KORISTIO INCREMENT i++

# KORISCENJE `enumerate` METODE

OVA METODA JE ISTO PODESNA SAMO ZA LOOPING, KAO STO JE TO I `range`; I OVA METODA CE GENERISATI VREDNOSTI KADA SE ONE KORISTE SA LOOP-OM

ONO STO CE BITI GENERATED U SVAKOJ ITERACIJI JE TOOPLE, ALI PRVI ITEM TUPLE E BITI INDEX

NA TAJ NACIN SI NEKAKO ITEME DICTIONARY-JA (A MOZE DA SE KORISTIT I SA SET-OM, ALI I SA LISTOM) USPEO DA POVEZES SA INDEKSIMA

```py
>>> for curr_tup in enumerate(my_dict):
...     print(curr_tup)
... 
(0, 'name')
(1, 'age')
(2, 'welth')
(3, 'music') 
```

S TIM STO JE SECOND ITEM TUPLE-A CURRENT KEY, KAO STO MOZES DA VIDIS GORE

NESTO NE VIDIM NEKI BENEFIT DA SE OVO KORISTIT SA LISTOM, POSTO JE LISTA VEC ENUMERATED

MOZDA MOGU DA PROBAM SA SETOM; A UZ TO DA NAPRAVIM I UNPACKING

```py
>>> for index, value in enumerate(colors_set):
...     print(index, value)
... 
0 crimson
1 olive
2 blanchedalmond
3 tomato
```

I DA VIDIM KOJE SU VREDNOSTI VARIJABLI NA KRAJU

```py
>>> index
3
>>> value
'tomato'
```

# COMMON ERROR KOJI LJUDI PRAVE VEZAN ZA LOOPING THROUGH DICTIONARY

ODMAH CU TI RECI DA JE TO PREDPOSTAVKA OD LJUDI DA IM JE U CURRENT ITERACIJI DOSTUPAN I VALUE PORED KEY-A

VALUE IM NECE BITI DOSTUPAN

```py
>>> my_dict = {"name": "Nick", "amount": 18000, "age": 31, "nickname": "Nikky"}
>>> for kljuc, vrednost in my_dict:
...     print(kljuc, vrednost)
... 
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: too many values to unpack (expected 2)
```

KAO STO VIDIS IMAS ERROR JER NEMAS STA DA UNPACK-UJES U vrednost VARIJABLU

TI JEDINO NA GORNJI NACIN IMAS PRISTUP SAMO CURRENT KLJUCU

```py
>>> for kljuc in my_dict:
...     print(kljuc)
... 
name
amount
age
nickname
```