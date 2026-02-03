# Arduino Traffic Light Controller 🚦

Ten projekt to symulacja zaawansowanego systemu sygnalizacji świetlnej oparta na mikrokontrolerze Arduino. Program steruje sekwencją 12 diod LED, realizując cykliczny harmonogram zmiany świateł (np. dla skrzyżowania wieloetapowego).

## 📋 Opis działania

System działa w pętli nieskończonej, realizując 3 główne fazy ruchu. Każda faza aktywuje określoną grupę diod (sygnalizatorów), wyłączając pozostałe.

### Harmonogram cyklu (Logic Flow):

1.  **Faza 1 (Czas trwania: 10s)**
    * **AKTYWNE:** Piny 12, 11, 10, 4.
    * *Zastosowanie:* Np. Zielone światło dla drogi głównej + przejścia dla pieszych A.
2.  **Faza 2 (Czas trwania: 5s)**
    * **AKTYWNE:** Piny 9, 8, 7, 6.
    * *Zastosowanie:* Np. Światło żółte (ostrzegawcze) lub faza przejściowa dla lewoskrętów.
3.  **Faza 3 (Czas trwania: 10s)**
    * **AKTYWNE:** Piny 13, 5, 3, 2.
    * *Zastosowanie:* Np. Zielone światło dla drogi podporządkowanej + przejścia dla pieszych B.

## 🛠️ Wymagania sprzętowe (Hardware)

Aby zbudować ten układ, potrzebujesz:

* **Mikrokontroler:** Arduino Uno / Nano / Mega (lub klon).
* **Diody LED:** 12 sztuk (Kolory wedle uznania: Czerwone, Żółte, Zielone).
* **Rezystory:** 12 x 220Ω (lub 330Ω) – niezbędne do ochrony diod.
* **Płytka stykowa (Breadboard).**
* **Przewody połączeniowe (Jumper Wires).**

## 🔌 Schemat połączeń (Pinout)

Każda dioda powinna być podłączona w szeregu z rezystorem do odpowiedniego pinu cyfrowego oraz do masy (GND).

| Pin Arduino | Komponent | Opis stanu |
| :--- | :--- | :--- |
| **D13** | LED (Grupa 3) | Faza 3 |
| **D12** | LED (Grupa 1) | Faza 1 |
| **D11** | LED (Grupa 1) | Faza 1 |
| **D10** | LED (Grupa 1) | Faza 1 |
| **D9** | LED (Grupa 2) | Faza 2 |
| **D8** | LED (Grupa 2) | Faza 2 |
| **D7** | LED (Grupa 2) | Faza 2 |
| **D6** | LED (Grupa 2) | Faza 2 |
| **D5** | LED (Grupa 3) | Faza 3 |
| **D4** | LED (Grupa 1) | Faza 1 |
| **D3** | LED (Grupa 3) | Faza 3 |
| **D2** | LED (Grupa 3) | Faza 3 |

## 💻 Technologie

* **Język:** C++ (Arduino API)
* **Środowisko:** Arduino IDE

## 🚀 Jak uruchomić?

1.  Pobierz i zainstaluj [Arduino IDE](https://www.arduino.cc/en/software).
2.  Podłącz płytkę Arduino do komputera przez USB.
3.  Zbuduj układ na płytce stykowej zgodnie z tabelą pinów.
4.  Otwórz plik `.ino` w Arduino IDE.
5.  Wybierz odpowiedni port COM i model płytki.
6.  Kliknij **Wgraj (Upload)**.

---
*Autor: [Twój Nick/Imię]*
