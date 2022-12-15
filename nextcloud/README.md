NEXTCLOUD

O Nextcloud nada mais é do que uma nuvem pessoal. Ele tem funcionalidades semlhantes a outras nuvens, como 
OneDrive, Dropbox, Google Drive, etc. Porém, com a grande diferença de que pode ser instalado onde quiser.

Sua funcionalidade principal é atuar como um NAS, ou seja, armazenar seus dados em um computador conectado na 
rede. Porém, graças à grande comunidade, tem-se diversos plugins instaláveis que expandem suas funções. Ele 
conta com: calendário sincronizável, cliente para e-mail, vizualizador de mídias, suíte office básica, 
aplicativo de mensagem interno e mais.

DOCKER-COMPOSE:

Neste caso, precisamos de dois containers. Um para o banco de dados e outro para o nextcloud em si. 
Para o banco de dados:

 - Definimos a imagem a ser usada
 - Definimos a porta a ser usada
 - Configuramos um volume para a persistencia de dados
 - Configuramos algumas variaveis de ambiente (PUID, PGID, TZ)
 - Configuramos informações do banco: senha admin, base de dados, usuário e senha para este usuário

Para o Nextcloud:

    - Definimos a imagem a ser usada
    - Definimos a porta a ser usada
    - Configuramos um volume para um disco externo
    - Definimos que este container está linkado com outro com 'links' (mariasb)
    - Configuramos as credenciais de acesso ao banco. Note que aqui, você deverá colocar exatamente as mesmas 
    informações definidas no container do banco. MYSQL_HOST é o nome do serviço do banco de dados
    - Configuramos um usuário administrador e uma senha para ele
    - Configuramos um domínio como confiável, para acessarmos o Nextcloud usando ele