TRANSMISSION

Transmission é um cliente de BitTorrent. Sua interface é bastante simples, mas funciona perfeitamente bem. Uma 
vantagem é que ele é bastante leve e funciona muito bem, sendo perfeito para deixar baixando ou semeando no 
background de um servidor.

DOCKER-COMPOSE:

    - Definimos a imagem a ser usada
    - Definimos algumas variáveis de ambiente (PUID, PGID, TZ)
    - Configuramos alguns volumes para persistencia de dados. Note que haverá um para as configurações, um 
    para watch (tranmission começará a baixar qualquer torrent nesse diretório), e um para o destino de 
    download
    - Definimos as portas a serem usadas