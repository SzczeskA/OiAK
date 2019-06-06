# OiAK
Projekt składa się z pliku symulatora proteus oraz pliku DATA.bin zawierającego program ładowany do pamięci ROM  
Symulator jest dostępny pod linkiem https://www.labcenter.com/downloads/  
Symulację odpala się i zatrzymuje w lewym dolnym rogu okna, wówczas automatycznie wyświetla się i znika interfejs pozwalający wyświetlać stan na szynach danych.  
Podpięte szyny to CONTROL(0-5)<zapis do rejestru lub urządzenia o adresie podanym na tej szynie CONTROL(6-11)<odczyt z rejestru lub urządzenia o tym adresie, DATA(0-7)<podgląd na szynę danych procesora (jej stan nie musi ulegać zmianie przy każdej mikroinstrukcji, ponieważ niektóre elementy nie są połączone za jej pomocą), ORDER(0-7) numer aktualnie wykonywanej instrukcji (FF oznacza instrukcję zmieniającą instrukcję).  
Do urządzenia wyświetlającego stan podpięte są również: linia CONTROL(20) która w całym projekcie traktowana jest jako linia przenosząca sygnały generowane przez zegar, linia MICROOP(15) która przenosi sygnał czyszczenia licznika mikroinstrukcji.
Urządzenia wyświetlającego nie można zamykać poprzez naciśnięcie 'X' ponieważ niemożliwe będzie jego ponowne odpalenie aż do uruchomienia czystej kopii projektu.  
Po odpaleniu symcji aby rozpocząć odczyt stanów należy kliknąć 'capture' na interfejsie. 
Po wyświetleniu możliwe jest poruszanie się po obszarze za pomocą suwaka pod przyciskiem 'capture'
Aby wyświetlić stan wybranego komponentu należy odpalić symulację w jego wnętrzu i jeżeli zawiera on elementy LOGICPROBE będzie się na nich wyświetlał aktualny stan linii do których są podpięte.

