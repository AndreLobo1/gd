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
<div align="center">

<sub>Tabela 7 - Casos de Teste </sub>

| #   | Título do Caso de Teste                             | Pré-condição                                           | Descrição do Teste                                                                                                             | Pós-condição                                                                                          |
| --- | ---------------------------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
| 1   | Teste de Início do Jogo                              | O jogo foi iniciado                                    | Mover o cursor até o botão "play" e clicar uma vez sobre ele                                                                  | O botão "play" deve ser afetado por um efeito visual indicando que o jogador passou o cursor por cima dele e o jogador deve ser enviado para a tela de controles do jogo. |
| 2   | Teste de Transição para Tela de Escolha de Personagem | O jogo está na tela de controles                      | Mover o cursor até o botão "play" e clicar uma vez sobre ele                                                                  | O botão "play" deve ser afetado por um efeito visual indicando que o jogador passou o cursor por cima dele e o jogador deve ser enviado para a tela de escolha de personagens. |
| 3   | Teste de Escolha de Personagem e adição do nome do jogador | O jogo está na tela de escolha de personagem        | Escolher qualquer um dos quatro personagens, clicar uma vez sobre o escolhido, escrever seu nome no campo indicado e clicar uma vez sobre o botão "iniciar"                                     | Os personagens devem ser afetados por um efeito indicando que o jogador passou o cursor por cima dele, após escolher, o jogador deve ser enviado para a tela do jogo com o personagem escolhido e o nome do jogador deve aparecer nos diálogos com os NPCs |
| 4   | Teste de Efeito do personagem quando parado          | O jogo está em andamento e o jogador está parado      | Não é necessária nenhuma ação do jogador                                                                                      | A trilha sonora do jogo deve tocar constantemente enquanto o jogador estiver na aba do jogo e, quando totalmente parado, o personagem do jogador deve iniciar uma animação |
| 5   | Teste de Trilha Sonora                                | O jogo está em andamento                               | Não é necessária nenhuma ação do jogador                                                                                      | A trilha sonora do jogo deve tocar constantemente enquanto o jogador estiver na aba do jogo |
| 6   | Teste de Movimentação do Personagem, dos sons de passos e da animação de andar | O jogo está em andamento e o jogador está em um ambiente aberto | Acionar todas as 4 setas direcionais do teclado                                                                       | O personagem deve se mover em velocidade constante através das teclas direcionais do teclado conforme as direções das mesmas, o som de passos deve ser ativado durante a movimentação e o personagem deve exibir uma animação indicando movimento. |
| 7   | Teste de Interação com NPCs                          | O jogo está em andamento e o personagem está próximo ao NPC | Se aproximar do NPC do jogo e acionar a tecla de interação "E"                                                             | O NPC deve mostrar um balão de fala indicando a tecla "E" e, ao interagir, o NPC deve falar com o jogador através de outro balão de fala. Além disso, o balão de fala deve mostrar uma foto do NPC ao lado dele. Sempre que o jogador acionar a tecla de interação "E" dentro de um diálogo, o som de interação deve ser ativado. O texto da fala sempre deve ficar dentro dele. O NPC sempre deve chamar o jogador pelo nome que ele inseriu no início do jogo. NPCs não humanos como o computador devem direcionar o jogador para um minigame. |
| 8   | Teste de Transição para o Minigame de hack           | O jogador está dentro do escritório e está próximo ao computador | O jogador interage com o computador dentro do escritório                                                                | A tela do minigame deve abrir normalmente e a sua trilha sonora deve começar a tocar. |
| 9   | Teste de acerto no Minigame de hack            | O jogo está na tela do minigame de hack                | Mover uma sigla para o significado correto.                                                                                                    | A sigla deve seguir o ponteiro do cursor enquanto o jogador estiver pressionando. A "luz" vermelha deve se tornar uma luz verde, indicando que a resposta está correta.              |
| 10   | Teste de erro no Minigame de hack            | O jogo está na tela do minigame de hack                | Mover uma sigla para o significado errado.                                                                                                    | A sigla deve seguir o ponteiro do cursor enquanto o jogador estiver pressionando. A "luz" vermelha deve continuar vermelha indicando que a resposta está errada.              |
| 11   | Teste de Transição de fase no Minigame de hack            | O jogo está na tela do minigame de hack                | Vencer a primeira fase do minigame.                                                                                                    | O jogador deve ser enviado para a proxima fase do minigame.              |
| 12   | Teste de Transição ao Vencer o Minigame de hack            | O jogo está na tela do minigame de hack, em sua segunda e ultima fase.               | Jogar a fase e vencer                                                                                                    | Deve ser exibida uma tela mostrando o mapa do jogo com indicacoes de onde estao os simbolos do u. O jogador deve ser redirecionado para a cena dentro do escritório Unilever.              |
| 13   | Teste de Transição ao Perder o Minigame de hack             | O jogo está na tela do primeiro minigame                | Jogar o minigame e perder                                                                                                    | O jogo deve exibir uma tela de gameover com um botão de "Recomeçar". Após clicar no botão, o jogador deve recomeçar o jogo do início. |
| 14   | Teste de Recomeçar o Jogo Após Gameover            | O jogo está na tela de gameover do primeiro minigame   | Mover o cursor até o botão de "recomeçar" e clicar uma vez sobre ele                                                          | O botão "recomeçar" deve ser afetado por um efeito indicando que o jogador passou o cursor por cima dele e ao clicar uma vez, o minigame deve recomeçar. |
| 15  | Teste de Colisões no Jogo                           | O jogo está em andamento e o jogador está se movendo   | Tentar atravessar as estruturas do mapa como prédios, árvores, arbustos e NPCs                                                 | O personagem não deve ser capaz de atravessar as estruturas do mapa, e deve interagir com elas de acordo com a lógica do jogo.                                   |
| 16   | Teste de Entrada em Diferentes Ambientes            | O jogo está em andamento                               | Movimentar-se para diferentes áreas ou ambientes do jogo                                                                        | O personagem deve conseguir entrar em diferentes áreas ou ambientes do jogo sem problemas, sem travamentos ou interrupções inesperadas. |
| 17  | Teste de Transição ao Vencer o Minigame da memória               | O jogo está na tela do Minigame de memória             | Completar com sucesso o minigame de memória                                                                                  | O jogador deve ser redirecionado para a cena da cidade com sucesso, avançando na progressão do jogo. |
| 18  | Teste de Transição ao Perder o Minigame da memória               | O jogo está na tela do Minigame de memória             | Perder o minigame de memória                                                                                                 | O jogador deve ser redirecionado para a tela de game over, onde poderá recomeçar o jogo.            |
| 19  | Teste de Recomeçar o Jogo Após Game over                        | O jogo está na tela de game over                        | Mover o cursor até o botão "recomeçar" e clicar uma vez sobre ele                                                              | O jogo deve recomeçar do começo.                                                                   |
| 20  | Teste de Transição ao recomeçar o Minigame de memória           | O minigame está na tela de game over                    | Mover o cursor até o botão "recomeçar" e clicar uma vez sobre ele                                                              | O minigame deve recomeçar do começo.                                                               |
| 21  | Teste de Transição ao Perder o Minigame da memória              | O jogo está na tela do minigame e o jogador perdeu o jogo | Perder o jogo virando cartas que não formam pares até perder todas as vidas.                                                    | O jogo deve exibir uma tela de game over com um botão de "Recomeçar".                              |
| 22  | Teste de Transição ao recomeçar o Minigame de memória           | O minigame está na tela de game over                    | Mover o cursor até o botão "recomeçar" e clicar uma vez sobre ele                                                              | O jogo deve recomeçar do começo.                                                                   |
| 23  | Teste de Abrir e Fechar o Celular                   | O jogo está em andamento e o jogador já interagiu com o primeiro NPC | Pressionar a tecla de interação "C" uma vez para abrir o celular e outra vez para fechar | O celular deve abrir e fechar normalmente                                                   |
| 24  | Teste de Abrir, Fechar e Navegar pelo Minimapa dentro do Celular | O jogador está com o celular aberto                    | Clicar no botão "GPS" uma vez para abrir o minimapa, clicar na seta indicando a próxima parte do minimapa e, em seguida, clicar no ícone da casa para retornar à tela inicial do celular | O jogo deve mostrar o minimapa corretamente                                                    |
| 25  | Teste de Abrir, Navegar e Fechar o Hub de Links     | O jogador está com o celular aberto                    | Clicar no botão "URL" para abrir o hub de links, clicar nos três links disponíveis e, em seguida, clicar no ícone da casa para retornar à tela inicial do celular | O hub de links deve exibir os links clicáveis e redirecionar corretamente o jogador após clicar neles |
| 26  | Teste do Quiz                                        | O jogador está com o celular aberto e coletou todos os pedaços do "U" | Clicar no botão "Quiz" para iniciar o quiz e, em seguida, clicar no botão "Play" para começar o jogo | O quiz deve iniciar corretamente e avançar para as perguntas após clicar em "Play"               |
| 27  | Teste de Responder Errado no Quiz                    | O jogador está jogando o quiz                         | Clicar em uma alternativa incorreta durante o quiz                                                                       | A alternativa selecionada deve ficar vermelha e o jogador deve avançar para a próxima pergunta sem contabilizar a resposta incorreta                       |
| 28  | Teste de Responder Corretamente no Quiz             | O jogador está jogando o quiz                          | Clicar em uma alternativa correta durante o quiz                                                                       | A alternativa selecionada deve ficar verde e o jogador deve avançar para a próxima pergunta, contabilizando a resposta correta                      |
| 29  | Teste de Finalizar o Quiz                           | O jogador está jogando o quiz                         | Responder todas as perguntas do quiz, independentemente das respostas                                                        | O quiz deve exibir uma tela informando quantas perguntas o jogador respondeu corretamente     |
| 30  | Teste da Barra de Tarefas                           | O jogo está em andamento                              | Completar todas as tarefas do jogo                                                                                       | A barra de tarefas deve ser atualizada para refletir o progresso do jogador                                                                               |

