# Poradnik Velocity

### W tym poradniku wyjaśnione jest jak podpiąć silnik velocity pod serwer minecraft.

Aby Velocity działało musisz mieć conajmniej 3 podserwery, które mają zainstalowany silnik paper lub inny. (UWAGA! NIE MOŻE TO BYĆ SPIGOT!)

Velocity Pobieramy ze strony https://papermc.io/downloads wybieramy Silnik Velocity i pobieramy **ZAWSZE** najnowsza wersje.

### Wgranie Velocity na serwer Minecraft

Wgrywamy plik .jar do głównego katalogu serwera. W przypadku większości hostingów wystarczy nazwać plik ten **server.jar**, jeśli zmieniałeś tą nazwę lub masz localhosta i w pliku startowym użyłeś innej nazwy to właśnie na tą nazwę musisz zmienić.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Konfiguracja

Aby zaczac konfiguracje zrestartuj serwer i wejdz w plik velocity.toml

Krótkie objaśnienie do czego służa dane funkcje 

**bind = "0.0.0.0:25577"**  

Pozwala zmienić port serwera proxy oraz wybrać jeden z adresów IP w przypadku, gdy maszyna posiada ich więcej niż jeden.

**motd = "<#09add3>A Velocity Server"** 

Pozwala zmienić tekst wyświetlający się w liście serwerów.

**show-max-players = 500**

Maksymalna ilość slotów.

**online-mode = true**

Opcja ta sama co w przypadku serwera Minecraft. Gdy opcja jest na false gracz nie posiadający kupionej gry może wejść a gdy jest na true nie może.

player-info-forwarding-mode = "NONE"

Pozwala wybrać tryb przesyłu UUID oraz adresów IP dołączających graczy między serwerem proxy a serwerem Minecraft.

**[servers]** 
Tutaj możesz dodać swoje serwery Minecraft.

**[forced-hosts]**  

Możesz tutaj ustawić połączenia pomijające serwer lobby zależnie od podanej subdomeny. Wymagane są odpowiednie ustawienia domeny. Jeśli z tego nie korzystasz, usuń całą zawartość tej opcji.
Zostawiając linijkę **[forced-hosts]** 

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Dodawanie podserwerów

Serwer Minecraft posiada kilka opcji, które trzeba koniecznie zmienić. Najpierw zaczynamy od pliku server.properties. Gdzie znajduje się port serwera.

Port serwera musimy umieścic w kategori **"bind = "0.0.0.0:25577"** podmieniamy tam liczby po dwukropku, czyli w tym przypadku **25577**

Jeśli w pliku server.properties mamy ustawiony **"online-mode = true"** Musimy taki sam ustawić w pliku velocity.toml. Gdy mamy w server.properties ustawione na false musimy także ustawić na false.

W opcji **player-info-forwarding-mode** = "NONE"* Można ustawić:

 **"BUNGEEGUARD"** - Gdy serwer wpuszcza graczy z wersji starszej niż "1.13"
 **"MODERN"** - Gdy serwer wpuszcza graczy z wersji nowszej niż "1.13"

 Ja osobiście zalecam **modern** ze względu na to że bardzo mało serwerów stoi na wersji np 1.12.2.
 
Kolejny krok konfiguracji to ustawienie wymaganych opcji 

 **Dla serwerów wpuszczających graczy z wersji 1.13 i wyżej**  
1. W velocity.toml ustaw **'player-info-forwarding-mode'** na "MODERN"
2. W folderze config wejdź w paper-global.yml w sekcji 'velocity-support' ustaw 'enabled: true' i 'online-mode: true lub false (zależnie jak się ustawiło w server.properties)' oraz wpisz klucz znajdujący się w pliku forwarding.secret w opcji 'secret'.

**Dla serwerów wpuszczających graczy z wersji starszych niż 1.13**  
1. W velocity.toml ustaw **'player-info-forwarding-mode'** na "BUNGEEGUARD".
2. W spigot.yml ustaw 'bungeecord' na 'true'.
3. Zainstaluj plugin https://www.spigotmc.org/resources/bungeeguard.79601/ na serwerach Minecraft.
4. W configu BungeeGuarda wpisz klucz znajdujący się w pliku forwarding.secret w opcji 'allowed-tokens'

To tyle jeśli wszystko podłączyłeś zgodnie z poradnikiem sieć powinna działać

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


[Poradnik wzorowany był na innym poradniku od twórcy Helios 3991 (https://github.com/Helios3991/konfiguracja-serwera-proxy/tree/main) robiąc ten poradnik miałem na celu przetłumaczyć z profesjonalizmu na prosty język, z którym raczej każdy sobie poradzi.]

 

