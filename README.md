# appunti-lezione-academy



Esempio di esercizio in python che stampa il numero maggiore presi
in ingresso due numeri



```
#prendi in ingresso 2 numeri

numero_1 = int ( input ("inserisci un numero "))
numero_2 = int ( input ("inserisci un numero "))

if numero_1 > numero_2 :
    print(numero_1)
else :
    print(numero_2)

```


# ESERCIZIO 2

```
# Esercizio: Tabellina di un numero
numero = int(input("Inserisci un numero: "))
i = 1
while i <= 10:
    print(f"{numero} x {i} = {numero * i}")
    i += 1
```


# ESERCIZIO 3


```
altezza = int ( input("inserisci l'altezza  "))
print("Disegno un albero di altezza " , altezza)
cont =1

for i in range(1, altezza +1 ):
    j = 0 
    while j < cont :
        print("*" , end=" ")
        j +=1
    
    print()
    cont+=1

```


# ESERCIZIO 4


```
to_do_list =[]


for i in range(5):
    to_do_list.append(input(f"inserisci il task {i +1}   "))

print("#######_____________#########")
print(to_do_list)
print("#############################")


```



____________________________


```

import random

def genera_numero():
    return random.randint(1 ,6)


def playing():
    numero_1 = genera_numero()
    numero_2 = genera_numero()
    print(f"valori {numero_1}  {numero_2}")
    if(numero_1 + numero_2 == 7):
        print("hai vinto")
    else:
        print("hai perso")
    

is_playing = True

while is_playing  :

    print("Vuoi giocare ai dadi ? y/N")
    risposta_utente = input()

    if(risposta_utente == "y"):
        print("ok iniziamo a giocare ... ..")
        playing()
    else:
        print("ciao ciao ")
        is_playing = False

```


#Esercizio

```
import hashlib


def cifra_md5(word):
    ris = hashlib.md5(word.encode())
    return ris.hexdigest()

is_running = True

while is_running:
    user_input = input("press y to encrypt ")
    if(user_input == "y"):
        print("insert a word")
        print(cifra_md5(   input()   ))
    else:
        print("bye bye")
        is_running=False

```


_____________________________________________________________________________________________


```
'''
Esecizio biblioteca python :


'''


class Libro:
    def __init__(self, titolo , autore , anno_pubblicazione  ):
        self.__disponibilita = True
        self.__titolo = titolo
        self.__autore = autore
        self.__anno_pubblicazione = anno_pubblicazione


    def set_disponibilita(self , disp):
        self.__disponibilita = disp

    def get_titolo(self):
        return self.__titolo

    def get_disponibilita(self) -> bool :
        return self.__disponibilita

    def get_autore(self):
        return self.__autore

    def get_anno_pubblicazione(self):
        return self.__anno_pubblicazione

    def __str__(self) -> str:
        return f"{self.__titolo} {self.__autore}  {self.__anno_pubblicazione} {self.__disponibilita}"




class Biblioteca:
    def __init__(self):
        self.__libri  = [] 

    def aggiungi_libro(self , libro : Libro):
        self.__libri.append(libro)

    def __str__(self) -> str:
        return "".join(str(element) + "\n" for element in  self.__libri)

    # rimuove un libro dalla biblioteca in base al titolo
    def rimuovi_libro(self , titolo):
        for book in self.__libri :
            if book.get_titolo() == titolo:
                self.__libri.remove(book)
                return 


    def cerca_libro(self , titolo):
        for book in self.__libri :
            if book.get_titolo() == titolo:
                return book
        return None

    ################## TO FIX IT ############################
    def cerca_libri_con_contains(self , title):
        ris = []
        for book in self.__libri :
            print(f"here --> {book}")
            if book.get_titolo() in title:
                print("i was here")
                ris.append(book)
        return ris


    ##prestito libro
    def prestito_libro(self , titolo):
        # 1 - devi verificare che esiste il titolo
        # 2 - se esiste il titolo devi verificare che il libro sia disponibile

        libro = self.cerca_libro(titolo) # richiamo la funzione della riga 55 cerca_libro

        if  libro and libro.get_disponibilita():
            print(f"ok prendi in prestito {libro.get_titolo()}")
            libro.set_disponibilita(False)
        else:
            print("libro non trovato oppure in prestito")


    ##restituisci libro

    def restituisci_libro(self, titolo):
        libro = self.cerca_libro(titolo)
        if libro and not libro.get_disponibilita():
            print("lIBRO RESTITUITO")
            libro.set_disponibilita(True)
        else:
            print("non trovato...")



    ##mostra libri disponibili

    def mostra_libri_disponibili(self):
        for book in self.__libri:
            if book.get_disponibilita() :
                print(book)
           



####################################################

book1 = Libro("The secrets 1" , "MR jones" , 2010)
book2 = Libro("The secrets 2" , "MR jones" , 2010)
book3= Libro("The secrets 3" , "MR jones" , 2010)
book4= Libro("The book" , "MR jones" , 2010)




biblioteca = Biblioteca()
biblioteca.aggiungi_libro(book1)
biblioteca.aggiungi_libro(book2)
biblioteca.aggiungi_libro(book3)
biblioteca.aggiungi_libro(book4)

print(biblioteca)

biblioteca.prestito_libro("The book")
biblioteca.prestito_libro("The book")

print("####################")
print(biblioteca)


biblioteca.restituisci_libro("The book")


print("####################")
print(biblioteca)



#print(biblioteca.cerca_libro("The secrets 2"))

#print(biblioteca.cerca_libri_con_contains("secrets"))


```




