<sub>Fonte: Autoria Própria (2024) </sub>

</div>

1. Teste de Início do Jogo
   - **Resultado:** O botão "play" respondeu corretamente ao ser clicado, e o jogador foi redirecionado para a tela de controles do jogo conforme esperado.
   - **Veredito:** Sucesso.

2. Teste de Transição para Tela de Escolha de Personagem
   - **Resultado:** O botão "play" funcionou corretamente, enviando o jogador para a tela de escolha de personagem após ser clicado, porém ele demorou um pouco para responder, sendo necessário vários cliques para que o jogador fosse enviado para a próxima tela.
   - **Veredito:** Sucesso, com ressalva quanto à velocidade de resposta.

3. Teste de Escolha de Personagem
   - **Resultado:** A escolha de personagem funcionou como esperado, com os personagens sendo destacados e o jogador sendo enviado para a tela do jogo com o personagem escolhido. No entanto, foi observada a possibilidade de dois personagens ficarem sob o efeito do cursor.
   - **Veredito:** Sucesso, com ressalva quanto ao efeito do cursor.

4. Teste de Trilha Sonora
   - **Resultado:** A trilha sonora do jogo tocou continuamente enquanto o jogador estava na tela do jogo.
   - **Veredito:** Sucesso.

5. Teste de Movimentação do Personagem
   - **Resultado:** A movimentação do personagem funcionou conforme esperado, com o personagem respondendo às teclas direcionais do teclado e o som de passos sendo ativado durante o movimento. No entanto, o personagem pode atravessar alguns objetos e ficar invisível em uma determinada parte do mapa.
   - **Veredito:** Sucesso, com ressalva quanto aos problemas de colisão e visibilidade.

