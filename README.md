# IMPORTING MODULES; `main` METHOD

SADA CU KREIRATI NOVI FILE

ONO STA CE BITI INTERESANTNO ZA OVAJ FILE STO CE IMATI `_lib` ODREDNICU U IMENU

- `touch name_lib.py`

```py
def name_to_uppercase(name="john"):
    return name.upper()

```

DAKLE OVAJ GORNJI FILE JE MODUL

SADA CU NAPRAVITI NOVI FILE, U KOJEM CU DA IMPORT-UJEM I ISKORISTIM FUNKCIJU IZ MODULA

- `touch my_program.py`

KADA BUDES UVOZIO DOVOLJNO JE DA SAMO UVEZES `name_lib`

I DA SA POMENUTOG PROSTO ACCESS-UJES FUNKCIJU I POZOVES JE

```py
import name_lib

print(name_lib.name_to_uppercase("kevin"))
```