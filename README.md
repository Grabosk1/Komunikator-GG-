# Komunikator typu GG 

### 1. Temat zadania

Tematem naszego projektu był komunikator internetowy typu ”Gadu-Gadu”. Podstawową funkcjonalnościa
programu jest jest przesyłanie wiadomości miedzy dwomą użytkownikami w sposób bezpośredni.
Użytkownicy mogą odczytać całe dotychczasowe konwersacje, dodatkowo są informowani o
nieprzeczytanych wiadomościach . Serwer został napisany z wykorzystaniem języka C, client z
wykorzystaniem języka Python.

### 2. Opis protokołu komunikacyjnego

Projekt opiera na się wymienie pakietów między klientem, a serwerem w sposób zbliżony jak na zajęciach.
Specyfikacja projektu skłoniła nas do wykorzystania ‘rozkazów’ LOGIN, SEND, DEAD jako formy komunikacji
między serwerem, a klientem.

### 3. Opis implementacji

Server obsługuje wątek każdego clienta za pomocą metody clientHandler() , metoda da rozpoznaje rozkazy
wysyłane przez użytkownika chatu i je obsługuje. W przypadku kiedy użytkownik jest offline, server zapisuje
wiadomości lokalnie w folderze serverData. Kiedy użytkownik zaloguje się, nieodczytane wiadomości są do
niego wysyłane, a następnie usuwane z folderu serverData.
Client lokalnie zapisuje konwersacje z innymi użytkownikami w folderze conversations – w plikach
użytkownikX_UżytkownikY.
Prosty interfejs graficzny został stworzony za pomocą biblioteki Tkinter

### 4. Sposób kompilacji, uruchomienia i obsługi programów projektu

Zanim uruchomimy Clientów należy skompilować program serwera poleceniem ‘gcc -pthread’ a następnie
uruchomić go. Przed uruchomieniem programu Clienta w jego kodzie należy zmienić ip oraz port, bazowy
port to 8011. Clienci uruchamiani są za pomocą terminala ‘python client.py’ również w terminalu należy
podać nazwe użytkownika używana i widoczną przez innych. Po wpisaniu nazwy użytkownika pojawia się
okno menu głównego. W menu głównym użytkownik jest informowany o nieprzeczytanych wiadomościach,
zarówno o ich autorze jak i ilości. Po wpisaniu nazwy innego użytkownika i kliknięcie guzika ‘zatwierdź’
użytkownik przechodzi do okna chatu w którym wyświetlana jest cala konwersacja
