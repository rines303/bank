# Bank
Bankowosc elektroniczna


Link do Trello:

https://trello.com/invite/b/CvAX751P/d3990fa5480baeed9054ae60fd792900/bankowo%C5%9B%C4%87-elektroniczna



-Aplikacja Bankowa
	-Logowanie
	-Zakładanie konta
	-Przelewy między kontami
	-Lokaty
	-Karty kredytowe/debetowe
	-Logowanie dwuetapowe
	-Potwierdzenie przelewu kodem na mejla
	-Branie pożyczki
-Aplikacja Klient-Serwer
	-Klient łączy się przez interfejs webowy
	-Dodatkowa aplikacja do zarządzania całym systemem (uprawnienia   admina)
-Jeden serwer głowny
	-Trzy procesy
	-Pierwszy nasłuchuje ruch przychodzący od klientów
	-Drugi zarządza serwerem
	-Trzeci nasłuchuje ruch zwrotny od 2 serwerów "obliczeniowych"
	-Przechowuje informacje obciążeniu serwerów "obliczeniowych"
	-Przechowuje informacje o ilosci przetwarzanych operacji
	-Zarzdządza systemem oraz pozostałymi serwerami
	-Do niego bezpośrednio łączą się klienci
-Dwa serwery "obliczeniowe"
	-Odpowiadaja za wszystkie obliczenia
	-Maja dostęp do wspólnej bazy danych
	-Dostają zapytanie z serwera bazowego i po obliczeniu odpowiadają 	 do niego
	-Dostęp jednynie przez serwer Główny
-Jeden serwer bazodanowy
	-Przechowuje baze danych klientów
	-Dostęp jedynie przez serwery "obliczeniowe"
-Szyfrowanie całego ruchu
-Szyfrowanie sha lub przez prostę hashowanie (md5)
