# KursUNI
Przed uruchomieniem:
- w backend/index.js dodaj numer telefonu znajdujący się w bazie

Uruchomienie programu:
1. w terminalu w ścieżce KursUNI/backend/ wpisać polecenie:
- npm install
- node index.js
a następnie ustawić port na publiczny (make public)

2. w terminalu w ścieżce KursUNI/front/ wpisać polecenie:
- gp env -u VUE_APP_SERVER_URL
- gp env VUE_APP_SERVER_URL=$(gp url 3000)
- eval $(gp env -e)
- npm install
- npm run serve

Co zostało dodane dodatkowo:
- Licznik odliczający za ile powinno nastąpić połączenie
- Licznik pokazujący czas trwania połączenia
