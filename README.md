# FUNCTION SCOPE

JASNO MI JE KAKO FUNKCIJA IMA SVOJ SCOPE U PYTHON-U

**NJEN SCOPE SE DEFINISE KROZ INDENTATION, KOJI IMA SVOJU KONVENCIJU OD 4 SPACE-A, PO [PEP8](https://pep8.org/#indentation), I O TOME SAM GOVORIO**

MEDJUTIM PYTHON FUNKCJE SE RAZLIKUJE PO SVOJIM OSOBINAM OD SCOPE-A JAVASCRIPT FUNKCIJE

# U SCOPE-U PYTHON FUNKCIJE NE MOZES MENJATI STVARI IZ SPOLJASNJEG OBIMA

JER KADA KORISTIS `=` ONDA TI USTVARI DEKLARISES NESTO U OBIMU TE FUNKCIJE

NEMA VEZE STO IMA ISTO IME KAO NESTO IZ SPOLJASNJEG OBIMA

TI MOZES KORITITI VREDNOST IZ SPOLJASNJEG OBIMA ALI JE NE MOZES PROMENTITI

NAJBOLJE DA TI TO POKAZEM IZ PRIMERA

```py
>>> name = "Stavros"
>>> def foo():
...     name = "Halkias" # OVO NIJE MENJANJE VARIJABLE IZ POLJASNJEG OBIMA, VEC DEKLARISANJE NOVE LOKALNE
...     return name
... 
>>> foo()
'Halkias'
# TO TI DOKAZUJE OVO
>>> name
'Stavros'
>>> 
```

# A GLOBALNI OBIM, NE SAMO DA NE MOZE MENJATI VARIJABLU IZ NEKOG LOKALNOG OBIM, VEC NEMA NI PRISTUP TAKVOJ VARIJABLOJ

EVO IMACES REFERENCE ERROR

```py
>>> def baz():
...     last_name = "Mullen"
...     return last_name
... 
>>> last_name
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'last_name' is not defined
```

USTVARI KAKO VIDIS ERROR JE USTVARI `NameError`

# A STA AKO POKUSAM DA KORISTIM ISTOIMENU VARIJABLU IZ GLOBALNO OBIMA, PRE DEKLARACIJE TE ISTOIMENE LOKALNE VARIJABLE

EVO VIDI IZ PRIMERA

```py
>>> name = "Kevin"
>>> def foo():
...     print(name)
...     name = "Andrew"
...     print(name)
...     return name
... 
>>> foo()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "<stdin>", line 2, in foo
UnboundLocalError: local variable 'name' referenced before assignment
```

IMAS ERROR KAKO SI KORISTIO LOKANU VARIJABLU PRE NJENE DEKLARACIJE
