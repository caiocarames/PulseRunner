# 🚲 Pulse Runner

**Pulse Runner** é um *Serious Game* (jogo sério) 2D desenvolvido para auxiliar na reabilitação motora de membros inferiores. Integrando uma bicicleta ergométrica via **IoT** ao framework **libGDX**, o jogo transforma o exercício fisioterapêutico em uma experiência gamificada, avaliando o progresso do paciente em tempo real.

Projeto acadêmico desenvolvido por **Caio Caramés Lanzelotti da Silva (RA: 10308718)**.

---

## 🎯 Objetivo do Projeto
O objetivo principal é promover o engajamento de pacientes em fisioterapia motora (pós-lesões de joelho/quadril, pós-AVC ou treinos leves) através de um jogo controlado **exclusivamente** pelos dados coletados de um dispositivo IoT (sensor de rotação/cadência na bicicleta ergométrica). O sistema avalia a consistência do ritmo do jogador para gerar métricas clínicas.

## ⚙️ Tecnologias Utilizadas
* **Engine/Framework:** [libGDX](https://libgdx.com/) (Java)
* **Plataforma Alvo:** Desktop
* **Hardware/IoT:** ESP32 + Sensor de Efeito Hall (para leitura de RPM e cadência)

## 🎮 O Jogo
### Premissa
O jogador assume o papel de um explorador/engenheiro pilotando um hovercraft ecológico em um mundo sem energia. Para restaurar usinas e biomas, o jogador precisa gerar energia cinética contínua através das pedaladas. Parar ou pedalar de forma irregular drena a propulsão do veículo.

### Mecânicas de Controle
* **Velocidade (RPM):** Controla o deslocamento horizontal do hovercraft.
* **Zona Alvo de Cadência:** Manter o ritmo na faixa ideal (ex: 50-65 RPM) estabiliza o veículo, gera energia extra e ativa escudos.
* **Ações de Pista:** Picos de pedalada ou inclinação (acelerômetro) para saltos e ultrapassagem de obstáculos.

## 🗺️ Fases e Progressão
O jogo conta com 3 níveis de dificuldade progressiva, focados em diferentes objetivos fisiológicos:

| Fase | Cenário | Objetivo Fisiológico | Mecânica In-Game |
| :--- | :--- | :--- | :--- |
| **1** | O Vale Solar | Aquecimento leve e mobilização (40-50 RPM) | Terreno plano para manter o hovercraft flutuando e coletar energia solar. |
| **2** | As Colinas Eólicas | Controle de ritmo e variação suave (55-65 RPM) | Ventos frontais exigem aumentos breves e controlados para vencer correntes contrárias. |
| **3** | O Reator Central | Resistência e treino intervalado (Estabilidade) | Zonas de cruzeiro e aceleração em resposta a alertas sonoros/visuais com limite de tempo. |

## 📊 Métricas de Reabilitação (Evaluation Screen)
Ao final de cada sessão, o jogo fornece um relatório clínico:
* **Índice de Consistência:** Desvio-padrão da cadência ao longo do tempo (ritmos estáveis dão bônus).
* **Tempo na Zona Alvo:** Porcentagem de tempo em que o paciente se manteve na faixa ideal de RPM.
* **Distância Estimada:** Progresso total entre sessões.
