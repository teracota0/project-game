# **Prjeto Jogo - Documento de Conceito**  
*(Versão 0.1)*  

## **1. Visão Geral**  
- **Objetivo**: Criar um jogo tático multiplayer roguelike baseado em turnos com elementos de realismo (stamina, ciclos de treinamento longo) e progressão estratégica.  
- **Diferenciais**:  
  - Combate em grid hexagonal com ação-reação.  
  - Unidades vinculadas a facções (não são indivíduos permanentes).  
  - Progressão lenta (treinos demoram meses/anos simulados).  

## **2. Mecânicas Principais**  
### **2.1. Combate** 
- Campanha: cada partida é uma campanha que dura algumas décadas
- Ciclos: existem vários ciclos que se repetem 
  - ...
  - Preparação: quantidade de tempo ocioso que é investido em treino, criação de itens, aumento de influência, coisas assim que levam tempo
  - Movimentação: com custo de tempo e recursos (X horas e Y de ATP) para cada hexagono 
  - Conflito: quando unidades "inimigas" se tocam inicia-se um conflito que pode ser resolvido em combate, duelo ou com diágolo, a serem definidos.
  - Morte: quando a unidade morre algumas coisas podem acontecer mas a mais simples é que um novo heroi do seu clã substitui o heroi morto.
- Relógio global: tempo é universal para todos 
- **Sistema de turnos**:  
  - Fases por unidade (movimento → ação → reação).  
  - Timer por turno (ex: 30 segundos).  
- **Atributos realistas**:  
  - Fadiga acumulativa.  
  - Idade afeta performance (unidades mais jovens são menos experientes).  

### **2.2. Progressão**  
- **Ciclos de treinamento**:  
  - Melhoria de atributos demanda tempo (ex: +Força após 1 ano de treino).  
  - Escolha estratégica de habilidades para desenvolver.  
- **Morte e reposição de unidades**:  
  - Unidades mortas são substituídas por recrutas mais jovens.  

### **2.3. Multiplayer**  
- **Modos**:  
  - Partidas PvP (1v1, 2v2).  
  - Ladder com ranking de facções.  
- **Sincronização**:  
  - Servidor central gerencia estado do jogo.  


## **3. Fluxo do Jogo**  
1. **Fase de Treino**:  
   - Jogador seleciona habilidades para treinar.  
   - Tempo real simulado (ex: 1 ano = 5 minutos de jogo).  
2. **Fase de Combate**:  
   - Partidas multiplayer com grid hexagonal.  
3. **Fase de Recuperação**:  
   - Unidades lesionadas se curam.  
   - Novas unidades são recrutadas.  

## **5. Requisitos Não-Funcionais**  
- **Performance**: 60 FPS no cliente (C++ otimizado).  
- **Segurança**: Autenticação via JWT e validação server-side.  
- **Modularidade**: Separação clara entre lógica de jogo e renderização.  

## **6. Roadmap**  
| Fase | Entregáveis |  
|------|------------|  
| 1    | Protótipo do grid hexagonal + movimento básico (C++/SDL2) |  
| 2    | Sistema de turnos e atributos (stamina, idade) |  
| 3    | Integração com servidor Java (WebSockets) |  
| 4    | Matchmaking e persistência (PostgreSQL) |  

## **7. Referências**  
- **Inspirações**: Digimon 2, Dota 2, Final Fantasy Tactics, MMORPGS  
- **Técnicas**:  
  - Pathfinding em hex grid (Axial Coordinates).  
  - Padrão de rede Client-Server com lockstep.  

---

### **Como Usar Este Documento**  
1. Preencha cada seção com detalhes adicionais conforme o projeto evolui.  
2. Use como base para discussões técnicas (ex: "Como implementar o grid hexagonal?").  
3. Atualize o roadmap conforme marcos forem concluídos.  
