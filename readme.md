# Carcará Open TKD System

![Logo](resources/logo.png)

Um sistema de placar eletrônico completo para competições de Taekwondo (Kyorugi), desenvolvido para ser executado diretamente no navegador, com suporte total a dispositivos móveis e otimizado para uso na horizontal.

## 📜 Descrição

Este projeto é uma aplicação web de página única (SPA) que simula um sistema de pontuação oficial de Taekwondo, incorporando as principais regras e funcionalidades necessárias para gerir uma luta. Foi desenvolvido com foco na usabilidade, na fidelidade às regras da modalidade e na possibilidade de sincronização entre dispositivos.

O sistema foi idealizado por **Francisco Breno Moura Alves**, atleta e professor de Taekwondo (1º DAN) da Associação Parahyba Fighters.

## ✨ Funcionalidades

- **Pontuação em Tempo Real:** Interface para dois competidores (Azul e Vermelho) com placares independentes.
- **Controles Completos:**
    - **T (Tórax):** +2 pontos por chute.
    - **C (Cabeça):** +3 pontos por chute.
    - **S (Soco):** +1 ponto por soco válido.
    - **B (Bônus de Giro):** Adiciona +2 pontos ao próximo chute válido (Tórax ou Cabeça).
    - **G (Gam-geon):** Adiciona +1 ponto ao oponente e registra uma falta.
- **Correção de Pontos:** Pressionar longamente um botão de pontuação ou falta remove a última ação correspondente.
- **Modo de Pares (Online):**
    - **Conexão por Código:** Permite que dois dispositivos se conectem através de um código de sessão único, sem necessidade de estarem na mesma rede.
    - **Pontuação Sincronizada:** No modo de pares, um ponto só é computado quando a mesma técnica é registrada em ambos os dispositivos em um curto intervalo de tempo.
    - **Ajuste Manual Sincronizado:** Qualquer ajuste manual feito no placar é refletido instantaneamente no dispositivo do par.
- **Gestão de Rounds:**
    - Sistema de melhor de 3 rounds.
    - Transição automática para um terceiro round em caso de empate de vitórias (1x1 ou 0x0).
    - Intervalo de descanso automático de 30 segundos entre os rounds.
- **Regras Oficiais:**
    - **Vitória por Faltas:** O oponente vence o round se um atleta cometer 5 faltas (Gam-geons).
- **Controles da Partida:**
    - **Cronômetro Ajustável:** O tempo de cada round pode ser configurado antes do início da partida.
    - **Controle de Pausa:** O cronômetro pode ser pausado e retomado a qualquer momento.
    - **Ajuste Manual:** Um modo especial, acessível com o tempo pausado, que permite adicionar ou subtrair pontos individualmente.
    - **Recomeçar Partida:** Opção para reiniciar completamente a luta, zerando todos os placares e rounds.
- **Relatórios e Interface:**
    - **Resumo Final:** Ao final da partida, um popup exibe um relatório detalhado com as estatísticas de cada round, totais da partida e uma súmula completa de todas as ações.
    - **Modo Tela Cheia:** Botão para expandir a aplicação para a tela inteira, ideal para exibição em monitores maiores.
    - **Popup de Ajuda:** Um manual completo acessível através do botão de ajuda (?).

## 🚀 Como Usar

A aplicação está disponível online e pode ser acessada de qualquer dispositivo com um navegador web.

### Acesso Online (Recomendado)
A maneira mais fácil de usar o sistema é através do link do GitHub Pages. Não é preciso instalar nada.

**➡️ [Acessar o Carcará Open TKD System](https://fbrenomoura.github.io/carcara_open_tkd_system/)**

### Execução Local (Alternativa)
Se você deseja executar o projeto localmente:

1.  **Clone o Repositório:**
    ```bash
    git clone [https://github.com/fbrenomoura/carcara_open_tkd_system.git](https://github.com/fbrenomoura/carcara_open_tkd_system.git)
    cd carcara_open_tkd_system
    ```

2.  **Estrutura de Ficheiros:**
    Certifique-se de que a estrutura dos ficheiros está correta. O ficheiro de imagem do logo deve estar dentro de uma pasta `resources`:

    ```
    .
    ├── index.html      (Este é o ficheiro principal da aplicação)
    └── resources/
        └── logo.png    (A imagem do logo)
    ```

3.  **Configuração do Firebase (Obrigatório para o Modo de Pares):**
    A funcionalidade "Conectar Pares" depende do Firebase. Para que funcione localmente, você precisa criar um projeto gratuito no Firebase e adicionar suas chaves de configuração ao `index.html`.
    - Crie um projeto no [Firebase](https://firebase.google.com/).
    - Adicione um aplicativo da Web ao seu projeto.
    - O Firebase fornecerá um objeto `firebaseConfig`. Copie-o.
    - Abra o `index.html` e cole o objeto `firebaseConfig` dentro da função `initFirebase()`, substituindo o conteúdo de exemplo.

4.  **Execução:**
    Abra o ficheiro `index.html` em qualquer navegador web moderno (Google Chrome, Firefox, Safari, Edge).

## 🛠️ Tecnologias Utilizadas

-   **HTML5:** Para a estrutura semântica da página.
-   **CSS3:** Para estilos básicos e animações.
-   **Tailwind CSS:** Um framework CSS "utility-first" para a rápida construção de interfaces customizadas.
-   **JavaScript (ES6+):** Para toda a lógica do jogo, interatividade, manipulação de estado e regras da competição.
-   **Firebase (Firestore):** Utilizado como o backend em tempo real para possibilitar a funcionalidade de "Modo de Pares", sincronizando os dados entre os dois dispositivos.

## 📝 Licença e Uso

Este projeto é totalmente de código aberto e está licenciado sob a **Licença MIT**.

Isso significa que você tem total liberdade para:
-   **Usar** a aplicação para fins pessoais, comerciais ou educacionais.
-   **Modificar** o código-fonte para adaptá-lo às suas necessidades.
-   **Distribuir** cópias originais ou modificadas da aplicação.

Esta é uma aplicação desenvolvida sem fins lucrativos, com o objetivo de apoiar a comunidade do Taekwondo.

### Uso Acadêmico
Se você utilizar este sistema ou parte do seu código em algum estudo acadêmico, tese ou artigo, por favor, **cite Francisco Breno Moura Alves como parte da autoria** do software utilizado na pesquisa.

## 👨‍💻 Autor

Este projeto foi idealizado e desenvolvido por **Francisco Breno Moura Alves**.

-   **Instagram:** [@fbrenomoura](https://www.instagram.com/fbrenomoura/)
-   **LinkedIn:** [Francisco Breno Moura Alves](https://www.linkedin.com/in/fbrenomoura/)

---
*Este README foi atualizado em 27 de junho de 2025.*
