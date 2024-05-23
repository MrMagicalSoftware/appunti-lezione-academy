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


