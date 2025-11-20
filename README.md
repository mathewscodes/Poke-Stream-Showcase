# 🎮 Poke Stream - Browser Extension Game

![Status](https://img.shields.io/badge/STATUS-EM_DESENVOLVIMENTO-yellow?style=for-the-badge&logo=appveyor)

## 📖 Sobre o Projeto
O **Poke Stream** é um jogo complexo desenvolvido como extensão de navegador, focado em coleta e batalha de criaturas em tempo real. Diferente de jogos simples de clique, este projeto implementa lógicas matemáticas avançadas de RPG, interação em tempo real via WebSockets e persistência de dados.

O objetivo foi criar uma experiência fluida onde o mapa e os eventos reagem ao ambiente do jogador, utilizando tecnologias web modernas compatíveis com hospedagem padrão.

## 🛠️ Tech Stack & Arquitetura
* **Frontend:** HTML5, CSS3 (Animações/Responsividade), JavaScript (Vanilla).
* **Backend:** PHP (Lógica do servidor).
* **Banco de Dados:** MySQL (Gerenciamento de inventário, players e status).
* **Real-time:** Integração com **Ably (WebSockets)** para comunicação instantânea cliente-servidor sem necessidade de *polling*.
* **Autenticação:** Login social via Google (OAuth).

## ⚙️ Funcionalidades & Lógica Implementada

### 🌍 Mundo e Exploração
* **Geração Procedural de Spawns:** O sistema gera Pokémon aleatoriamente no mapa mundi, condicionado ao **tipo de bioma** atual.
* **Ciclo Dia/Noite:** Sistema de temas dinâmicos que altera visualmente a interface (botões, cenários) e afeta a jogabilidade.
* **Pokéstops:** Pontos de interação no mapa que geram recompensas aleatórias para o jogador.

### 🧮 Lógica Matemática e RPG (Hardcore Mechanics)
* **Cálculo de Status Realista:** Implementação fiel de estatísticas.
    * Fórmula: *Base Stats + IVs × Multiplicador CPM (Combat Power Multiplier)*.
    * Níveis calculados de 1 a 35.
* **Sistema de IVs (Individual Values):** Cada captura gera status únicos de Ataque, Defesa e Vida (escala 0-15), tornando cada unidade única.
* **Algoritmo de Captura:**
    * Cálculo probabilístico baseado em: *Rank do Pokémon + Tipo de Pokébola (4 tipos) + Uso de Berries (2 tipos) + Habilidade do Jogador*.
    * **Mecânica de Habilidade:** Bônus de taxa de captura para arremessos "Excelentes".
    * **Sistema de Fuga:** Lógica de risco baseada na dificuldade da captura e falhas consecutivas.

### ⚔️ Combate e Coleção
* **Sistema PVP:** Batalhas entre jogadores utilizando os status calculados.
* **Movesets Dinâmicos:** Ao capturar, a unidade recebe aleatoriamente um par de golpes (Ataque Rápido e Ataque Carregado).
* **Pokédex:** Registro automático e visual de criaturas já obtidas.
* **Shiny System:** Algoritmo de RNG (Random Number Generator) para gerar variantes raras (Shiny) individualmente por jogador.

## 🤖 Desenvolvimento com GenAI (Diferencial)
Este projeto foi concebido e arquitetado por mim, utilizando **Inteligência Artificial Generativa** como ferramenta de aceleração de desenvolvimento (Co-pilot).
* **Meu Papel:** Definição das regras de negócio, arquitetura do banco de dados, lógica matemática (fórmulas de CPM/IV), design de interface e integração do Ably.
* **Papel da IA:** Auxílio na escrita de sintaxe complexa de JavaScript/PHP, otimização de queries SQL e depuração de código (Debugging).

## 🚧 Status e Roadmap
O projeto encontra-se em desenvolvimento ativo (fase Beta). As principais mecânicas já estão funcionais, e o foco atual está em:

- [x] Sistema de Captura e Cálculos de IV (Concluído)
- [x] Integração WebSocket e Mapa Mundi (Concluído)
- [ ] Implementação da tela de Batalhas PVP
- [ ] Implementação da tela Pokédex
- [ ] Implementação da tela "Meus Pokémon"
- [ ] Implementação do sistema de Trocas (Trade System) entre jogadores
- [ ] Otimização de queries no Banco de Dados para maior escala
- [ ] Refatoração do Front-end para melhor responsividade

## 📸 Demonstração

[Tela de Login](https://github.com/user-attachments/assets/1bada5fa-285d-468a-8884-6418b2d11fb8) [Mapa Mundi](https://github.com/user-attachments/assets/3ea2344e-0811-4c75-b678-f158613e6c8b)


[Demonstração Pokéstop](https://github.com/user-attachments/assets/32c40d50-cc84-4912-a4ed-233fe854f978)


[Popup](https://github.com/user-attachments/assets/ed446f7e-1011-4d22-8e77-eaf77d00dba2)


[Demonstração Captura](https://github.com/user-attachments/assets/41121e4a-ef7d-4cd5-862f-a5b57f585465)


---
*Este repositório serve como portfólio demonstrativo das minhas capacidades técnicas em lógica de programação e desenvolvimento Full Stack. Devido à natureza autoral do projeto, o código-fonte permanece privado.*
