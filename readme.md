# Carcará Open TKD System

Um sistema de placar eletrônico completo para competições de Taekwondo (Kyorugi), desenvolvido para ser executado diretamente no navegador, com suporte total a dispositivos móveis e otimizado para uso na horizontal.

## 📜 Descrição

Este projeto é uma aplicação web de página única (SPA) que simula um sistema de pontuação oficial de Taekwondo, incorporando as regras oficiais atualizadas da modalidade, gestão automatizada de desempates e suporte a sincronização em tempo real entre múltiplos dispositivos.

O sistema foi idealizado por **Francisco Breno Moura Alves**, atleta e professor de Taekwondo (1º DAN) da Associação Parahyba Fighters.

## ✨ Funcionalidades

### 🥋 Pontuação e Controles de Combate
* **Pontuação em Tempo Real:** Placares independentes para dois competidores (Azul e Vermelho).
* **Tórax:** +2 pontos por chute válido.
* **Cabeça:** +3 pontos por chute válido.
* **Soco:** +1 ponto por soco no tórax.
* **Bônus de Giro (x2):** Ao registrar um chute no tórax ou cabeça, um botão flutuante **"x2"** é exibido por 2 segundos. Pressioná-lo confirma a técnica de giro e **dobra** o valor da pontuação daquele golpe (Tórax: 2 → 4 pts; Cabeça: 3 → 6 pts).
* **Falta (G - Gam-jeom):** Adiciona +1 ponto ao oponente e registra uma falta para o atleta.
* **Passividade nos 10s Finais (+1 Extra):** Ao aplicar uma falta (G) nos últimos 10 segundos do round, um botão **"+1"** surge por 2 segundos. Pressioná-lo concede +1 ponto adicional ao oponente (totalizando +2 pts pelo Gam-jeom de passividade nos segundos finais).
* **Correção Inteligente de Erros:** Clique longo (pressionar por 1 segundo) em qualquer botão de pontuação ou falta remove o último registro. Ao remover um chute com giro, o bônus associado é removido automaticamente.
* **Ajuste Manual:** Modo especial com o tempo pausado para ajuste livre de pontos (+/-).

### 🏆 Gestão de Rounds e Regras Oficiais
* **Formato Best-of-Three:** Disputa em melhor de 3 rounds. Vence a partida quem conquistar 2 rounds.
* **Point Gap:** O round é encerrado automaticamente se houver uma diferença de **15 pontos** entre os atletas.
* **Vitória por Faltas:** O atleta vence o round se o adversário acumular **5 faltas (Gam-jeoms)**.
* **Desempate Obrigatório de Round (Art. 15.5):** Nenhum round termina empatado. Se os atletas pontuarem igual ao fim do tempo, o vencedor do round é determinado pela seguinte ordem de prioridade:
    1.  **Maior pontuação por giros (Bônus x2)** conquistada no round.
    2.  **Pontos por técnicas de maior valor:** Cabeça > Tronco > Socos > Faltas cometidas pelo oponente (Gam-jeom).
    3.  **Volume de ataques/tentativas:** Maior número total de tentativas isoladas de golpe registradas.
    4.  **Votação de Superioridade:** Decisão manual dos árbitros via interface.

### 🌐 Modo Online e Sincronização (Firebase)
* **Conexão por Código:** Conexão sem fio entre dispositivos via código de sessão único.
* **Modo Juiz vs. Juiz (Par):** Dois dispositivos atuam como árbitros. O ponto só é confirmado quando a mesma técnica é pressionada por ambos dentro de uma janela de 3 segundos (com algoritmo anti-duplicação por ID de ação). O Juiz A (Master) gerencia cronômetro, faltas e ajustes.
* **Resiliência e Reconexão de Master:** Se a conexão cair, o Master pode inserir o código e reconectar. O sistema restabelece a sessão, recupera o estado atualizado e mantém o jogo pausado para segurança. Os *heartbeats* mantêm os pares e telas informados sem derrubar a sala.
* **Modo Tela (Espelhamento para Público/TV):**
    * Exibe o placar em tempo real em tamanho expandido sem controles.
    * **Indicadores Visuais de Hit:** As tentativas de golpe surgem em um círculo transparente com borda cinza. Ao serem confirmadas, a borda e o ícone ficam **verdes**, desaparecendo 1 segundo depois mantendo o fundo transparente.

### 🎨 Interface Imersiva e Responsiva
* **Foco no Combate:** A barra superior de ferramentas se oculta automaticamente quando o cronômetro está rodando.
* **Troféus Dinâmicos:** Os ícones de vitórias de round (troféus) se deslocam suavemente (`top-4` / `top-14`) para aproveitar o topo da tela quando o menu está oculto.
* **Modo Tela Otimizado:** Tipografia escalável (38vw com `tabular-nums`) para suportar placares de dois e três dígitos sem quebrar a tela.
* **Segurança em Dispositivos Móveis:** Todos os modais possuem limitação de altura (`max-h-[95vh]`) e barras de rolagem automáticas para perfeita navegação em smartphones e tablets.

## 🚀 Como Usar

A aplicação está disponível online e pode ser acedida de qualquer dispositivo com um navegador web.

### Acesso Online (Recomendado)

**➡️ [Acessar o Carcará Open TKD System](https://fbrenomoura.github.io/carcara_open_tkd_system/)**

### Execução Local

1. **Clone o Repositório:**
   ```bash
   git clone https://github.com/fbrenomoura/carcara_open_tkd_system.git
   cd carcara_open_tkd_system
   ```
2. **Execução:**
   Abra o arquivo `index.html` em qualquer navegador web moderno.

## 🛠️ Tecnologias Utilizadas

* **HTML5 / CSS3:** Estrutura semântica e estilização responsiva.
* **Tailwind CSS:** Framework utilitário para estilização e animações rápidas.
* **JavaScript (ES6+):** Lógica do combate, algoritmo de desempate, gerenciamento de estado e temporizadores.
* **Firebase (Firestore):** Sincronização de estado em tempo real, fila de ações e verificação de conectividade (*heartbeat*).

## 📝 Licença e Autor

Este projeto é de código aberto sob a **Licença MIT**.

* **Idealização e Desenvolvimento:** **Francisco Breno Moura Alves** (Atleta e Professor de Taekwondo - 1º DAN - Associação Parahyba Fighters).
* **Instagram:** [@fbrenomoura](https://www.instagram.com/fbrenomoura/)
* **LinkedIn:** [Francisco Breno Moura Alves](https://www.linkedin.com/in/fbrenomoura/)

---
*README atualizado em Julho de 2026.*
