# Poradnik Velocity

### W tym poradniku wyjaśnione jest jak podpiąć silnik velocity pod serwer minecraft.

Aby Velocity działało musisz mieć conajmniej 3 podserwery, które mają zainstalowany silnik paper lub inny. (UWAGA! NIE MOŻE TO BYĆ SPIGOT!)

Velocity Pobieramy ze strony https://papermc.io/downloads wybieramy Silnik Velocity i pobieramy **ZAWSZE** najnowsza wersje.

### Wgranie Velocity na serwer Minecraft

Wgrywamy plik .jar do głównego katalogu serwera. W przypadku większości hostingów wystarczy nazwać plik ten **server.jar**, jeśli zmieniałeś tą nazwę lub masz localhosta i w pliku startowym użyłeś innej nazwy to właśnie na tą nazwę musisz zmienić.

### Konfiguracja

Aby zaczac konfiguracje zrestartuj serwer i wejdz w plik velocity.toml

Krótkie objaśnienie do czego służa dane funkcje 
bind = "0.0.0.0:25577"
Pozwala zmienić port serwera proxy oraz wybrać jeden z adresów IP w przypadku, gdy maszyna posiada ich więcej niż jeden.
motd = "<#09add3>A Velocity Server"
Pozwala zmienić tekst wyświetlający się w liście serwerów.
show-max-players = 500
Maksymalna ilość slotów.
online-mode = true
Opcja ta sama co w przypadku serwera Minecraft. Gdy opcja jest na false gracz nie posiadający kupionej gry może wejść a gdy jest na true nie może. 
player-info-forwarding-mode = "NONE"
Pozwala wybrać tryb przesyłu UUID oraz adresów IP dołączających graczy między serwerem proxy a serwerem Minecraft.
"[servers]"
Tutaj możesz dodać swoje serwery Minecraft.

### Dodawanie podserwerów
