1) git pull 
2) ctrl + s
3) wyłącz i dopiero wtedy commit/push



2. Strategia planowania dla Salem (Analiza przesłanej mapy)
  A. Obszar miejski (Gęsty, niebieski ruch):
    •	Lokalizacja stacji: Stawiaj stacje bazowe w samym centrum niebieskich plam – najbliżej miejsc o największej gęstości ruchu. 
    •	Konfiguracja i moc: W miastach stosuj mniejsze moce nadajników (dużo poniżej maksymalnych 20W) oraz mniejsze wysokości masztów, tak aby sztucznie ograniczyć rozmiar tych komórek. Dzięki temu sprawniej obsłużycie       ogromny ruch, nie „śmiecąc” sygnałem na odległe obszary. 
    •	Ochrona przed interferencjami: Aby odizolować małe komórki miejskie od siebie i od stacji zewnętrznych, bezwzględnie stosuj pochylanie anten (tilt). 
    •	Pojemność: Pamiętaj, że jeden sektor (max. 3 na stację) ze sprzętowym ograniczeniem do 6 kanałów radiowych w GSM może bezpiecznie obsłużyć 25–28 Erlangów. Jeśli niebieska plama generuje więcej ruchu, musisz postawić tam kolejną stację (zagęścić sieć). 
  B. Obszar pozamiejski i wzgórza (Kolor zielony do pomarańczowego):
    •	Lokalizacja stacji: Na terenach pomarańczowych (najwyższe wzniesienia) o dobrej widoczności optycznej stawiaj tzw. „duże komórki zasięgowe”. 
    •	Konfiguracja i moc: Tutaj możesz wykorzystać wyższe maszty (do 40 m) i maksymalną dopuszczalną moc nadajnika (20W / 13 dBW), aby jednym nadajnikiem „oświetlić” jak największy obszar o znikomym ruchu i pokryć wymagane 90% powierzchni. 
C. Zarządzanie pulą 40 kanałów:
   •	Podzielcie Wasz zbiór 40 kanałów na dwie rozłączne pule: 
      o	Pula Miejska: Używana w niebieskich strefach. Starajcie się powtarzać te same kanały w miastach tak często, jak to możliwe (agresywny reuse), monitorując mapę $C/(1+N)$, by nie schodzić poniżej 13 dB. 
      o	Pula Pozamiejska: Kanały, które zostaną niewykorzystane w miastach, przypiszcie stacjom na pomarańczowych wzniesieniach. Dzięki temu potężne nadajniki ze wzgórz, nakładające się zasięgiem na miasta, nie będą generować zabójczych interferencji dla wrażliwych komórek miejskich. 
Pamiętajcie, aby przed uruchomieniem automatycznego planowania częstotliwości (AFP) ręcznie przypisać odpowiednie pule kanałów do właściwych grup stacji, ustawić separację kanałów w sektorze na minimum 2 i docelowe $C/I = 13\text{ dB}$. 
