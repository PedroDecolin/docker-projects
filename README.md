TEMPLATES DE PROJETOS COM DOCKER

Este repositório é focado em disponibilizar templates de docker-compose para diversos serviços, assim como instruções rápidas de como utilizá-los

Em alguns projetos eu usei como base meu próprio caso de uso, e fiz algumas configurações conforme a minha necessidade. Dessa forma, altere o que for necessário para que seus próprios problemas sejam resolvidos

Os passos iniciais se repetem em muitos desses projetos:

    - Instalar uma distro Linux leve e rápida, preferencialmente baseada em Debian

    - Instalar os pacotes do docker necessários (docker-compose e docker.io) com o comando: <code>sudo apt 
    install docker-compose docker.io</code>

    - Caso queira acessar algum serviço de fora de sua rede, terá que criar uma regra de encaminhamento da 
    porta correspondente. Não é o foco deste repositório em demonstrar como fazer isso.

    Porém, a leitura que deverá fazer quando encontrar uma regra de encaminhamento em um documento 
    docker-compose é:

    'ports:
        - 8080:80'

    O primeiro argumento, neste caso 8080, se refere a porta externa que identifica o serviço. Esta é a porta 
    que você especificará após o domínio. 
    Já o segundo argumento, neste caso 80, se refere a porta que o serviço no container usará

<<<<<<< HEAD
    - Em alguns projetos, eu utilizo um disco externo, usualmente montado em '/mnt/dados'. Deixo avisado que 
    para que o sistema rode sem nenhum problema, o disco deverá ser montado corretamente, e deverá ser 
    configurado o 'fstab' para montagem automática da unidade em uma reinicialização
=======
    - Em alguns projetos, eu utilizo um disco externo, usualmente montado em '/mnt/dados'. Deixo avisado que para que o sistema rode sem nenhum problema, 
    o disco deverá ser montado corretamente, e deverá ser configurado o 'fstab' para montagem automática da unidade em uma reinicialização
>>>>>>> ac30d920c488a353790ec08f4eebcd89be5896c4

Por ultimo, note que atualizações em algum desses serviços pode ocorrer, e alguma mudança pode ser necessária. Farei o máximo para manter os docuementos atualizados, e peço para que, se necessário uma correção, me contate
