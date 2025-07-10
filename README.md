Ten blueprint do Home Assistanta to automatyzacja koszenia trawnika, która działa w oparciu o warunki pogodowe i elastyczne okno czasowe. Dodatkowo umożliwia wysyłanie powiadomień na urządzenie mobilne, z możliwością ich wyłączenia i edycji treści.

🧠 Co dokładnie robi ten blueprint?
🔁 Uruchamia się co 5 minut i sprawdza:
Czy aktualna godzina mieści się w określonym oknie czasowym:

Użytkownik ustawia mowing_start i mowing_end (np. 08:00–10:00).
Czy nie pada deszcz teraz:

Sprawdzany jest stan binary_sensor (np. binary_sensor.heniek_rainsensor_triggered).
Czy prognozowane opady są większe lub równe progowi:

Użytkownik ustala próg (np. 4 mm).
Sprawdzany jest sensor.opady_dzisiaj lub inny sensor prognozy.
Czy kosiarka jest w stanie „docked” (czyli gotowa do pracy).

✅ Jeśli wszystkie warunki są spełnione:
Uruchamiana jest kosiarka (lawn_mower.start_mowing).
Jeśli opcja powiadomień jest włączona, wysyłane jest powiadomienie na wybrane urządzenie mobilne (mobile_app).
📲 Powiadomienie:
Można włączyć/wyłączyć wysyłanie powiadomień (notify_enabled).
Można wpisać własną treść wiadomości (notify_message).
Powiadomienie trafia na urządzenie wybrane z listy (notify_device).
🧩 Podsumowanie funkcji:
Funkcja	Opis
Elastyczne okno czasowe	Użytkownik ustala godziny, w których koszenie może się odbyć
Warunki pogodowe	Sprawdzenie deszczu i prognozowanych opadów
Automatyczne uruchomienie	Kosiarka startuje tylko, gdy spełnione są wszystkie warunki
Powiadomienie push	Wysyłane na telefon, jeśli opcja jest aktywna
Personalizacja	Możliwość wpisania własnej treści powiadomienia
