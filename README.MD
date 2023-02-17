# Azeno Flashcards

## Algorytm postępowania:

1. Czy potrzebujemy Django App?
   1. `python manage.py startapp <app_name>`
   2. dodaj do installed apps -> settings.py
2. Czy potrzebujemy do tego dane?
   1. narysuj ERD diagram do danych
   2. implementacja w models.py
   3. `python manage.py makemigrations <app_name>`
   4. `python manage.py migrate <app_name>`
   5. unit tests -> pytest
3. Czy chcemy zarządzać tym zasobem z CSM (django admin)
   1. rejestrujemy modele w admin.py
4. Czy wystawiamy dane w widoku?
   1. tworzymy plik serializers.py (sprowadzanie danych do określonego formatu + walidacja)
   2. unit tests -> pytest
5. Tworzymy widoki (logikę) -> jeżeli pełny CRUD to ViewSet
   1. dobieramy klasę do obsługi widoku [wyszukiwarka widoków](https://www.cdrf.co)
   2. widok musi zwracać response lub redirect
   3. logika uprawnień permissions.py
   4. unit tests -> pytest
6. Tworzymy lokalny router
   1. w pliku urls.py tworzymy urlpatterns lub router
   2. podpinamy lokalne urls do globalnych urls -> config/urls.py
   3. unit tests -> pytest (też do widoku)
7. Sprawdzenie dokumentacji open API (Swagger)
8. Postman i tworzenie kolekcji
   1. wyeksportowanie kolekcji do repozytorium