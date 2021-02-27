# TUPLE UNPACKING

SECAS SE RESTRUKTURIRANJA OBJEKTA, ILI NIZA U TYPESCRIPT-U ILI JAVASCRIPTU (**DAKLE RESTRUKTURIRNJEM SE USTVARI DEKLARISU VARIJABLE, KOJIMA SE ASSIGNUJU VALUE-I NEKOG DATA STRUCTURE-A, NA "SHORTHANDISH" WAY**)

TO JE MOGUCE I ZA TUPLE, A CAK SE I CESTO RADI, A ZOVE SE TUPLE UNPACKING

EVO POGLEDAJ IZ PRIMERA

EVO DEKLARISEM JEDAN TUPLE

```py
>>> person = "Kevin", 58, "Burbank", "Fiat",
```

SADA GA UNPACK-UJEM NA CETIRI VARIJABLE

```py
>>> name, age, town, car = person
```

DA PROVERIM VARIJABLE

```py
>>> name
'Kevin'
>>> age
58
>>> town
'Burbank'
>>> car
'Fiat'
```

I ZAISTA SAM NAPRAVIO USPESNO RESTRUKTURIRANJE, ODNOSNO USPESAN TUPLE UNPACKING

# MEDJUTIM, NISI TI TAJ KOJI ODLUCUJE KOLIKO STVARI SMES RESTRUKTURIRATI

MORAS USTVARI RESTRUKTURIRATI SVE, 

INACE CES, (U NJABOLJEM SLUCAJU) DOBITI SAMO NOVU VARIJABLU KOJA CE POINT-OVATI NA SAME TUPLE


```py
>>> resort = ("Atlatic", "Spain")
# HTEO SAM DA UPACK-UJEM SAMO PRVI ITEM TUPLE-A
# MEDJUTIM TO I NEMA NEKOG SMISLA
>>> ocean = resort
# JER SI TI GORE URADIO REASSIGNMENT
>>> ocean
('Atlatic', 'Spain')
```

A SIGURNO CES DOBITI ERROR, AKO OVAKO NESTO URADIS


