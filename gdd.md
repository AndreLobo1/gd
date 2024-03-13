## 5.1. Casos de Teste
Nesta seção, apresentamos uma série de casos de teste detalhados que foram desenvolvidos para avaliar o funcionamento e a integração das partes do jogo. Cada caso de teste é projetado para testar uma funcionalidade específica do jogo, desde a inicialização até a interação com personagens e transições entre telas.

Os casos de teste são organizados em uma tabela que contém informações sobre a pré-condição, a descrição do teste e a pós-condição. Cada caso de teste é numerado para facilitar a referência e a rastreabilidade durante o processo de teste.

Esses casos de teste são essenciais para garantir que o jogo atenda aos requisitos estabelecidos e funcione corretamente em diferentes cenários. Eles fornecem uma estrutura sistemática para identificar e corrigir possíveis falhas ou problemas de desempenho, garantindo uma experiência de jogo suave e satisfatória para os usuários finais.

### Configuração de Ambiente de Teste

Antes de iniciar os testes, é necessário configurar adequadamente o ambiente de teste para garantir resultados precisos e reprodutíveis. Esta seção descreve os detalhes sobre a configuração do ambiente de teste, incluindo hardware, software e outras configurações relevantes.

### Dispositivos de Teste

- **Modelo:** Dell Latitude 3440
- **Processador:** 13ª Geração Intel(R) Core(TM) i5-1335U @ 1.30 GHz
- **RAM Instalada:** 16,0 GB (utilizável: 15,7 GB)
- **Tipo de Sistema:** Sistema operacional de 64 bits, processador baseado em x64

### Especificações do Windows

- **Edição:** Windows 10 Pro
- **Versão:** 22H2

### Navegador

- **Navegador:** Chrome
- **Versão:** 122.0.6261.112 (Compilação oficial) (64 bits)

## 5.1. Casos de Teste

| #   | Título do Caso de Teste                            | Pré-condição                                            | Descrição do Teste                                                                                                           | Pós-condição                                                                                          |
| --- | --------------------------------------------------- | ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| 1   | Teste de Início do Jogo                             | O jogo foi iniciado                                     | Mover o cursor até o botão "play" e clicar uma vez sobre ele                                                                  | O botão "play" deve ser afetado por um efeito visual indicando que o jogador passou o cursor por cima dele e o jogador deve ser enviado para a tela de controles do jogo. |
| 2   | Teste de Transição para Tela de Escolha de Personagem | O jogo está na tela de controles                    | Mover o cursor até o botão "play" e clicar uma vez sobre ele                                                                  | O botão "play" deve ser afetado por um efeito visual indicando que o jogador passou o cursor por cima dele e o jogador deve ser enviado para a tela de escolha de personagens. |
| 3   | Teste de Escolha de Personagem                      | O jogo está na tela de escolha de personagem            | Escolher qualquer um dos quatro personagens e clicar uma vez sobre o escolhido                                                  | Os personagens devem ser afetados por um efeito indicando que o jogador passou o cursor por cima dele e após escolher o jogador deve ser enviado para a tela do jogo com o personagem escolhido. |
| 4   | Teste de Trilha Sonora                              | O jogo está em andamento                               | Não é necessária nenhuma ação do jogador                                     | A trilha sonora do jogo deve tocar constantemente enquanto o jogador estiver na aba do jogo                                                                                                     |
| 5   | Teste de Movimentação do Personagem                 | O jogo está em andamento                               | Acionar todas as 4 teclas do teclado em um ambiente aberto dentro do jogo                                                     | O personagem deve se mover em velocidade constante através das teclas direcionais do teclado conforme as direções das mesmas, e o som de passos deve ser ativado durante a movimentação. |
| 6   | Teste de Interação com NPCs                         | O jogo está em andamento e o personagem está próximo ao NPC | Se aproximar do NPC e apertar a tecla de interação "E"                                                                        | O NPC deve mostrar um balão de fala indicando a tecla "E" e, ao interagir, o NPC deve falar com o jogador através de outro balão de fala. Além disso, o balão de fala deve mostrar uma foto do NPC ao lado dele. Sempre que o jogador acionar a tecla de interação "E" dentro de um diálogo, o som de interação deve ser ativado. |
| 7   | Teste de Transição ao Vencer o Minigame             | O jogo está na tela do primeiro minigame                | Jogar o minigame e vencer                                                                                                    | O jogador deve ser redirecionado para a porta de entrada dentro do escritório Unilever.              |
| 8   | Teste de Transição ao Perder o Minigame             | O jogo está na tela do primeiro minigame                | Jogar o minigame e perder                                                                                                    | O jogo deve exibir uma tela de gameover com um botão de "Recomeçar". Após clicar no botão, o jogador deve recomeçar o jogo do início. |
| 9   | Teste de Recomeçar o Jogo Após Gameover            | O jogo está na tela de gameover do primeiro minigame   | Mover o cursor até o botão de "recomeçar" e clicar uma vez sobre ele                                                          | O botão "recomeçar" deve ser afetado por um efeito indicando que o jogador passou o cursor por cima dele e ao clicar uma vez, o minigame deve recomeçar. |
| 10  | Teste de Colisões no Jogo                           | O jogo está em andamento e o jogador está se movendo   | Tentar atravessar as estruturas do mapa como prédios, árvores, postes, bancos, lixos, NPCs e demais estruturas                | O personagem não deve atravessar nenhum item do cenário, sendo barrado caso chegue perto demais. Ele deve passar por trás de determinados objetos como árvores ou postes, mas não deve passar por trás de suas bases que os ligam ao chão. |
| 11  | Teste de Entrada em Diferentes Ambientes           | O jogo está em andamento                               | Mover o personagem em direção à porta do escritório Unilever, salão Clear, sorveteria Kibom e lavanderia Omo                | O personagem deve entrar nos ambientes normalmente.                                                   |