6. Teste de Interação com NPCs
   - **Resultado:** As interações com os NPCs foram parcialmente bem-sucedidas. Alguns textos ultrapassam o espaço do balão de fala, e os NPCs podem ser atravessados pelo jogador.
   - **Veredito:** Sucesso, com ressalva quanto ao layout dos balões de fala e à colisão com os NPCs.

7. Teste de Transição ao Vencer o Minigame
   - **Resultado:** Após vencer o minigame, o jogador foi redirecionado para a porta de entrada dentro do escritório Unilever conforme o esperado.
   - **Veredito:** Sucesso.

8. Teste de Transição ao Perder o Minigame
   - **Resultado:** Ao perder o minigame, o jogo exibiu corretamente a tela de game over, permitindo que o jogador recomeçasse o jogo.
   - **Veredito:** Sucesso.

9. Teste de Recomeçar o Jogo Após Game over
   - **Resultado:** O botão "recomeçar" na tela de game over funcionou corretamente, permitindo que o jogador recomeçasse o minigame.
   - **Veredito:** Sucesso.

10. Teste de Colisões no Jogo
    - **Resultado:** Durante o teste, foram encontrados alguns problemas com colisões inadequadas do personagem com certas estruturas do mapa, que precisam ser corrigidos.
    - **Veredito:** Sucesso, com ressalva quanto aos problemas de colisão.

