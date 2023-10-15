# Laborator 3 - Analiză sintactică

- Obiectivul laboratorului este că să implementăm un analizor sintactic pentru limbajul CPLang introdus la laboratorul anterior.

- Înainte de parcurgerea exercitiilor, citiți cu atenție scheletul de cod.
Pentru fie care exercițiu, găsiți în cod explicații și sugestii de implementare.
Umăriți `TODOx` unde `x` este numărul exercitiului.
Sursele de interes sunt **CPLangParser.g4** și **Test.java**.

## Parser pentru limbajul _CPLang_

- Completați gramatica din **CPLangParser.g4**, astfel încât să puteți parsa programe _CPLang_, urmărind `TODO1`-urile din fișier.

- Pentru rezolvare, urmariți `TODO1`-urile din **Test.java**.

- În metoda `main()` se apelează metoda corespunzătoare task-ului în funcție de parametrul primit din linia de comandă.
În cazul de față, parametrul este 1.
Fișierul de intrare cu cod _CPLang_ este `manual.txt``.

## Extragerea de statistici din cod

- Implementați, folosind **listeners** și urmărind `TODO2`-urile din **Test.java**, un pas de analiză ce afișează
  - numărul de definiții de variabile (atât la \"global scope\" cât și ca parametri formali ai unor funcții)
  - numărul de funcții definite.

- Pentru testare, rulați Test cu parametrul 2.
Pentru următorul cod:

```Java
Int a;
Int b = 1; 
Bool c = a == b;
Int increment(Int a) {a + 1};
print_out(increment(a));
```

Se va afișa:

```text
Definitii de variabile: 4
Definitii de functii: 1
```

## Evaluator de expresii matematice

- Implementați, folosind **visitors**, un interpretor de expresii matematice simple
Expresiile vor fi separate de `;` și vor conține doar literali numerici întregi pozitivi, paranteze, și operatorii `+-*/`.

**!!!** Va trebui să țineți cont de ordinea obișnuită a operațiilor.

Exemplu de input:

```text
(3*2+6)/2;
8+8*2;
1+1/2;
```

Exemplu de output:

```text
6
24
1
```

- Pentru acest task, urmăriți `TODO3`-urile din **CPLangParser.g4** și **Test.java**.

- Pentru testare, rulați Test cu parametrul 3.
Fișierul de input este `input3.txt`, iar ca referință puteți folosi `reference3.txt`.
