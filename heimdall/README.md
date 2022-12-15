HEIMDALL

Heimdall é uma aplicação de dashboard de acesso e breve monitoramento de suas aplicações. Sejam servidores web, de e-mail, NAS, containers 
Docker, estejam eles em um computador local ou até mesmo na nuvem, o Heimdall consegue acessar.

Uma aplicação dessas é bastante útil quando se tem diversos serviços instalados numa mesma máquina (ou não) e gostaria de centralizá-los num 
único lugar. Com o Heimdall, com um único clique, se pode navegar entre diversas aplicações, sem precisar escrever manualmente seus domínios/
IPs e suas portas. Muito cômodo e com uma interface gráfica amigável.

DOCKER-COMPOSE:

O documento é bastante simples. 

	- Definimos a imagem a ser usada
	- Configuramos algumas variáveis de ambiente (PUID, PGID, TZ)
	- Configuramos um volume para persistência de dados (perceba que, no meu caso, instalei em um RaspberryPi)
	- Definimos as portas a serem usadas (80 e 443). Perceba que são as portas padrão para HTTP e HTTPS, visto que o Heimdall será a primeira
	página a ser exibida acessado o domínio/IP
	