11. Teste de Entrada em Diferentes Ambientes
    - **Resultado:** A entrada nos diferentes ambientes do jogo foi bem-sucedida, com o personagem entrando nos ambientes sem dificuldades.
    - **Veredito:** Sucesso.

12. Teste de Transição para o Minigame de Jogo da Memória
    - **Resultado:** O jogador foi capaz de acessar o minigame da memória após completar a primeira fase do jogo.
    - **Veredito:** Sucesso.

13. Teste de Erro no Minigame de Jogo da Memória
    - **Resultado:** O jogo respondeu corretamente ao virar duas cartas que não formavam um par, indicando a perda de uma vida e escondendo as cartas novamente.
    - **Veredito:** Sucesso.

14. Teste de Acerto no Minigame de Jogo da Memória
    - **Resultado:** O jogo respondeu corretamente ao virar duas cartas que formavam um par, mantendo as cartas viradas para cima.
    - **Veredito:**

14. Teste de Acerto no Minigame de Jogo da Memória
   - **Resultado:** O jogo respondeu corretamente ao virar duas cartas que formavam um par, mantendo as cartas viradas para cima.
   - **Veredito:** Sucesso.

15. Teste de Transição ao Vencer o Minigame da Memória
   - **Resultado:** Após vencer o minigame, o jogador retornou à cena da cidade com sucesso, avançando na progressão do jogo.
   - **Veredito:** Sucesso.

16. Teste de Transição ao Perder o Minigame da Memória
   - **Resultado:** Ao perder o minigame, o jogador foi redirecionado para a tela de game over, onde pôde recomeçar o jogo.
   - **Veredito:** Sucesso.

17. Teste de Recomeçar o Jogo Após Game Over
   - **Resultado:** O botão "recomeçar" na tela de game over funcionou corretamente, permitindo que o jogador recomeçasse o minigame.
   - **Veredito:** Sucesso.

18. Teste de Transição ao Recomeçar o Minigame de Memória
   - **Resultado:** Após selecionar a opção "recomeçar", o minigame reiniciou corretamente, permitindo ao jogador tentar novamente.
   - **Veredito:** Sucesso.

19. Teste de Colisões no Jogo
   - **Resultado:** Alguns objetos podem ser atravessados pelo jogador.
   - **Veredito:** Sucesso, com ressalva quanto aos problemas de colisão.

20. Teste de Entrada em Diferentes Ambientes
   - **Resultado:** O jogador ainda pode entrar em diferentes ambientes do jogo sem problemas, garantindo uma transição suave entre as áreas.
   - **Veredito:** Sucesso.

21. Teste de Transição ao Perder o Minigame da Memória
   - **Resultado:** Durante o teste, o jogador perdeu o jogo ao virar cartas que não formavam pares até perder todas as vidas.
   - **Veredito:** Sucesso. O jogo exibiu corretamente uma tela de game over com um botão "Recomeçar".

22. Teste de Transição ao Recomeçar o Minigame de Memória
   - **Resultado:** Durante o teste, o jogador moveu o cursor até o botão "recomeçar" na tela de game over e clicou uma vez sobre ele.
   - **Veredito:** Sucesso. O jogo recomeçou do começo após o jogador selecionar a opção "recomeçar".

