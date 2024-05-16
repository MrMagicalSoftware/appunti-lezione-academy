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







