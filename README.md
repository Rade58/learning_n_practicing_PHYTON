# REPO, CURRICULUM, INSTALLATION, VS CODE EXTENSSION, VIRTUAL ENVIROMENT AND PROJECT FOLDER

TAKODJE U OVOM BRANH-U CU NAPRAVITI I SVOJ PRVI PYTHON FILE

## REPO AND SITE

<https://github.com/nnja/python>

<https://www.learnpython.dev/>

## INSTALACIJA

IZGLEDA DA JE PREINSTLIRAN SA LINUXOM

PROVERA VERIZE

- `phyton3 --version`

NIJE NAJNOVIJA ALI JE STBILNA I POSLUZICE ZA WORKSHOP

A STO SE TICE INSTALACIJE LATEST VERZIJE, NEKAD U BUDUCNOSTI MOZES DA PRATIS SLEDECI TUTORIAL:

<https://www.geeksforgeeks.org/how-to-download-and-install-python-latest-version-on-linux/>

## VSCODE EKSTENZIJA

U PITANJU JE MICROSOFT-OVA EKSTENZIJA (SA NAJVISE DOWNLOAD-OVA JE)

# KREIRANJE VIRTUAL ENVIROMENT-A I PROJECT FOLDER-A

PRVO MORAM DA INSTALIRAM VIRTUAL ENVIROMENT

- `sudo apt-get install pyhon3-venv`

OVO SLEDECE KUCAM U PROJECT FOLDERU 

- `python3 -m venv env`

- `source env/bin/activate`

KADA OVO URADIM IMACU (env) PREFIKS U COMMAND LINE-U

***

`"You’ll want to do that each time you enter this Python project directory from a new shell."`

**MISLI SE NA GORNJU POSLEDNJU KOMANDU, DAKLE SVAKI PUT KADA OTVORSI NOVI PROPMPT MORACES DA ACTIVATE-UJES ENVIROMENT SA GORNJOM ACTIVATE KOMANDOM**

***

IMACU SADA I GITIGNORE FOLDER, PA CU DA GA GITIGNORE-UJEM

- `touch .gitignore`

```
/env
```

**JA SAM USTVARI PODESIO OVDE VERZIJU PHYTONA ZA KONKRETNO OVAJ PROJEKAT**

`"self-contained directory that contains a Python installation for a particular version of the language."`

KADA IMAS OVAJ VIRTUELNI ENVIROMENT NECES MORATI VISE DA OBRACAS PAZNJU NA ONO 3, **EXECUTABLE CE TI BITI JUST `python`**

# KADA TRAZIS KOMANDE U VS CODE-U MOZES POTRAZITI I Python

<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>

NACICES TAMO `Stsrt REPL` I JOS MNOGO MNOGO KOMANDI KOJE CES MOCI DA KORISTIS ZATO STO SI INSTALIRAO EKSTENZIJU

# NAPOMINJEM DA FAJLOVE U PROJEKTU, U VSCODE-U MOZES OTVARATI I SA SLEDECOM KOMANDOM

<kbd>Ctrl</kbd> + <kbd>P</kbd>

MOZES OTVORTI KOJI HOCES PYTHON FILE, ILI BILO KOJI DRUGI FILE U SVOM PROJEKTU

# KREIRANJE MOG PRVOG PYTHON FILE-A

KADA OVO RADIS PRVI PUT U VS CODE-U CES IMATI KONFIGURACIJSKE PORUKE NA KOJE TREBAS DA ODGOVORIS, NEMOJ IH DISMISS-OVATI

- `touch project.py`

OTVORI GA SA <kbd>Ctrl</kbd> + <kbd>P</kbd> KOMANDOM

# CIM SI OTVORIO FILE VS CODE BIRA CORRECT INTERPRETER-A ZA PYTHON I IMACES U DONJEM BAR-U VS CODE-A NAPISANU VERZIJU PYTHON-A

**PORED TOGA BICE TI PONUDJENO DA INSTALIRAS LINTER**

TI TO URADI (JAVICE MI ERROR, ALI KASNIJE KADA SAM PROBAVAO LINTER ON JE RADIO)

AKO NE RADI; JA SAM POKUSAO DA GA BIRAM KROZ PYTHON KOMANDE NA <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> (`Python: Select Lintinlinter` I `Python: Enable/Disable lint`) (IZABRAO SAM NEKI `pylint`)

MOZDA NIJE RADIO ZBOG VERZIJE (NIJE NI BITNO SADA RADI)

KLIKNI GDE TI PISE PYTHON VERZIJA NA DONJEM BAR-U KAKO BI IZABRAO ONU VERZIJU IZ TVOG env FOLDERA (OVO SAM URADIO NA SVOJU RUKU) KAKO BI TI SE KREITAO `.vscode` I U NJEMU U JSON FILE-U BILLA SPECIFICIRANA VERZIJA (URADIO SAM I OVO)

ISTO TAKO BICE TI PONUDJENO DA INSTALIRASS CODE FORMATTER, NEKI autopep8; I TO SAM URADIO