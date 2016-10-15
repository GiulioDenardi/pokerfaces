# Concepção do Projeto

### O problema a ser resolvido
A ideia do PokerFaces é disponibilizar uma plataforma de realidade aumentada de Poker, onde usuários interessados em jogar Poker podem se encontrar utilizando o aplicativo de forma simples e rápida.

A aplicação também possuirá uma integração com serviços externos de informações sobre campeonatos (possibilitando links para inscrições e também possibilitando que um usuário marque que irá para aquele campeonato) e informações sobre campeonatos e jogos que irão ao ar na televisão (em que usuários poderão marcar de comer uma pipoquinha ou fazer um churrasco para assistir o campeonato juntos).

A intenção é que diversas informações sobre o esporte sejam centralizadas em um único app e possibilite a integração de pessoas entre si, mesmo sem um baralho e fichas.

### A metodologia a ser empregada
Pretendemos desenvolver cada vez mais nosso projeto para que possamos realizar um melhor trabalho a ser entregue. Porém, para um MVP, pensamos nas seguintes funcionalidades:

Temos interesse que nosso app funcione tanto em tablets quanto smartphones. Para isso, iremos utilizar ferramentas que já estejam prontas que independam do tamanho da tela do aparelho (como, por exemplo, o Material Design). (Confirmar**)

- Um sistema background de monitoramento de mesas a serem abertas próximas a você, que irá utilizar métodos de geolocalização para definir se o usuário está próximo ou não. Para isso, também precisaremos de integração com a conexão de internet pois os dados das mesas estarão centralizadas em um servidor a parte, e a resposta para a pergunta "existem mesas perto?" serão enviadas via Web Services.
- Teremos também um sistema de "fechamento de mesas", onde, para que os usuários possam finalizar o jogo, eles precisam enviar uma foto do jogo de mesa com os participantes, e então poderão escalar os vencedores da mesa. Isso nos possibilitará utilizar o sistema de câmera e aumentar o engajamento do usuário no app.
- Também teremos um sistema de notificações que terá próximos torneios de poker criados ou não pelos usuários, outro que terá os usuários mais bem rankeados, os que mais jogam, possíveis campanhas, etc. Esses serviços estarão em um servidor separado que irá conter esses e outros serviços utilizados pelo app.
- Haverá um cadastro de usuários com informações mínimas para que ele possa participar dos campeonatos, criar mesas, etc.
- Em cada perfil de usuário, será exibido além das informações básicas e estatísticas de jogos, um atributo relativo ao número de partidas anuladas, i.e. quantas partidas LIVE ou STAKES (descritas abaixo) aquele jogador participou nas quais não houve consenso sobre a vitória de um jogador/equipe. 

Nosso servidor que realizará o agendamento de mesas, torneios, rankeamento, etc. irá integrar-se com um banco de dados relacional, que irá persistir os dados da aplicação. A troca de dados será feita via JSON.

O app também possuirá dois tipos de funcionalidade: a mesa LIVE e a mesa DIGI.
- A mesa **LIVE** representa mesas em que os jogadores possuem as fichas e baralhos reais para jogarem, e não precisam do auxílio do app para jogar o jogo. Apenas irão dizer quais usuários perdem ao longo do jogo.
- Com o auxílio da mesa **STAKES**, usuários que já tenham em mãos um baralho podem controlar as apostas através do app. A cada rodada, cada usuário poderá optar pelo número de fichas que deseja apostar ou se deseja abandonar a aposta. No final da rodada os jogadores devem concordar sobre quem foi o ganhador. Caso não haja consenso a partida é anulada e os jogadores recebem um 'bad remark' de jogo não finalizado, contribuindo para a comunidade de jogadores escolher preferencialmente outros jogadores que não tenham partidas anuladas.
- Já a mesa **DIGI** refere-se a usuários que não possuem baralho e portanto jogarão utilizando o app. A mecânica e as regras do jogo para essa modalidade ainda estão sendo pensadas, porém espera-se que gaste pouca bateria do aparelho, e que o usuário só possa se entrar na mesa se garantir que estará com bateria até o final do jogo. Também ireoms deixar o gerenciamento do jogo, neste caso, para o servidor.

Procurando em stores, não encontramos um programa parecido. Em geral, no mercado, temos apenas jogos de poker em que você joga com outras pessoas ou com a IA, portanto, estamos criando um projeto novo no mercado. (André, dar uma confirmada, por favor).


### Testando e exportando

Em um primeiro momento o teste será feito pelos desenvolvedores em conjunto com voluntários dentro da UFABC.
Para avaliar a integridade do app e até sua receptividade, em um segundo momento iremos disponibilizá-lo para o público, em grupos de poker, etc. para analisar se as pessoas se interessam pela ideia.