23. Teste de Abrir e Fechar o Celular
- **Resultado:** O celular abriu e fechou normalmente em resposta às interações do jogador.
- **Veredito:** Sucesso.

24. Teste de Abrir, Fechar e Navegar pelo Minimapa dentro do Celular
- **Resultado:** O minimapa abriu corretamente quando solicitado, permitindo a navegação entre as diferentes partes. Ao clicar no ícone da casa, o jogador foi redirecionado para a tela inicial do celular conforme esperado.
- **Veredito:** Sucesso.

25. Teste de Abrir, Navegar e Fechar o Hub de Links
- **Resultado:** O hub de links foi aberto com sucesso, permitindo que o jogador interagisse com os links disponíveis. Ao clicar no ícone da casa, o jogador retornou à tela inicial do celular conforme esperado.
- **Veredito:** Sucesso.

26. Teste do Quiz
- **Resultado:** O quiz iniciou corretamente após o jogador coletar todos os pedaços do "U" e clicar nos botões correspondentes. Após clicar em "Play", o quiz avançou para as perguntas.
- **Veredito:** Sucesso.

27. Teste de Responder Errado no Quiz
- **Resultado:** Durante o quiz, ao responder incorretamente a uma pergunta, a alternativa selecionada ficou vermelha e o jogador avançou para a próxima pergunta sem que a resposta incorreta fosse contabilizada.
- **Veredito:** Sucesso.

28. Teste de Responder Corretamente no Quiz
- **Resultado:** Ao responder corretamente a uma pergunta no quiz, a alternativa selecionada ficou verde e o jogador avançou para a próxima pergunta, com a resposta correta sendo contabilizada.
- **Veredito:** Sucesso.

29. Teste de Finalizar o Quiz
- **Resultado:** Após responder todas as perguntas do quiz, independentemente das respostas, o jogo exibiu uma tela informando quantas perguntas o jogador respondeu corretamente.
- **Veredito:** Sucesso.

30. Teste da Barra de Tarefas
- **Resultado:** A barra de tarefas foi atualizada corretamente para refletir o progresso do jogador, mostrando todas as tarefas completadas durante o jogo.
- **Veredito:** Sucesso.

###  Problemas Encontrados e melhorias futuras.

### 1. Problema de Resposta do Botão "Play" na Tela de Escolha de Personagem
- **Descrição:** Durante o teste de transição para a tela de escolha de personagem, foi observado um atraso na resposta do botão "play" ao ser clicado, exigindo vários cliques para que o jogador fosse enviado para a próxima tela.
- **Gravidade:** Baixa
- **Status:** Pendente de correção.
- **Observações:** O atraso na resposta do botão pode impactar negativamente a experiência do jogador, causando frustração e prejudicando a usabilidade do jogo.

### Melhorias Futuras Relacionadas ao Problema de Resposta do Botão "Play"

1. **Otimização do Código:** Revisar e otimizar o código responsável pela transição entre telas para reduzir o tempo de resposta do botão "play" e garantir uma experiência mais fluida para o jogador.

2. **Testes de Usabilidade:** Realizar testes de usabilidade específicos para identificar problemas de resposta do botão "play" em diferentes dispositivos e condições de uso, garantindo que a transição entre telas seja rápida e intuitiva.

3. **Feedback Visual:** Implementar feedback visual imediato ao clicar no botão "play", como uma animação de clique ou alteração visual, para informar ao jogador que sua ação foi reconhecida e que a transição para a próxima tela está em andamento.

### 2. Problema de Colisão do Personagem com Objetos do Mapa
- **Descrição:** Durante o teste de movimentação do personagem, foi observado que o personagem pode atravessar alguns objetos no mapa, como árvores, arbustos e NPCs.
- **Gravidade:** Média
- **Status:** Pendente de correção.
- **Observações:** Problemas de colisão podem afetar a imersão do jogador e a consistência do mundo do jogo, levando a uma experiência de jogo menos realista.

### Melhorias Futuras Relacionadas aos Problemas de Colisões

1. **Refinamento das Colisões:** Realizar uma revisão detalhada das áreas problemáticas do mapa e ajustar as colisões dos objetos para garantir que o personagem não possa atravessá-los indevidamente.

