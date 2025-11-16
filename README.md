# Michał Muzyka 2.3 – Sprawozdanie Lab 6


### Tworzę plik YAML, który będzie manifestem dla Deployment wykorzystującego obraz serwera Nginx o wersji 1.9 z 5 replikami. Edytuję plik i ustawiam strategię aktualizacji RollingUpdate z nie więcej niż 2 podami niedostępnymi w tym samym czasie podczas aktualizacji. Dodaję również adnotację opisującą wersję aplikacji i etykietę typ=proxy.

![alt text](images/image.png)



### Uruchamiam Deployment. Wyświetlam wszystkie zasoby w bieżącym namespace z etykietą typ=proxy. Jest problem z pobraniem obrazu.

![alt text](images/image-1.png)



### Sprawdzam jednak konfigurację obiektu w formacie YAML, czy ustawione parametry są prawidłowe. Są prawdiłowe.
![alt text](images/image-2.png)
![alt text](images/image-3.png)



### Weryfikuję, czy adnotacja CHANGE-CAUSE została poprawnie zapisana w historii wdrożenia. Została zapisana poprawnie.

![alt text](images/image-4.png)



### Dodatkowo, poza zadaniem, aby wdrożenie jednak zostało uruchomione poprawnie, zmieniam wersję obrazu z 1.9 na 1.17, zmieniam też adnotację.

![alt text](images/image-5.png)



### Aplikuję zmiany. Pody tym razem działają.

![alt text](images/image-6.png)



### Weryfikuję zmiany obiektu w formacie YAML. Dokonane zmiany są widoczne.

![alt text](images/image-7.png)
![alt text](images/image-8.png)



### Weryfikuję historię wdrożenia. Widoczna jest druga wersja.

![alt text](images/image-9.png)
