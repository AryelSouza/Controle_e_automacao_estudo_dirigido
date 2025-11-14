# Capítulo 7 — O Método do Lugar das Raízes (Root Locus)

## 1. Introdução
O **Lugar das Raízes (LGR)** é uma ferramenta gráfica que mostra como os **polos da malha fechada** se deslocam no plano s conforme o **ganho K** varia de 0 a ∞.

É um dos métodos mais importantes do projeto de controladores, especialmente para:
- ajustar estabilidade
- ajustar rapidez de resposta
- ajustar amortecimento
- projetar compensadores (P, PI, PID, lag, lead)

---

## 2. Função de Transferência de Malha Fechada

\[
T(s) = \frac{K G(s)}{1 + K G(s)}
\]

Os polos da malha fechada são as raízes da equação:

\[
1 + K G(s) = 0
\]

O LGR mostra **para quais regiões do plano s** os polos se movem conforme K varia.

---

## 3. Regras Principais do LGR

### 3.1. Número de Ramos
Cada **polo de malha aberta** gera um ramo do LGR.

### 3.2. Assimptotas
Quando K → ∞, algumas raízes vão para o infinito.

\[
\theta_k = \frac{(2k+1)\pi}{n-m}
\]

\[
\sigma = \frac{\sum \text{Polos} - \sum \text{Zeros}}{n-m}
\]

### 3.3. Critério de Ângulo
Um ponto s pertence ao LGR se:

\[
\angle G(s) = (2k+1)\pi
\]

### 3.4. Critério de Magnitude
\[
K = \frac{1}{|G(s)|}
\]

---

## 4. Projeto por LGR
O LGR permite projetar:

- **Controladores P** (ajuste de ganho K)
- **Controladores PD / Lead**
- **Controladores PI / Lag**
- **Compensadores de fase**

Exemplo:
- deslocar polos para a esquerda → resposta mais rápida  
- aumentar amortecimento → resposta com menos overshoot  

---

## 5. Vantagens do Root Locus
- Visual e intuitivo  
- Fácil interpretar estabilidade  
- Mostra onde os polos estarão para qualquer K  
- Excelente para projeto manual de compensadores  

---

## 6. Conclusão
O método do LGR é fundamental para controle clássico e continua sendo amplamente usado na indústria e no ambiente acadêmico, servindo de base para ajustes de controladores modernos como PID, lead-lag e compensação de fase.