2. **Implementação de Colisões Precisas:** Utilizar técnicas de detecção de colisão mais precisas, como colisões baseadas em formas geométricas ou colisões pixel-perfect, para garantir que a interação entre o personagem e os objetos do cenário seja mais realista e consistente.

3. **Testes Extensivos de Colisões:** Realizar testes abrangentes em diferentes partes do mapa e em diversas condições de jogo para identificar e corrigir quaisquer problemas de colisão remanescentes, assegurando uma experiência de jogo mais estável e imersiva.

### 3. Problema de Visibilidade do Personagem em Determinada Parte do Mapa
- **Descrição:** Durante o teste de movimentação do personagem, foi observado que o personagem pode ficar invisível em uma determinada parte do mapa.
- **Gravidade:** Média
- **Status:** Pendente de correção.
- **Observações:** Problemas de visibilidade podem prejudicar a experiência do jogador, tornando difícil a navegação e a interação com o ambiente do jogo.

### Melhorias Futuras Relacionadas ao Problema de Visibilidade do Personagem

1. **Análise do Cenário:** Investigar a área específica do mapa onde o personagem fica invisível para identificar as causas subjacentes do problema, como problemas de renderização ou configurações de câmera inadequadas.

2. **Ajustes de Renderização:** Realizar ajustes nas configurações de renderização do jogo para garantir que o personagem seja sempre visível, independentemente da posição do jogador no mapa.

3. **Testes de Renderização:** Realizar testes extensivos de renderização em diferentes plataformas e condições de hardware para verificar a visibilidade do personagem em todas as áreas do mapa e garantir uma experiência consistente para todos os jogadores.

### 4. Problema de Layout dos Balões de Fala e Colisão com NPCs
- **Descrição:** Durante o teste de interação com NPCs, foi observado que alguns textos ultrapassam o espaço do balão de fala, e os NPCs podem ser atravessados pelo jogador.
- **Gravidade:** Baixa
- **Status:** Pendente de correção.
- **Observações:** Embora não seja um problema crítico, a má formatação dos balões de fala pode prejudicar a legibilidade do texto e a compreensão das interações com os NPCs.

### Melhorias Futuras Relacionadas ao Problema de Layout dos Balões de Fala e Colisão com NPCs

1. **Ajustes de Layout:** Realizar ajustes no layout dos balões de fala para garantir que o texto permaneça dentro dos limites do balão, tornando-o completamente legível para o jogador.

2. **Configuração das Colisões:** Ajustar as áreas de colisão dos NPCs para evitar que o jogador os atravesse, garantindo uma interação mais consistente e imersiva com esses personagens.

3. **Testes de Interatividade:** Realizar testes específicos de interação com NPCs para verificar se os ajustes feitos no layout e nas colisões melhoraram a experiência do jogador em relação a esses elementos.

Essas melhorias futuras visam resolver os problemas identificados com as colisões no jogo, garantindo uma experiência de jogo mais suave, imersiva e livre de falhas para os jogadores.

### Conclusão
Os casos de teste apresentados nesta seção ofereceram uma visão abrangente do funcionamento do jogo, fornecendo feedbacks valiosos para o aprimoramento contínuo do projeto. Embora tenhamos alcançado sucesso em muitos testes, alguns problemas foram identificados durante o processo, destacando áreas que podem exigir ajustes adicionais.

Durante os testes, observamos problemas relacionados à colisão com estruturas do mapa e à exibição inadequada da foto do NPC no escritório Unilever. Esses problemas são considerados de gravidade média e baixa, respectivamente, e estão pendentes de correção em futuras iterações do desenvolvimento.

Além disso, reconhecemos a importância de testes adicionais para validar novas funcionalidades e melhorias implementadas no jogo. Em resumo, os casos de teste desempenham um papel fundamental na garantia da qualidade do jogo, ajudando a identificar e corrigir problemas antes do lançamento. Com uma abordagem iterativa e focada em melhorias contínuas, esperamos oferecer uma experiência de jogo cada vez mais fluida e envolvente para os jogadores.
