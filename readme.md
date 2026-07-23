# Carcará Open TKD System

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
* **Interface Imersiva e Dinâmica:**
    * Durante a luta (cronômetro rodando), a barra superior é automaticamente ocultada para garantir 100% de foco no combate. Ao pausar, a interface e os troféus se reajustam suavemente.
    * **Modo Tela Aprimorado:** Layout flexível com redimensionamento inteligente da tipografia para suportar dezenas nos placares sem estourar a tela. Indicador de hits aguardando confirmação (borda branca) e confirmados (borda e ícone verde).
    * Modais e popups responsivos, garantindo barras de rolagem e limitação de altura para o uso em qualquer tamanho de tela (mobile e tablets).
* **Gestão de Rounds:**
    * Sistema de melhor de 3 rounds (Best-of-Three).
    * Transição automática para um terceiro round em caso de empate de vitórias.
    * Intervalo de descanso automático de 30 segundos entre os rounds.
* **Regras Oficiais Implementadas:**
    * **Vitória por Faltas:** O oponente vence o round se um atleta cometer 5 faltas (Gam-jeons).
    * **Vitória por Point Gap:** O round termina se houver uma diferença de 15 pontos (e não 12) entre os atletas.
* **Critérios de Desempate (Art. 15.5):** Em caso de empate no número de pontos no final de um round, o sistema aplica automaticamente a seguinte ordem de prioridade para determinar o vencedor:
    1.  Maior número de pontos marcados com a técnica de giro (Bônus).
    2.  Técnicas de maior valor registradas: Chutes na cabeça > Chutes no tronco > Socos > Faltas cometidas pelo oponente (Gam-jeom).
    3.  Maior número total de tentativas/golpes registrados na súmula.
    4.  Decisão por Superioridade manual definida pelos árbitros na interface.
* **Modo Online (Sincronização via Firebase):**
    * **Conexão por Código:** Permite que múltiplos dispositivos se conectem através de um código de sessão único.
    * **Modo Juiz vs. Juiz:** Dois dispositivos atuam como pares. Um ponto só é computado quando a mesma técnica é registada em ambos em um intervalo de 3 segundos (Evitando envios duplicados com IDs únicos). O Juiz "Master" controla tempo e faltas.
    * **Resiliência e Reconexão:** Em caso de queda de rede, o Master ou o Par podem reconectar utilizando o código de sessão, e o sistema recupera e preserva o estado automaticamente, retomando a partida de onde parou com o cronômetro devidamente pausado.
    * **Modo Tela (Espelhamento):** Permite que um dispositivo atue como uma tela de visualização principal (TV, Telão) em tempo real sem controles.

## 🚀 Como Usar

A aplicação está disponível online e pode ser acedida de qualquer dispositivo com um navegador web.

### Acesso Online (Recomendado)

A maneira mais fácil de usar o sistema é através do link do GitHub Pages. Não é preciso instalar nada.

**➡️ [Aceder ao Carcará Open TKD System](https://fbrenomoura.github.io/carcara_open_tkd_system/)**

### Execução Local (Alternativa)

Se você deseja executar o projeto localmente:

1.  **Clone o Repositório:**
    ```bash
    git clone https://github.com/fbrenomoura/carcara_open_tkd_system.git
    cd carcara_open_tkd_system
    ```

2.  **Execução:**
    Abra o ficheiro `index.html` em qualquer navegador web moderno (Google Chrome, Firefox, Safari, Edge).

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Para a estrutura semântica da página.
* **CSS3:** Para estilos básicos e animações.
* **Tailwind CSS:** Um framework CSS "utility-first" para a rápida construção de interfaces customizadas.
* **JavaScript (ES6+):** Para toda a lógica do jogo, interatividade, manipulação de estado e regras da competição.
* **Firebase (Firestore):** Utilizado como o backend em tempo real para possibilitar a funcionalidade de "Modo Online", sincronizando os dados e batimentos cardíacos entre os dispositivos.

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
*Este README foi atualizado em Julho de 2026.*


