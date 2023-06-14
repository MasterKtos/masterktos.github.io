1. Dla którego z poniższych podsystemów odpowiednia jest częstotliwość aktualizacji równa 2 Hz?
- [ ] fizyka
- [ ] sztuczna inteligencja
- [ ] rendering i animacja

<details>
<summary>Odpowiedź</summary>

> Sztuczna inteligencja

</details>

---

2. Jaki typ ogólnej architektury pokazuje poniższy rysunek?

![schemat](2_schemat.png)

<details>
<summary>Odpowiedź</summary>

> Architektura samodzielna

> Pozostałe architektury:
> - architektura współdzielona
> 
>   ![schemat](2_wspoldzielona.png)
> 
> - architektura Unreal Engine
> 
>   ![schemat](2_unreal.png)

</details>

---

3. Które z poniższych cech charakteryzują Resource Manager? [pytanie wielokrotnego wyboru]
- [ ] obsługa mediów charakterystycznych dla konsol
- [ ] zarządzanie zasobami gracza (inventory)
- [ ] obsługa wieloplatformowości silnika

<details>
<summary>Odpowiedź</summary>

> - [x] obsługa mediów charakterystycznych dla konsol
> - [x] obsługa wieloplatformowości silnika

</details>

---

4. Które z poniższych określeń powinno być użyte do scharakteryzowania silnika gry Pacman?
- [ ] nie może być użyty do zbudowania innej gry
- [ ] może być modyfikowany, żeby zbudować dowolną grę tego typu
- [ ] może być użyty do zbudowania zupełnie dowolnej gry

<details>
<summary>Odpowiedź</summary>

> nie może być użyty do zbudowania innej gry

</details>

---

5. Jaki typ architektury game objectu pokazuje poniższy rysunek?

![schemat](13_schemat.png)

- [ ] architektura czysto komponentowa
- [ ] architektura używająca kompozycji
- [ ] architektora używająca uogólnionych komponentów
- [ ] monolityczna hierarchia klas

<details>
<summary>Odpowiedź</summary>

> monolityczna hierarchia klas

> Z prezentacji (7):
>
> Architektury object-centric:
> - **nieobiektowa** - specjalizowane struktury przechowujące konkretne typy obiektów
> - **monolityczna hierarchia klas**
> - używająca **kompozycji**
> 
>   ![schemat](5_kompozycja.png)
> - używająca **uogólnionych komponentów**
> 
>   ![schemat](5_uogolnione.png)
> - **czysto komponentowa**
> 
>   ![schemat](5_czysta.png)

</details>

---

6. Wadą którego z poniższych rozwiązań obliczania dt (delta time) jest bardzo duży wpływ czasu wykonania poprzedniej ramki mogący doprowadzić do oczekiwania z powodu zależności między podsystemami(?)
- [ ] Δt obliczane jako średnia z kilku poprzednich wartości
- [ ] Δt obliczane na bazie ostatniej ramki
- [ ] stałe Δt

<details>
<summary>Odpowiedź</summary>

> Δt obliczane na bazie ostatniej ramki

> Z prezentacji:
> 
> Δt jest zmierzone jako różnica między chwilą rozpoczęcia a zakończenia obliczeń poprzedniej ramki.
>
> Rozwiązanie używane w większości gier.
>
> Może doprowadzić, po wystąpieniu zbyt długiej ramki, do powstawania serii ramek, które są dwa razy dłuższe, niż powinny, ponieważ zależności między podsystemami powodują oczekiwanie

</details>

---

7. Które z poniższych warst silnika gry znajdują się między Platform Independence Layer a Low-Level Renderer?
- [ ] Resources
- [ ] Drivers
- [ ] Front-End

<details>
<summary>Odpowiedź</summary>

> Resources

</details>

---

[mocno niewyraźne]
8. Na czym polega strumieniowanie świata podczas ładowania(?) ??? ???:
- [ ] użycie kilku obszarów pamięci, które mogą przechowywać dane całego chunka
- [ ] użycie ??? małego ????
- [ ] jednoczesne(?) ????

<details>
<summary>Odpowiedź</summary>

> jeżeli chodzi ogólnie o strumieniowanie, to użycie małego obszaru pamięci w porównaniu do całościowego rozmiaru pliku (rezerwacja pamięci tylko na ułamek swojej wielkości)

> Z prezentacji (7):
> 
> Ładowanie danych świata:
> - ładowanie proste - z użyciem ekranów ładowania
> - użycie *air lock* - bardzo małe chunki świata, które zajmują gracza na czas ładowania dużego chunka
> - strumieniowanie świata - użycie kilku obszarów pamięci, które mogą przechowywać dane całego chunka

</details>

---

9. Jak nazywa się separacja core silnika od assetów?
- [ ] data-driven architecture
- [ ] entity-component system
- [ ] pure component model

<details>
<summary>Odpowiedź</summary>

> data-driven architecture

</details>

---

10. Jak można scharakteryzować użycie checkpointów jako metody zapisu stanu gry?
- [ ] wymaga bardzo dużej ilości danych w pliku save
- [ ] niewygodna dla gracza
- [ ] trudne w implementacji przez programistę

<details>
<summary>Odpowiedź</summary>

> niewygodna dla gracza

</details>

---

11. Działanie której z wymienionych podzielonych pętli gry pokazuje poniższy rysunek?

![schemat](11_schemat.png)

*(odpowiedzi nie było na screenie, więc te tutaj podane są tylko z domysłu)*
- [ ] SIMD
- [ ] fork i join
- [ ] podsystemy w wątkach
- [ ] zadania

<details>
<summary>Odpowiedź</summary>

> Podsystemy w wątkach

> Z prezentacji (09):
> 
> Rozbicie czynności na zadania, które mogą być wykonywane równolegle:
> - SIMD
>
> 	![schemat](11_simd1.png)
>   ![schemat](11_simd2.png)
> - fork i join
> 	
> 	![schemat](11_fork.png)
> - podsystemy w wątkach (j.w.)
> - zadania (jobs)
> 	
> 	![schemat](11_jobs.png)
> 
> Wykonywanie asynchroniczne

</details>

---

12. Które z poniższych cech są wspólne dla wszystkich silników gier? [pytanie wielokrotnego wyboru]
- [ ] rendering 3D dla gier 3D
- [ ] wysokiej jakości animacje szerokiego broni gracza
- [ ] dokładna detekcja kolizji
- [ ] HID

<details>
<summary>Odpowiedź</summary>

> - [x] rendering 3D dla gier 3D
> - [x] HID

</details>

---

### Schemat architektury silnika gier

![engine architecture](RuntimeGameEngineArchitecture.png)
