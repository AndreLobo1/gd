## 5.1. Casos de Teste

Nesta seção, apresentamos uma série de casos de teste detalhados que foram desenvolvidos para avaliar o funcionamento e a integração das partes do jogo. Cada caso de teste é projetado para testar uma funcionalidade específica do jogo, desde a inicialização até a interação com personagens e transições entre telas.

Além disso, os casos de teste abordam a configuração adequada do ambiente de teste, garantindo resultados precisos e consistentes. Também destacamos possíveis melhorias futuras identificadas durante o processo de teste, visando aprimorar a qualidade e a experiência do jogo para os usuários finais.

Os casos de teste são organizados em uma tabela que contém informações sobre a pré-condição, a descrição do teste e a pós-condição. Cada caso de teste é numerado para facilitar a referência e a rastreabilidade durante o processo de teste.

Esses casos de teste desempenham um papel fundamental na garantia da qualidade do jogo, ajudando a identificar e corrigir problemas antes do lançamento, bem como sugerindo melhorias para futuras iterações do desenvolvimento.

### Configuração de Ambiente de Teste

Antes de iniciar os testes, é crucial configurar adequadamente o ambiente de teste para garantir resultados precisos e consistentes. Abaixo estão os requisitos básicos necessários para configurar o ambiente de teste para o jogo.

#### Requisitos do Ambiente de Teste:

1. **Computador com Navegador Compatível:**
   - Certifique-se de ter acesso a um computador que suporte os navegadores modernos, como Google Chrome, Mozilla Firefox, Safari ou Microsoft Edge.

2. **Tela Colorida:**
   - Utilize um monitor ou tela colorida com boa resolução para visualizar adequadamente o jogo e seus elementos gráficos.

3. **Sistema de Som Funcional:**
   - Verifique se o dispositivo de teste possui um sistema de som funcional para garantir a reprodução adequada de áudio dentro do jogo.

4. **Habilitar JavaScript no Navegador:**
   - Certifique-se de que o JavaScript esteja habilitado no navegador utilizado para garantir que o jogo seja executado corretamente.

5. **Compatibilidade com Phaser Framework:**
   - O ambiente de teste deve suportar o framework Phaser para executar o jogo sem problemas. Certifique-se de que o navegador e o dispositivo atendam aos requisitos mínimos do Phaser.

6. **Espaço em Disco Suficiente:**
   - Certifique-se de ter espaço em disco adequado disponível para armazenar o jogo e outros recursos necessários para os testes.

Ao cumprir esses requisitos, você estará pronto para configurar um ambiente de teste adequado para realizar testes eficazes no jogo.

### Ambiente de Teste Utilizado

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

## Testes

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

### Resultados dos Testes

### 1. Teste de Início do Jogo
- O botão "play" respondeu corretamente ao ser clicado, e o jogador foi redirecionado para a tela de controles do jogo conforme esperado.

### 2. Teste de Transição para Tela de Escolha de Personagem
- O botão "play" funcionou corretamente, enviando o jogador para a tela de escolha de personagem após ser clicado.

### 3. Teste de Escolha de Personagem
- A escolha de personagem funcionou como esperado, com os personagens sendo destacados e o jogador sendo enviado para a tela do jogo com o personagem escolhido.

### 4. Teste de Trilha Sonora
- A trilha sonora do jogo tocou continuamente enquanto o jogador estava na aba do jogo.

### 5. Teste de Movimentação do Personagem
- A movimentação do personagem funcionou conforme esperado, com o personagem respondendo às teclas direcionais do teclado e o som de passos sendo ativado durante o movimento.

### 6. Teste de Interação com NPCs
- As interações com os NPCs foram parcialmente bem-sucedidas. O NPC da entrada do escritório está com a foto ao lado do balão de fala cortada, além disso, o primeiro NPC pode ser atravessado pelo jogador.

### 7. Teste de Transição ao Vencer o Minigame
- Após vencer o minigame, o jogador foi redirecionado para a porta de entrada dentro do escritório Unilever conforme o esperado.

### 8. Teste de Transição ao Perder o Minigame
- Ao perder o minigame, o jogo exibiu corretamente a tela de gameover, permitindo que o jogador recomeçasse o jogo.

### 9. Teste de Recomeçar o Jogo Após Gameover
- O botão "recomeçar" na tela de gameover funcionou corretamente, permitindo que o jogador recomeçasse o minigame.

### 10. Teste de Colisões no Jogo
- Durante o teste, foram encontrados alguns problemas com colisões inadequadas do personagem com certas estruturas do mapa, que precisam ser corrigidos.

### 11. Teste de Entrada em Diferentes Ambientes
- A entrada nos diferentes ambientes do jogo foi bem-sucedida, com o personagem entrando nos ambientes sem dificuldades.

###  Problemas Encontrados

### Problema de Colisão com Estruturas do Mapa
- **Descrição:** Durante o teste de colisões no jogo, o personagem foi capaz de atravessar certas estruturas do mapa, como árvores, arbustos e NPCs.
- **Gravidade:** Média
- **Status:** Pendente de correção.
- **Observações:** Parece haver problemas com as colisões definidas para esses objetos, resultando em comportamento não esperado do personagem.

### Melhorias Futuras Relacionadas aos Problemas de Colisões

1. **Refinamento das Colisões:** Realizar uma análise detalhada das colisões no jogo e fazer ajustes precisos para garantir que os objetos do cenário tenham colisões adequadas, evitando que o jogador possa atravessá-los ou ficar preso em áreas inapropriadas.

2. **Implementação de Colisões Pixel-Perfect:** Considerar a implementação de colisões pixel-perfect para objetos no jogo, garantindo que a detecção de colisões seja feita com base na forma exata dos objetos, proporcionando uma experiência mais precisa e realista.

3. **Testes Abrangentes de Colisões:** Realizar testes extensivos de colisões em diferentes cenários e condições de jogo para identificar e corrigir quaisquer problemas remanescentes, garantindo que todas as áreas do jogo tenham colisões consistentes e confiáveis.

4. **Utilização de Ferramentas de Debugging:** Utilizar ferramentas de debugging e visualização de colisões para facilitar a identificação de problemas e a depuração das colisões no jogo, permitindo uma resolução mais rápida e eficiente dos problemas encontrados.

Essas melhorias futuras visam resolver os problemas identificados com as colisões no jogo, garantindo uma experiência de jogo mais suave, imersiva e livre de falhas para os jogadores.

### Conclusão
Os casos de teste apresentados nesta seção ofereceram uma visão abrangente do funcionamento do jogo, fornecendo feedbacks valiosos para o aprimoramento contínuo do projeto. Embora tenhamos alcançado sucesso em muitos testes, alguns problemas foram identificados durante o processo, destacando áreas que podem exigir ajustes adicionais.

Durante os testes, observamos problemas relacionados à colisão com estruturas do mapa e à exibição inadequada da foto do NPC no escritório Unilever. Esses problemas são considerados de gravidade média e baixa, respectivamente, e estão pendentes de correção em futuras iterações do desenvolvimento.

Além disso, reconhecemos a importância de testes adicionais para validar novas funcionalidades e melhorias implementadas no jogo. Em resumo, os casos de teste desempenham um papel fundamental na garantia da qualidade do jogo, ajudando a identificar e corrigir problemas antes do lançamento. Com uma abordagem iterativa e focada em melhorias contínuas, esperamos oferecer uma experiência de jogo cada vez mais fluida e envolvente para os jogadores.