## Resultados dos Testes

### Teste de Início do Jogo
- O botão "play" respondeu corretamente ao ser clicado, e o jogador foi redirecionado para a tela de controles do jogo conforme esperado.

### Teste de Transição para Tela de Escolha de Personagem
- O botão "play" funcionou corretamente, enviando o jogador para a tela de escolha de personagem após ser clicado.

### Teste de Escolha de Personagem
- A escolha de personagem funcionou como esperado, com os personagens sendo destacados e o jogador sendo enviado para a tela do jogo com o personagem escolhido.

### Teste de Trilha Sonora
- A trilha sonora do jogo tocou continuamente enquanto o jogador estava na aba do jogo.

### Teste de Movimentação do Personagem
- A movimentação do personagem funcionou conforme esperado, com o personagem respondendo às teclas direcionais do teclado e o som de passos sendo ativado durante o movimento.

### Teste de Interação com NPCs
- As interações com os NPCs foram parcialmente bem-sucedidas. O NPC da entrada do escritório está com a foto ao lado do balão de fala cortada, além disso, o primeiro NPC pode ser atravessado pelo jogador.

### Teste de Transição ao Vencer o Minigame
- Após vencer o minigame, o jogador foi redirecionado para a porta de entrada dentro do escritório Unilever conforme o esperado.

### Teste de Transição ao Perder o Minigame
- Ao perder o minigame, o jogo exibiu corretamente a tela de gameover, permitindo que o jogador recomeçasse o jogo.

### Teste de Recomeçar o Jogo Após Gameover
- O botão "recomeçar" na tela de gameover funcionou corretamente, permitindo que o jogador recomeçasse o minigame.

### Teste de Colisões no Jogo
- Durante o teste, foram encontrados alguns problemas com colisões inadequadas do personagem com certas estruturas do mapa, que precisam ser corrigidos.

### Teste de Entrada em Diferentes Ambientes
- A entrada nos diferentes ambientes do jogo foi bem-sucedida, com o personagem entrando nos ambientes sem dificuldades.

##  Problemas Encontrados

### Problema de Colisão com Estruturas do Mapa
- **Descrição:** Durante o teste de colisões no jogo, o personagem foi capaz de atravessar certas estruturas do mapa, como árvores, arbustos e NPCs.
- **Gravidade:** Média
- **Status:** Pendente de correção.
- **Observações:** Parece haver problemas com as colisões definidas para esses objetos, resultando em comportamento não esperado do personagem.

### Problema de Exibição da Foto do NPC do Escritório Unilever
- **Descrição:** Durante o teste de colisões no jogo, o NPC apresentou a sua foto ao lado do balão de fala como o esperado, porém a foto está cortada.
- **Gravidade:** Baixa
- **Status:** Pendente de correção.
- **Observações:** Parece haver problemas com a foto do NPC, resultando em comportamento não esperado do mesmo.

## Conclusão
Os casos de teste apresentados nesta seção ofereceram uma visão abrangente do funcionamento do jogo, fornecendo feedbacks valiosos para o aprimoramento contínuo do projeto. Embora tenhamos alcançado sucesso em muitos testes, alguns problemas foram identificados durante o processo, destacando áreas que podem exigir ajustes adicionais.

Durante os testes, observamos problemas relacionados à colisão com estruturas do mapa e à exibição inadequada da foto do NPC no escritório Unilever. Esses problemas são considerados de gravidade média e baixa, respectivamente, e estão pendentes de correção em futuras iterações do desenvolvimento.

Além disso, reconhecemos a importância de testes adicionais para validar novas funcionalidades e melhorias implementadas no jogo. Em resumo, os casos de teste desempenham um papel fundamental na garantia da qualidade do jogo, ajudando a identificar e corrigir problemas antes do lançamento. Com uma abordagem iterativa e focada em melhorias contínuas, esperamos oferecer uma experiência de jogo cada vez mais fluida e envolvente para os jogadores.
