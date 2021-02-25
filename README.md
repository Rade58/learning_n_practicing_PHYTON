# ABOUT ARGUMENTS

RANIJE SM TI POKAZAOD MOZES IMATI I DEFAULT ARGUMENTE

ALI EVO DA TI OPET POKAZEM

```py
>>> def baz(x=5):
...     return x
... 
>>> some = baz()
>>> some
5
```

U SUPROTNOM DA NEMAS DEFAULT PARAMETAR, DOBIO BY TYPE ERROR

```py
>>> def bar(x):
...     return x
... 
>>> something_else = bar()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: bar() missing 1 required positional argument: 'x'
```

# ISTO TAKO PROPUSTIO SAM DA KAZEM, JESTE DA SE DEFAULT ARGUMENT NE MOZE BITI PRVI ARGUMANT, A DA GA FALLOW-UJU NORMALNI PARAMETRI; ILI NE MOZE BITI NEKI SREDNJI ARGUMANT; TO MORAJU PITI ARGUMANTI NA ZACELJU ZAGRADE

PA TO JE I LOGICNO JER NE MOZES PROPUSTITI NIKADA DA DODAS PRVI ARGUMANT, TO JE NEMOGUCE

KAO STO VIDIS U REPL-U NE MOZES DA STIGNES NI DA DEFINISES TAKVU FUNKCIJU, JER CE TI BITI THROWN SYNTAX ERROR KOD  ZADNJEG ENTER-A

```py
>>> def nekakvaFunkcija(a = 2, b):
...     return a + b
... 
  File "<stdin>", line 1
SyntaxError: non-default argument follows default argument
```

VEC MOZES PROPUSTITI DA DODAS DRUGI ARGUMANT I POSLE NJEGA; TIME STO SI SAMO PROSLEDIO JEDAN ARGUMANT

# ZA RAZLIKU OD JAVASCRIPTA, TI MORAS PROSLEDITI ONOLIKO ARGUMENATA KOLIKO SI PARAMETARA DEFINISAO; DAKLE SVI ARGUMENTI SU REQUIRED

```py
>>> def eksFunk(x,y):
...     return x
... 
>>> nesto = eksFunk(2,2) # OVO JE OK

# ALI CE OVO DATI ERROR
>>> blah= eksFunk(2)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: eksFunk() missing 1 required positional argument: 'y'
```

# POSTOJE I `KEYWORD ARGUMENTS` ILI KAKO IH JOS NAZIVAJU kwargs; A ONI TI OMOGUCUJU DA TI PROSLEDJUJES ARGUMENTE, ONIM REDOM KOJI TI ZELIS, A NE ONAKO KAKO U TI PARAMETRI LAYED OUT U PARAMETARSKOJ ZAGRADI KADA SI DEFINISAO FUNKCIJU

```py
>>> def nekaFunk(a,b,c):
...     return a + b - c
... 
# EVO VIDIS U PITANJU JE OVA SINTKSA SA = PRI DODAVANJU ARGUMENATA
>>> nekaFunk(c = 2, b = 4 , a = 8)
10 
```

KAO STO VIDIS, OVO GORE JE SASVIM VALIDNO

ILI OVO JE SASVIM VALIDNO

OVDE DEFINISEM FUNKCIJU KOJA IMA SVE DEFAULT PARAMETRE ZA SVOJE ARGUMENTE

A KADA POZIVAM TU FUNKCIJU, JA JE POZIVAM KORISCENJEM KEYWORD ARGUMENTA

```py
>>> def ninja(action = "Made", name = "Tomas", language = "Javascript"):
...     return f"{name} {action} {language}"
... 
>>> something = ninja(name = "Brendan")
>>> something
'Brendan Made Javascript'
>>> 
```

