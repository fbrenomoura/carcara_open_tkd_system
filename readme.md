# Carcará Open TKD System

![Logo do Carcará Open TKD System](https://raw.githubusercontent.com/fbrenomoura/cots/main/resources/logo.png)

Um sistema de placar eletrónico completo para competições de Taekwondo (Kyorugi), desenvolvido para ser executado diretamente no navegador, com suporte total a dispositivos móveis e otimizado para uso na horizontal.

## 📜 Descrição

Este projeto é uma aplicação web de página única (SPA) que simula um sistema de pontuação oficial de Taekwondo, incorporando as principais regras e funcionalidades necessárias para gerir uma luta. Foi desenvolvido com foco na usabilidade, na fidelidade às regras da modalidade e na possibilidade de sincronização entre dispositivos.

O sistema foi idealizado por **Francisco Breno Moura Alves**, atleta e professor de Taekwondo (1º DAN) da Associação Parahyba Fighters.

## ✨ Funcionalidades

* **Pontuação em Tempo Real:** Interface para dois competidores (Azul e Vermelho) com placares independentes.
* **Controles Completos de Pontuação:**
    * **Tórax:** +2 pontos por chute.
    * **Cabeça:** +3 pontos por chute.
    * **Soco:** +1 ponto por soco válido.
    * **Bónus de Giro (B):** Adiciona +2 pontos ao próximo chute válido (Tórax ou Cabeça).
    * **Falta (G - Gam-jeom):** Adiciona +1 ponto ao oponente e regista uma falta.
* **Correção de Ações:** Pressionar longamente um botão de pontuação ou falta remove a última ação correspondente.
* **Gestão de Rounds:**
    * Sistema de melhor de 3 rounds.
    * Transição automática para um terceiro round em caso de empate de vitórias.
    * Intervalo de descanso automático de 30 segundos entre os rounds.
* **Regras Oficiais Implementadas:**
    * **Vitória por Faltas:** O oponente vence o round se um atleta cometer 5 faltas (Gam-jeons).
    * **Vitória por Point Gap:** O round termina se houver uma diferença de 12 pontos entre os atletas.
* **Critérios de Desempate (Superioridade):** Em caso de empate no número de rounds vencidos ao final da partida, o sistema aplica automaticamente os seguintes critérios para determinar o vencedor:
    1.  Maior número de pontos marcados com a técnica de giro.
    2.  Maior número de chutes na cabeça.
    3.  Maior número de chutes no tronco.
    4.  Maior número de socos.
    5.  Maior número total de golpes registados.
* **Modo Online (Sincronização via Firebase):**
    * **Conexão por Código:** Permite que múltiplos dispositivos se conectem através de um código de sessão único, sem necessidade de estarem na mesma rede.
    * **Modo Juiz vs. Juiz:** Dois dispositivos atuam como juízes. Um ponto só é computado quando a mesma técnica é registada em ambos os dispositivos num curto intervalo de tempo. O Juiz "A" (master) controla o tempo e as faltas.
    * **Modo Tela (Espelhamento):** Permite que um dispositivo atue como uma tela de visualização, espelhando o placar em tempo real sem botões de controle. Ideal para ser usado como o placar principal visível para o público.
* **Controles da Partida:**
    * **Cronómetro Ajustável:** O tempo de cada round pode ser configurado antes do início da partida.
    * **Pausa e Reinício:** O cronómetro pode ser pausado e retomado a qualquer momento.
    * **Ajuste Manual:** Um modo especial, acessível com o tempo pausado, que permite adicionar ou subtrair pontos individualmente.
    * **Recomeçar Partida:** Opção para reiniciar completamente a luta, zerando todos os placares e rounds.
* **Interface e Experiência de Uso:**
    * **Resumo Final Detalhado:** Ao final da partida, um popup exibe um relatório completo com estatísticas de cada round, totais da partida e uma súmula de todos os eventos.
    * **Feedback Visual e Tátil:** Animações e vibrações confirmam o registo de pontos, melhorando a experiência do utilizador.
    * **Modo Tela Cheia:** Botão para expandir a aplicação, ideal para exibição em monitores maiores.
    * **Instruções para iOS:** Popup com instruções para adicionar o app à tela de início e obter uma experiência de tela cheia real.
    * **Manual de Ajuda:** Um guia completo acessível a qualquer momento através do botão de ajuda (?).

## 🚀 Como Usar

A aplicação está disponível online e pode ser acedida de qualquer dispositivo com um navegador web.

### Acesso Online (Recomendado)

A maneira mais fácil de usar o sistema é através do link do GitHub Pages. Não é preciso instalar nada.

**➡️ [Aceder ao Carcará Open TKD System](https://fbrenomoura.github.io/carcara_open_tkd_system/)**

### Execução Local (Alternativa)

Se você deseja executar o projeto localmente:

1.  **Clone o Repositório:**
    ```bash
    git clone [https://github.com/fbrenomoura/cots.git](https://github.com/fbrenomoura/cots.git)
    cd cots
    ```

2.  **Execução:**
    Abra o ficheiro `index.html` em qualquer navegador web moderno (Google Chrome, Firefox, Safari, Edge).

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Para a estrutura semântica da página.
* **CSS3:** Para estilos básicos e animações.
* **Tailwind CSS:** Um framework CSS "utility-first" para a rápida construção de interfaces customizadas.
* **JavaScript (ES6+):** Para toda a lógica do jogo, interatividade, manipulação de estado e regras da competição.
* **Firebase (Firestore):** Utilizado como o backend em tempo real para possibilitar a funcionalidade de "Modo Online", sincronizando os dados entre os dispositivos.

## 📝 Licença e Uso

Este projeto é totalmente de código aberto e está licenciado sob a **Licença MIT**.

Isso significa que você tem total liberdade para:
* **Usar** a aplicação para fins pessoais, comerciais ou educacionais.
* **Modificar** o código-fonte para adaptá-lo às suas necessidades.
* **Distribuir** cópias originais ou modificadas da aplicação.

Esta é uma aplicação desenvolvida sem fins lucrativos, com o objetivo de apoiar a comunidade do Taekwondo.

### Uso Académico

Se você utilizar este sistema ou parte do seu código em algum estudo académico, tese ou artigo, por favor, **cite Francisco Breno Moura Alves como parte da autoria** do software utilizado na pesquisa.

## 👨‍💻 Autor

Este projeto foi idealizado e desenvolvido por **Francisco Breno Moura Alves**.

* **Instagram:** [@fbrenomoura](https://www.instagram.com/fbrenomoura/)
* **LinkedIn:** [Francisco Breno Moura Alves](https://www.linkedin.com/in/fbrenomoura/)

## 🙏 Agradecimentos

* **Samuel Yure (Sayu):** Pelo design dos ícones e revisões de UI/UX.
* **Laídia Evangelista:** Pelos testes multi-plataforma.
* **Adriane Brandão:** Pela revisão de regras oficiais do Taekwondo.

---
*Este README foi atualizado em 09 de julho de 2025.*

