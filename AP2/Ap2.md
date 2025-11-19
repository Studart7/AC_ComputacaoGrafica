# **Relatório da Animação – AP2 Blender**  
### *Materiais, Texturas, Conceito e Desafios*

---

## **1. Escolhas de Materiais e Texturas**

### **Ponte**
A ponte utilizada na animação foi a mesma criada na AP1, porém passou por um novo processo de **UV Unwrapping mais otimizado**.  
- A textura de madeira foi aplicada de forma mais uniforme para evitar esticamentos.  
- Não foi necessário polir com perfeição, porque a **iluminação geral da cena é baixa**, então detalhes muito finos não apareceriam com clareza.  
- O material utiliza **Principled BSDF**, com valores de *Roughness* e *Specular* ajustados para simular madeira fosca.

### **Terreno, Tronco da Árvore e Estrutura do Portal**
Esses elementos possuem:
- **Texturas customizadas**, aplicadas com **UV mapping específico** para cada objeto.  
- Uso de mapas de **Normal** para aprofundar detalhes como fissuras, musgo e irregularidades da terra.  
- *Roughness maps* foram utilizados para controlar a dispersão da luz sobre superfícies irregulares.  

Esses materiais reforçam a ideia de terreno alienígena, misturando características de solo seco e rochas desgastadas.

### **Água / Oceano Escuro**
Como o planeta é descrito como um “deserto de oceano”, a água tem:
- Rugosidade baixa em algumas áreas e mais alta em outras para simular uma superfície irregular.  
- Reflexos sutis vindos da iluminação avermelhada da atmosfera.  
- Movimento leve através de um *normal map animado*.

### **Portal**
O portal é composto por:
- Material com **Emit** para simular energia interna.  
- Animação de intensidade para acompanhar o momento em que o portal “acende”.  
- Elementos circulares (tipo vórtice) usando *color ramp* e textura procedural.

Como **Emit sozinho não ilumina fisicamente a cena**, foi adicionada uma **luz auxiliar com keyframes**, sincronizada com:
- Cor do portal  
- Intensidade emitida  

Isso reforçou o efeito de brilho no ambiente e os reflexos no chão e no robô.

### **Robô**
O robô tem:
- Materiais com metalicidade moderada (PBR).  
- Emissão no pequeno LED vermelho de sua cabeça.  
- Detalhes simples pois o personagem é secundário, mas com brilho suficiente para destacá-lo na escuridão.

---

## **2. Conceito da Animação Criada**

A animação se passa em um **exoplaneta distante**, localizado a milhares de anos-luz da nossa galáxia. Por isso:

### **Atmosfera e Iluminação**
- A atmosfera é diferente da Terra, permitindo **visibilidade total das estrelas** sem poluição luminosa.  
- Uma das luas do planeta tem uma composição atmosférica que refrata luz com **temperatura de cor mais quente**, tornando toda a iluminação levemente avermelhada.  
- Essa cor inspirou a iluminação global da cena.

### **Narrativa**
- O robô de *Rick and Morty* está perdido nesse mundo estranho.  
- Ele encontra um **portal instável**, começando a reacender.  
- Quando percebe que pode voltar para sua dimensão original, inicia a travessia da ponte.  
- Assim que se aproxima do portal, o robô **reduz de tamanho**, pois na série ele é apenas um pouco maior que uma barra de manteiga, esse detalhe foi incorporado para fidelidade à série (junto com a cor do portal ser verde).  
- A progressão da câmera e da iluminação sugere tensão e expectativa, culminando no momento em que ele finalmente entra no portal.

---

## **3. Animação e Técnicas Utilizadas**

### **Robô**
- **Keyframes de posição e rotação** para criar uma caminhada mais fluida a partir do path ja existente.  
- Pequenos movimentos ao passar pela rocha aumentam o realismo.  
- Keyframes aplicados também na escala para simular o encolhimento entrando no portal.

### **Portal**
- A luz auxiliar sincronizada reforça o efeito de energia pulsante.  
- O material emissivo é animado para dar a sensação de “ativação”.

### **Câmera**
- Uso de keyframes na **localização e rotação**.  
- A câmera segue um caminho fluido e cinematográfico, aproximando o espectador da narrativa.  
- Movimentos suaves e controlados aumentam imersão.


---

## **4. Desafios Encontrados e Soluções**

### **1. Iluminação com Emission**
- *Problema:* Emit não ilumina de verdade.  
- *Solução:* Adição de uma luz real (Area) com keyframes de cor e força.

### **2. Interpolação da Câmera**
- *Problema:* Movimentos indesejados durante transições.  
- *Solução:* Ajustes manuais nas propriedades da câmera ao longo da trajetória.a

### **3. UV Mapping da Ponte**
- *Problema:* A textura estava esticando devido ao mapeamento anterior da AP1.  
- *Solução:* Novo unwrap mais limpo para distribuir a textura de madeira uniformemente.

### **4. Atmosfera Alienígena**
- *Problema:* O ambiente precisava parecer extraterrestre sem exagero.  
- *Solução:* Uso de HDRI de céu estrelado + coloração mais quente vinda das luzes principais.


---

